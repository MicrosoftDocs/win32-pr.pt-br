---
Descrição: para acessar dados de contador em um computador remoto: o computador remoto deve ter o serviço de registro remoto habilitado. A exceção de compartilhamento de arquivo e impressão deve ser selecionada nas configurações do firewall do Windows. antes do Windows Vista: o serviço registro remoto está habilitado por padrão.
MS. AssetID: 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 título: acessando dados do contador remoto MS. tópico: artigo MS. Date: 08/17/2020
---

# <a name="accessing-remote-counter-data"></a>Acessando dados de contador remoto

Para acessar dados do contador em um computador remoto:

- O computador remoto deve ter o serviço de registro remoto habilitado.
- A exceção de **compartilhamento de arquivo e impressão** deve ser selecionada nas **configurações do firewall do Windows**.

**Antes do Windows Vista:** O serviço registro remoto é habilitado por padrão.

> [!NOTE]
> Ferramentas e APIs do contador de desempenho do Windows incluem suporte limitado para acessar contadores de desempenho de outros computadores por meio de RPC (para provedores v2) e registro remoto (para provedores v1). Esse suporte é muitas vezes difícil de usar em termos de controles de autenticação (as ferramentas e as APIs só podem ser autenticadas como o usuário atual), bem como em termos de configuração do sistema (os pontos de extremidade e serviços necessários são desabilitados por padrão na maioria dos sistemas). Em muitos casos, é melhor acessar os contadores de desempenho de sistemas remotos via [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) em vez de por meio do suporte interno a acesso remoto.
