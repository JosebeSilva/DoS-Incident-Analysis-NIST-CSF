# Análise de Incidente: Ataque DoS e Framework NIST CSF

Este projeto faz parte do meu portfólio de Cibersegurança e foi desenvolvido durante o curso **Google Cybersecurity Professional Certificate**. 

Nesta atividade, assumo o papel de Analista de Segurança Cibernética para uma empresa de multimídia, utilizando o framework NIST CSF para gerenciar a resposta a um ataque de interrupção de serviços.

---

## O Cenário

A organização sofreu um ataque DoS (Negação de Serviço) que paralisou a rede interna por duas horas. Durante o incidente, os serviços pararam de responder devido a uma enxurrada de pacotes ICMP (Ping Flood) que explorou um firewall não configurado.

Minha missão foi analisar o evento e criar um plano de melhoria baseado nas cinco funções do **NIST Cybersecurity Framework (CSF)** para evitar que novas sobrecargas ocorram.

## Ferramentas e Tecnologias Exploradas

*   **Framework de Segurança:** NIST CSF (Identify, Protect, Detect, Respond, Recover).
*   **Controles de Rede:** Firewall (Rate Limiting), IDS/IPS.
*   **Monitoramento:** Verificação de IP de origem (Anti-spoofing) e análise de padrões de tráfego.

---

## A Investigação (NIST CSF)

Utilizei as etapas do framework para organizar a análise técnica e o plano de ação:

1.  **Identify (Identificar):** Determinei que o ataque foi um *ICMP flood* direcionado a um firewall vulnerável. Identifiquei que todos os recursos da rede interna foram impactados.
2.  **Protect (Proteger):** Implementei limites de taxa (*rate limiting*) para pacotes ICMP no firewall e configurei sistemas IDS/IPS para filtrar tráfego baseado em assinaturas suspeitas.
3.  **Detect (Detectar):** Configurei a verificação de endereços IP de origem no firewall para identificar pacotes forjados (*spoofing*) e instalei softwares de monitoramento para alertar sobre picos anômalos de tráfego.
4.  **Respond (Responder):** Estabeleci protocolos de isolamento de sistemas afetados, análise de logs pós-incidente e comunicação formal com a alta administração e autoridades competentes.
5.  **Recover (Recuperar):** Defini uma estratégia de restauração gradual, priorizando serviços críticos de negócios antes de reestabelecer sistemas não essenciais após a estabilização da rede.

## Minha Conclusão

Este incidente destacou como uma falha de configuração básica em um firewall pode expor toda a infraestrutura de uma empresa. A aplicação do NIST CSF permitiu não apenas resolver o problema imediato, mas criar uma estratégia de defesa em profundidade.

**Principais melhorias implementadas:**
*   Bloqueio automático de ataques de flood no perímetro.
*   Visibilidade em tempo real do tráfego de rede para detecção precoce.
*   Plano de contingência para restauração rápida de serviços críticos.

> **O que aprendi com isso:** Reforcei meu conhecimento sobre a importância da resiliência de rede e como frameworks padronizados ajudam a transformar um caos operacional em um processo estruturado de recuperação e fortalecimento de segurança.

---
*Fique à vontade para explorar a análise completa do relatório de incidente disponível neste repositório!*
