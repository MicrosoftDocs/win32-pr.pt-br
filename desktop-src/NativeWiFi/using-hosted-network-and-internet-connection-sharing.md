---
title: Usar rede hospedada sem fio, compartilhamento de conexão com a Internet
description: Usando rede hospedada sem fio e compartilhamento de conexão com a Internet
ms.assetid: 56e86ef8-f759-4e56-a591-74e03430125a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972774e921199e32eb70841c74c7478e2178cda9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921631"
---
# <a name="use-wireless-hosted-network-internet-connection-sharing"></a>Usar rede hospedada sem fio, compartilhamento de conexão com a Internet

A rede hospedada sem fio é um novo recurso de WLAN com suporte no Windows 7 e no Windows 8. Ele também tem suporte no Windows Server 2012 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado. Esse recurso implementa duas funções principais:

-   A virtualização de um adaptador sem fio físico em mais de um adaptador sem fio virtual, às vezes chamado de Wi-Fi virtual.
-   Um AP (ponto de acesso sem fio) baseado em software é, às vezes, chamado de SoftAP que usa um adaptador sem fio virtual designado.

O ICS (compartilhamento de conexão com a Internet) é um recurso do Windows fornecido por meio do serviço SharedAccess. Estritamente falando, o SharedAccess permite o compartilhamento de rede por meio de um computador em que o acesso à rede compartilhada não fornece necessariamente acesso à Internet. Usamos o termo ICS e SharedAccess interalteradomente nesta seção, pois o compartilhamento de conexão com a Internet é um cenário importante para a rede hospedada sem fio e o termo de ICS é mais bem conhecido para a comunidade de usuários.

A rede hospedada sem fio está fortemente ligada ao ICS para habilitar a PAN (Wireless personal Area Network) e os cenários de compartilhamento de Internet. Esta seção fornece recomendações gerais para os desenvolvedores de aplicativos sobre como integrar a rede hospedada sem fio e o ICS usando a rede hospedada pública sem fio e as APIs de ICS.

## <a name="internet-connection-sharing"></a>Compartilhamento de Conexão com a Internet

O serviço ICS opera em um dos dois modos possíveis:

-   Modo autônomo

    Somente a função de servidor DHCPv4 está operando quando o serviço ICS é invocado. Esse é um modo de operação especial para o ICS e só é disponibilizado por meio da rede hospedada sem fio. Um usuário ou aplicativo não é capaz de iniciar e parar diretamente o ICS autônomo por meio de APIs ICS públicas ou comandos **netsh** . Iniciar a rede hospedada sem fio normalmente envolve iniciar o ICS no modo autônomo para usar a função de servidor DHCPv4 para fornecer endereços IPv4 privados para dispositivos conectados. A comunicação de rede para os dispositivos conectados é limitada ao envio e ao recebimento de pacotes de rede entre um dispositivo conectado e o computador local que hospeda a rede hospedada sem fio e entre os próprios dispositivos conectados. Isso efetivamente habilita o cenário de rede de área pessoal sem fio para a rede hospedada sem fio.

-   Modo completo

    Todos os recursos do ICS estão operando quando o serviço é invocado, como a conversão de endereços de rede e as funções de servidor DHCP para IPv4 e IPv6. Esse é o modo normal de operação para ICS. Um usuário ou aplicativo pode iniciar e parar o modo ICS completo por meio de APIs públicas ou comandos do NetShell. Por exemplo, esse serviço pode ser interrompido usando net stop SharedAccess em um prompt de comandos com privilégios elevados. Combinando a rede hospedada sem fio com o ICS completo, a comunicação de rede para os dispositivos conectados não é limitada à PAN sem fio. Qualquer dispositivo conectado tem acesso à rede (como a Internet) por meio da conexão de rede compartilhada do computador que executa a rede hospedada sem fio. Isso efetivamente habilita o cenário de compartilhamento de rede para a rede hospedada sem fio.

Nesta seção, usamos o termo ICS completo para significar o caso em que todas as funções ICS são invocadas no serviço ICS para fornecer acesso a todos os recursos do ICS completos com a rede hospedada sem fio.

Os dois modos de operação do ICS são mutuamente exclusivos com o ICS completo com precedência mais alta. O serviço ICS pode fazer a transição do modo autônomo para o modo completo, mas não do modo completo para o modo autônomo. O modo autônomo do ICS foi introduzido no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado em conjunto com o recurso de rede hospedada sem fio. Ele não está disponível em versões anteriores do Windows.

Qualquer operação ICS completa envolve dois adaptadores de rede diferentes no sistema:

-   A interface pública. Essa é a interface de rede com acesso à Internet. É essa interface que o computador local que está executando o ICS usa para compartilhar a Internet com clientes e dispositivos que se conectam a ele por meio de SoftAP.
-   A interface privada. Essa é a interface de rede que outros dispositivos usam para se conectar ao computador local que está executando o ICS. Um servidor DHCPv4 está sendo executado nessa interface privada para fornecer endereços IP locais privados para os outros computadores remotos.

Quando a interface pública não tem acesso à Internet, o servidor DHCP na interface privada continua a fornecer endereços IP locais para os dispositivos conectados. O ICS autônomo envolve apenas a interface privada na qual o SoftAP está em execução; Ele não envolve nenhuma interface pública.

A qualquer momento, há no máximo uma instância do ICS completo em execução no computador local. Se o ICS completo já estiver em execução no computador local, iniciar outro ICS completo apresentará os seguintes comportamentos funcionais:

-   Se as interfaces pública e privada do novo ICS completo forem as mesmas que o ICS completo existente, iniciar o segundo ICS completo será equivalente a um não op.
-   Se a nova interface pública for diferente da interface pública antiga, mas a nova interface privada for a mesma interface privada antiga, iniciar um segundo ICS completo terá pouco impacto nos dispositivos conectados na mesma interface privada. A capacidade de acessar a Internet pode mudar com a nova interface pública.
-   Se a nova interface privada for diferente da interface privada antiga, as funções do ICS deixarão de funcionar na interface privada antiga e começarão a ser aplicadas à nova interface privada. Qualquer dispositivo remoto conectando-se ao computador local usando a interface privada antiga perderá a conectividade IP com o computador local.

Quando o ICS completo já estiver em execução, invocar um segundo ICS completo será interrompido em dispositivos conectados remotamente usando a interface privada antiga, desde que a segunda integração de ICS use uma nova interface privada diferente.

Para gerenciar e usar o serviço ICS para dar suporte à integração de ICS com a rede hospedada sem fio, um aplicativo de software deve primeiro obter uma interface [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) . A interface **INetSharingManager** fornece acesso direta ou indiretamente a todas as outras interfaces com na API do ICS. O método [**Get \_ SharingInstalled**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_sharinginstalled) na interface **INetSharingManager** relata se o computador local dá suporte ao compartilhamento de conexão. O método [**Get \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) na interface **INetSharingManager** recupera uma interface de enumeração para todas as conexões na pasta Connections. O método [**Get \_ INetSharingConfigurationForINetConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection) recupera uma interface [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) para a conexão especificada. Os métodos na interface **INetSharingConfiguration** podem ser usados para consultar e alterar as configurações de ICS.

A rede hospedada sem fio deve ser iniciada antes de chamar o método [**Get \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) na interface [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) para enumerar todas as conexões na pasta Connections.

Para obter informações sobre o ICS e as interfaces públicas e os métodos que podem ser usados para consultar e alterar as configurações de ICS, consulte a documentação sobre [compartilhamento de conexão com a Internet e firewall de conexão com a Internet](/previous-versions/windows/desktop/ics/about-internet-connection-sharing-and-internet-connection-firewall).

## <a name="hosted-network-and-ics-integration"></a>Integração de rede hospedada e ICS

Quando o ICS completo não está em execução, iniciar uma rede hospedada sem fio também inicia internamente o serviço do ICS no modo autônomo apenas com a função de servidor DHCPv4 para alocar endereços IP para os dispositivos conectados na interface de rede hospedada sem fio. O intervalo de endereços de sub-rede para o servidor DHCPv4 autônomo é 192.168.173.0/24. Isso é diferente do intervalo de sub-rede de 192.168.137.0/24 usado com o ICS completo.

Iniciar uma rede hospedada sem fio com o ICS completo emprega a seguinte lógica:

-   Se o ICS completo ainda não estiver em execução, iniciar uma rede hospedada sem fio também iniciará o serviço ICS com o servidor DHCPv4 autônomo.
-   Se o ICS completo já estiver em execução e a interface privada for a interface de rede hospedada sem fio, basta iniciar a rede hospedada sem fio.
-   Se o ICS completo já estiver em execução, mas a interface privada não for a interface de rede hospedada sem fio, a rede hospedada sem fio será iniciada sem a função de servidor DHCPv4 na interface de rede hospedada sem fio.

O impacto da lógica acima realça os seguintes fatos:

-   O ICS não faz a transição do modo completo para o modo autônomo.
-   O modo autônomo só pode ser chamado pela rede hospedada sem fio quando o ICS não está em execução no modo completo.
-   Se o ICS estiver sendo executado no modo autônomo, ele será admitido em modo completo se um usuário ou aplicativo iniciar o ICS no modo completo.
-   A transição do modo autônomo para o modo completo no ICS causará interrupções nos dispositivos conectados na PAN sem fio se a interface privada do ICS completo não for a mesma do SoftAP.

Demora um tempo para iniciar ou parar o serviço ICS no computador local no modo completo ou autônomo. Um aplicativo deve verificar o estado do serviço ICS usando a função **NotifyServiceStatusChange** para garantir que o serviço ICS não esteja no estado iniciar/parar pendente antes de iniciar ou parar a rede hospedada sem fio para uso com a integração do ICS.

## <a name="starting-and-stopping-the-wireless-hosted-network"></a>Iniciando e parando a rede hospedada sem fio

O Windows fornece uma plataforma na qual mais de um aplicativo simultâneo tem permissão para gerenciar uma rede hospedada sem fio ao mesmo tempo. Especificamente, cada aplicativo pode iniciar e parar a rede hospedada sem fio por conta própria, sem conhecimento prévio sobre outros aplicativos.

Há dois conjuntos de funções para iniciar e parar uma rede hospedada.

Vários aplicativos podem exigir o uso da rede hospedada sem fio. As funções [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) e [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) iniciam e interrompem um entrada na rede hospedado sem fio de uma maneira compatível com outros aplicativos simultâneos. As funções **WlanHostedNetworkStartUsing** e **WlanHostedNetworkStopUsing** permitem que um aplicativo tenha uma referência à rede hospedada sem fio. Esse mecanismo mantém a rede hospedada sem fio em execução desde que pelo menos um outro aplicativo tenha uma referência atual à rede hospedada sem fio. Qualquer usuário pode chamar essas funções. As chamadas com êxito para **WlanHostedNetworkStartUsing** devem ser combinadas por chamadas para a função **WlanHostedNetworkStopUsing** . Qualquer alteração de estado de rede hospedada causada pela função **WlanHostedNetworkStartUsing** seria automaticamente desfeita se o aplicativo de chamada fechar seu identificador de chamada (chamando [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) com o mesmo parâmetro *hClientHandle* passado para **WlanHostedNetworkStartUsing**) ou se o processo terminar.

As funções [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) e [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) forçam a iniciar e interromper uma rede hospedada sem fio. Essas funções só poderão ser chamadas se o usuário tiver o privilégio elevado apropriado. As chamadas bem-sucedidas para **WlanHostedNetworkForceStart** podem eventualmente ser correspondidas por uma chamada para a função **WlanHostedNetworkForceStop** , dependendo do design do aplicativo. Essas funções passam o estado da rede hospedada sem fio sem associar a solicitação ao identificador de chamada do aplicativo. Qualquer alteração de estado de rede hospedada causada pela função **WlanHostedNetworkForceStart** não será desfeita automaticamente se o aplicativo de chamada fechar seu identificador de chamada (chamando [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) com o mesmo parâmetro *hClientHandle* passado para [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)) ou se o processo terminar. Se o aplicativo que chamou a função **WlanHostedNetworkForceStart** fechar sem chamar uma das funções para interromper a rede hospedada sem fio, a rede hospedada será deixada em execução. Um aplicativo pode chamar a função **WlanHostedNetworkForceStart** depois de garantir que um usuário de sistema elevado aceite os requisitos de energia maiores envolvidos na execução da rede hospedada sem fio por longos períodos de tempo.

As recomendações gerais sobre quais funções chamar para iniciar e parar uma rede hospedada sem fio são as seguintes:

-   Use as funções [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) e [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) dentro de um aplicativo para iniciar e parar uma rede hospedada sem fio.
-   Não use a função [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) para iniciar uma rede hospedada sem fio, a menos que seja absolutamente exigido pelo aplicativo. A função **WlanHostedNetworkForceStart** também requer privilégios elevados.
-   Use apenas a função [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) como método de recuperação. A função **WlanHostedNetworkForceStop** faz com que uma rede hospedada sem fio pare imediatamente. Outros aplicativos que escutam notificações de rede hospedada sem fio podem precisar fazer ações de recuperação. Para obter mais informações, consulte a discussão abaixo sobre a sequência de recuperação para rede hospedada sem fio.

## <a name="start-sequence-for-wireless-hosted-network"></a>Iniciar sequência para rede hospedada sem fio

Para um aplicativo que inicia uma rede hospedada sem fio com o ICS completo, a recomendação é iniciar a rede hospedada sem fio e iniciar o ICS completo. Se uma rede hospedada sem fio já estiver em execução, um aplicativo deverá usar a função [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para interromper a rede hospedada sem fio somente se o ICS completo for necessário, mas não tiver sido habilitado antes de a rede hospedada ser iniciada. Isso permitirá que outros aplicativos se recuperem de possíveis interrupções causadas pelo início do ICS completo. Para obter mais informações, consulte a discussão abaixo sobre a sequência de recuperação para rede hospedada sem fio. A operação combinada deve ter êxito e falhar como um todo.

> [!Note]  
> A rede hospedada sem fio deve ser iniciada antes de tentar enumerar o adaptador correspondente usando a interface [**IEnumNetSharingEveryConnection**](/windows/win32/api/netcon/nn-netcon-ienumnetsharingeveryconnection) .

 

As etapas ordenadas a seguir são a sequência inicial recomendada em um aplicativo usando a rede hospedada sem fio com o ICS completo:

-   Chame a função [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) para verificar se a rede hospedada sem fio está configurada e pronta para ser usada.
-   Chame as funções [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) e [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty) para determinar se a rede hospedada sem fio é permitida e está disponível. Se a rede hospedada sem fio não for permitida e não estiver disponível, retorne um erro.
-   Teste para ver se o serviço ICS usado para o ICS completo é permitido. Se o serviço ICS não puder ser iniciado, retorne um erro.
-   Chame a função [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para forçar uma interrupção da rede hospedada sem fio.
-   Chame a função [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) para iniciar a rede hospedada sem fio.
-   Se a rede hospedada sem fio falhar ao iniciar, retorne um erro.
-   Se o ICS completo já estiver em execução e a interface pública ou privada atual for diferente da nova interface a ser usada, armazene em cache as interfaces públicas e privadas atuais. Um aplicativo também pode optar por retornar um erro ou avisar o usuário se a integração com o ICS já estiver em execução.
-   Inicie o ICS completo com as novas configurações para as interfaces pública e privada.
-   Se o ICS completo não conseguir iniciar com essas configurações, tente iniciar o serviço ICS completo com as interfaces pública e privada em cache se o ICS completo estiver em execução antes. Chame a função [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para interromper a rede hospedada sem fio e retornar um erro.
-   Retorne o êxito de que a rede hospedada sem fio e o ICS completo tenham êxito.

## <a name="stop-sequence-for-wireless-hosted-network"></a>Parar sequência para rede hospedada sem fio

Ao usar a rede hospedada sem fio com o ICS completo, um aplicativo que concluiu seu trabalho pode querer interromper a rede hospedada sem fio e o serviço do ICS usado para o ICS completo. Nesse caso, é recomendável que a função [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) seja chamada para parar a rede hospedada em vez de chamar a função [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) . A função **WlanHostedNetworkForceStop** interrompe a rede hospedada sem fio e também serve para permitir que outros aplicativos se recuperem. Para obter mais informações, consulte a discussão abaixo sobre a sequência de recuperação para rede hospedada sem fio.

As etapas ordenadas a seguir são a sequência de parada recomendada em um aplicativo usando a rede hospedada sem fio e o ICS completo:

-   Pare o ICS completo.
-   Chame a função [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para interromper a rede hospedada sem fio.

Um aplicativo que usa uma rede hospedada sem fio sem o ICS completo que termina com seu trabalho só precisa chamar a função [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) ou [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para interromper a rede hospedada sem fio. Se a função [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) foi chamada para iniciar a rede hospedada sem fio, o aplicativo deverá chamar a função **WlanHostedNetworkStopUsing** para interromper a rede hospedada sem fio. Se a rede hospedada sem fio já tiver sido iniciada antes de o aplicativo ou o aplicativo ter chamado a função [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) para forçar o início da rede hospedada sem fio, o aplicativo poderá chamar a função **WlanHostedNetworkForceStop** para interromper a rede hospedada sem fio ou não fazer nada (deixar a rede hospedada sem fio iniciada) dependendo do cenário.

## <a name="recovery-sequence-for-wireless-hosted-network"></a>Sequência de recuperação para rede hospedada sem fio

Um aplicativo que usa a rede hospedada sem fio pode ser afetado pelas ações de outros aplicativos. O serviço ICS e as interfaces para gerenciar o ICS não fornecem nenhum método para um aplicativo se registrar para notificações de alteração de ICS. Se outro aplicativo chamar os métodos [**EnableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-enablesharing) ou [**DisableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing) na interface [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) para habilitar ou desabilitar o compartilhamento em uma conexão, uma mensagem será enviada para a interface do usuário (a tela) no computador local, não para outros aplicativos. Portanto, um aplicativo precisa contar com as notificações de rede hospedada sem fio para executar ações de recuperação quando ocorrerem alterações de rede hospedada sem fio ou ICS.

Um aplicativo que usa a rede hospedada sem fio deve se registrar para notificações de rede hospedada sem fio chamando o [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification). Se as notificações para apenas a rede hospedada sem fio forem necessárias, o aplicativo deverá passar a **fonte de notificação de WLAN \_ \_ \_ HNWK** no parâmetro *dwNotifSource* passado para o **WlanRegisterNotification**. Se outras notarções sem fio também forem necessárias, **a \_ fonte de notificação de WLAN \_ \_ HNWK** deverá ser combinada com as constantes de origem de notificação para outros tipos de notificações sem fio desejadas e passar esse valor no parâmetro *dwNotifSource* .

A sequência de recuperação é a mesma para aplicativos com ou sem o ICS completo, supondo que os aplicativos não desejam iniciar o serviço ICS novamente. Após receber uma notificação de rede hospedada sem fio que a rede hospedada parou, faça o seguinte:

-   Se o aplicativo chamou [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) para iniciar a rede hospedada sem fio, reinicie a rede hospedada chamando **WlanHostedNetworkForceStart**. Caso contrário, chame [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) para reiniciar a rede hospedada sem fio.

## <a name="recovery-sequence-for-connected-devices"></a>Sequência de recuperação para dispositivos conectados

Dispositivos remotos ou computadores conectados à rede hospedada sem fio podem ser afetados pelas ações de outros aplicativos que afetam o ICS e a rede hospedada sem fio. Felizmente, a maioria dos dispositivos tem lógica de repetição interna no aplicativo do dispositivo para lidar com uma perda temporária de sinal ou roaming.

Uma possível sequência de recuperação para dispositivos ou computadores conectados à rede hospedada sem fio que perde o contato é a seguinte:

-   O driver de dispositivo sem fio indica uma desconexão de mídia com as camadas superiores da pilha de rede no dispositivo.
-   O aplicativo do dispositivo inicia verificações periódicas para a disponibilidade da rede hospedada sem fio.
-   Depois que o aplicativo do dispositivo detectar novamente a rede hospedada sem fio, o dispositivo iniciará uma conexão sem fio.
-   Após uma conexão bem-sucedida com a rede hospedada sem fio, o aplicativo do dispositivo atualiza suas configurações de IP adequadamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a rede hospedada sem fio](about-the-wireless-hosted-network.md)
</dt> <dt>

[Exemplo de rede hospedada sem fio](wireless-hosted-network-sample.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 
