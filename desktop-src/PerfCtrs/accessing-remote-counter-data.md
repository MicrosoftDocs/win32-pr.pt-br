---
description: para acessar dados do contador em um computador remoto: o computador remoto deve ter o serviço registro remoto habilitado. A exceção Compartilhamento de Arquivos e Impressão deve ser selecionada Windows Firewall Configurações. Antes do Windows Vista: o serviço registro remoto está habilitado por padrão.
ms.assetid: 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 título: Acessando dados do contador remoto ms.topic: artigo ms.date: 17/08/2020
---

# <a name="accessing-remote-counter-data"></a>Acessando dados do contador remoto

Para acessar dados do contador em um computador remoto:

- O computador remoto deve ter o serviço registro remoto habilitado.
- A **exceção Compartilhamento de** Arquivos e Impressão deve ser selecionada **Windows Firewall Configurações**.

**Antes do Windows Vista:** O serviço registro remoto está habilitado por padrão.

> [!NOTE]
> Windows As APIs e ferramentas do Contador de Desempenho incluem suporte limitado para acessar contadores de desempenho de outros máquinas por meio de RPC (para provedores V2) e Registro Remoto (para provedores V1). Esse suporte geralmente é difícil de usar em termos de controles de autenticação (as ferramentas e APIs só podem se autenticar como o usuário atual), bem como em termos de configuração do sistema (os pontos de extremidade e serviços necessários são desabilitados por padrão na maioria dos sistemas). Em muitos casos, é melhor acessar os contadores de desempenho de sistemas remotos via [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) em vez de por meio do suporte interno de acesso remoto.
