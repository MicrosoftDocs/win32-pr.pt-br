---
description: Sobre a rede hospedada sem fio
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Sobre a rede hospedada sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88af34a1e0df2029c230b7b7800130d3b550dbf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882765"
---
# <a name="about-the-wireless-hosted-network"></a>Sobre a rede hospedada sem fio

A Rede Hospedada sem fio é um novo recurso WLAN com suporte no Windows 7 e no Windows Server 2008 R2 com o Serviço lan sem fio instalado. Esse recurso implementa duas funções principais:

-   A virtualização de um adaptador sem fio físico em mais de um adaptador sem fio virtual às vezes chamado de Wi-Fi Virtual.
-   Um AP (ponto de acesso sem fio) baseado em software às vezes chamado de SoftAP que usa um adaptador sem fio virtual designado.

Essas duas funções coexistem em um sistema Windows juntos. Habilitar ou desabilitar a Rede Hospedada sem fio habilita ou desabilita o Wi-Fi virtual e o SoftAP. Não é possível habilitar ou desabilitar essas duas funções separadamente no Windows.

Com esse recurso, um computador Windows pode usar um único adaptador sem fio físico para se conectar como um cliente a um ponto de acesso de hardware (AP), ao mesmo tempo que atua como uma AP de software, permitindo que outros dispositivos sem fio se conectem a ele. Esse recurso requer que um adaptador sem fio com capacidade de Rede Hospedada seja instalado no computador local. O driver para o adaptador sem fio deve implementar o modelo de driver de dispositivo LAN sem fio definido pela Microsoft para uso no Windows 7. Para receber o logotipo Windows 7, um driver sem fio deve implementar o recurso rede hospedada sem fio.

Há no máximo uma Rede Hospedada sem fio habilitada a qualquer momento no computador local e apenas um adaptador sem fio será usado pela Rede Hospedada sem fio. Se houver mais de um adaptador sem fio com capacidade de Rede Hospedada, Windows escolherá um adaptador para uso com a Rede Hospedada sem fio. Quando as APIs de Rede Hospedada são usadas, o adaptador sem fio com capacidade de Rede Hospedada é virtualizado para no máximo três adaptadores lógicos:

-   Um STA (adaptador de estação) para uso por aplicativos sem fio cliente ou ad hoc. O adaptador STA herda todas as configurações do adaptador sem fio físico original e exibe os mesmos comportamentos que o adaptador físico. Conceitualmente, é possível exibir o adaptador STA como idêntico ao adaptador físico após a virtualização. O adaptador STA está sempre no sistema, desde que o adaptador físico sem fio correspondente está presente.
-   Um adaptador AP para uso pela Rede Hospedada sem fio para hospedar o SoftAP. O adaptador AP está presente no sistema Windows somente depois que a Rede Hospedada sem fio é invocada pela primeira vez (quando a função [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)ou [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) é chamada pela primeira vez). Depois de criado, o adaptador AP permanecerá no sistema até que a Rede Hospedada sem fio seja desabilitada. Se a Rede Hospedada sem fio estiver habilitada em algum momento posterior, o adaptador ap será novamente no sistema.
-   Um VSTA (adaptador de estação virtual) para uso por fornecedores de hardware para estender a funcionalidade de Rede Hospedada sem fio Windows. O adaptador VSTA é opcional e só pode ser criado no sistema pelo serviço IHV correspondente. Ao contrário do adaptador AP, o adaptador VSTA existe no sistema Windows somente a partir do momento em que o serviço IHV inicializa o adaptador até o momento em que o serviço IHV libera o adaptador.

A Wi-Fi virtual mapeia os adaptadores lógicos para portas NDIS. A associação dos adaptadores STA, AP e VSTA a portas NDIS específicas é determinada por Windows. O adaptador STA está sempre vinculado à Porta 0. O adaptador AP é vinculado à próxima porta NDIS disponível quando a virtualização é iniciada e a associação permanece a mesma até que a virtualização termine quando a Rede Hospedada sem fio estiver desabilitada. O adaptador VSTA é vinculado à próxima porta NDIS disponível quando é inicializado pelo serviço IHV correspondente e a associação permanece a mesma até que seja liberada pelo serviço IHV.

É possível que o adaptador VSTA seja criado para uso por IHVs sem criar o adaptador SoftAP.

As seguintes combinações são válidas para um adaptador físico com virtualização:

-   Adaptador STA.
-   Adaptadores STA e AP.
-   Adaptadores STA e VSTA.
-   Adaptadores STA, AP e VSTA.

Exceto pelo caso do adaptador STA, todas as outras combinações só são válidas quando a Rede Hospedada sem fio está habilitada. Quanto ao caso de adaptador STA único, ele será o adaptador físico se a Rede Hospedada sem fio estiver desabilitada. Se a Rede Hospedada sem fio estiver habilitada, será o adaptador STA quando a Rede Hospedada sem fio nunca tiver sido invocada no sistema.

A ponte de Camada 2 é proibida entre o adaptador de AP e quaisquer outros adaptadores no sistema. A mesma restrição se aplica ao adaptador VSTA quando ele está presente no sistema.

O recurso rede hospedada sem fio Windows implementa um SoftAP. No entanto, esse SoftAP não foi projetado para substituir dispositivos AP sem fio baseados em hardware. Em particular, se a Rede Hospedada sem fio estiver em execução quando o computador entrar em espera (em espera), hibernar ou antes que o computador seja reiniciado, a Rede Hospedada sem fio será interrompida. A Rede Hospedada sem fio não será reiniciada automaticamente depois que o computador retomar da suspensão, hibernação ou reinicialização. Além disso, o SoftAP não fornece a resolução DNS. No caso em que um servidor DNS externo não é disponibilizado usando o Compartilhamento de Conexão com a Internet (consulte a discussão do ICS abaixo), a resolução de FQDN (nome de domínio totalmente qualificado) entre dois computadores ou dispositivos conectados com o SoftAP, incluindo o computador que hospeda o SoftAP, só funcionaria se ambas as entidades marcam o tipo de rede da rede SoftAP como PRIVATE (HOME ou WORK na pop-up de categoria de rede). Como o computador que hospeda o SoftAP sempre marca o tipo de rede SoftAP como PRIVATE, somente os computadores ou dispositivos conectados ao SoftAP precisam marcar o tipo de rede SoftAP como PRIVATE para que a resolução FQDN funcione.

SoftAP e rede ad hoc são mutuamente exclusivos no mesmo adaptador físico. Se o SoftAP estiver em execução no adaptador de AP e um usuário ou aplicativo iniciar a rede ad hoc no adaptador STA, o SoftAP será desligado. Se a rede ad hoc está em execução no adaptador STA, uma tentativa de iniciar o SoftAP no adaptador de AP falhará.

Para fornecer proteção para as comunicações sem fio entre o computador que hospeda o SoftAP e os dispositivos que se conectam ao SoftAP, a Rede Hospedada sem fio exige que todos os dispositivos conectados usem o conjunto de criptografias WPA2-PSK/AES. A chave compartilhada é um valor de 63 caracteres gerado pelo Windows quando a Rede Hospedada sem fio é invocada pela primeira vez (quando a função [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)ou [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) é chamada pela primeira vez). Um usuário ou aplicativo não pode alterar o valor dessa chave compartilhada, mas um aplicativo pode solicitar que o sistema operacional regenere uma nova chave chamando a [**função WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) ou um usuário pode solicitar que o sistema operacional regenere uma nova chave usando **comandos netsh wlan.** Essa chave compartilhada é chamada de chave primária ou do sistema para a Rede Hospedada sem fio e é persistente ao iniciar e parar a Rede Hospedada sem fio. Essa chave primária é chamada de "chave de segurança do sistema" nos **comandos netsh wlan.**

Para permitir a facilidade de uso, a Rede Hospedada sem fio também dá suporte ao conceito de uma chave de segurança de usuário ou secundária que seja mais amigável, mas que pode ser menos segura. Essa chave secundária é chamada de "chave de segurança do usuário" nos **comandos netsh wlan.** A chave secundária não é gerada por Windows. O usuário deve fornecer o valor dessa chave. Um usuário ou aplicativo pode definir ou alterar o valor da chave chamando a função [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) ou usando os **comandos netsh wlan.** A chave secundária pode ser definida como persistente ou temporária. Para uma chave temporária, se a Rede Hospedada sem fio já estiver em execução, a chave secundária será válida até que a Rede Hospedada sem fio pare. Para uma chave temporária, se a Rede Hospedada sem fio não estiver em execução, ela será válida apenas entre a próxima rede hospedada sem fio iniciar e parar.

Há exatamente uma chave primária e, no máximo, uma chave secundária para a Hetwork hospedada sem fio em qualquer computador. Qualquer dispositivo provisionado por meio Wi-Fi WPS (Configuração Protegida) receberá a chave primária. Outros dispositivos configurados manualmente podem usar qualquer chave. Sempre que uma chave for alterada, qualquer dispositivo com o valor de chave antigo não poderá se conectar à Rede Hospedada sem fio sem ser provisionado com a nova chave. No entanto, os dispositivos com a outra chave inalterada devem continuar a ser capazes de se conectar à Rede Hospedada sem fio.

Um aplicativo pode se registrar para notificações de Rede Hospedada sem fio, portanto, uma notificação WLAN será enviada para o retorno de chamada do aplicativo quando as propriedades mudarem na Rede Hospedada sem fio. Um aplicativo registra-se para notificações de Rede Hospedada sem fio chamando [**wlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) com o parâmetro *dwNotifSource* definido para incluir o \_ bit \_ HNWK de Origem de NOTIFICAÇÃO \_ WLAN.

Windows fornece duas maneiras para os administradores de IT gerenciarem o recurso rede hospedada sem fio. Para computadores que são membros de um domínio, os administradores podem usar a política de grupo para não permitir a Rede Hospedada sem fio. Usando **comandos netsh wlan,** um administrador pode habilitar ou desabilitar a Rede Hospedada sem fio localmente no computador.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Cenários com suporte para rede hospedada sem fio

A rede hospedada sem fio habilita dois cenários principais para Windows computadores:

• A capacidade de fornecer uma rede de área pessoal sem fio (PAN sem fio) para uso com vários outros dispositivos sem fio.

• Compartilhamento de conexão de rede para uso por outros computadores e dispositivos.

O PAN sem fio é o cenário principal habilitado pela Rede Hospedada sem fio por conta própria. Depois que a Rede Hospedada sem fio for iniciada em um computador, qualquer dispositivo com suporte a WPA2-PSK/AES sem fio poderá se conectar ao softAP como se estivesse se conectando a um AP de hardware regular. Os dispositivos conectados à Rede Hospedada sem fio formam um PAN sem fio, em que eles podem trocar informações com o computador Windows que hospeda o SoftAP, bem como entre si.

O compartilhamento de conexão de rede para uso por outros computadores e dispositivos requer o uso do ICS (Compartilhamento de Conexão com a Internet). Nesse cenário, a interface pública do ICS é a conexão compartilhada, enquanto a interface privada é o adaptador virtual que hospeda o SoftAP. A conexão compartilhada pode ser uma conexão Ethernet, LAN sem fio ou WAN sem fio. No caso de uma conexão LAN sem fio, a interface pública do ICS pode ser de outro adaptador de LAN sem fio ou do adaptador virtual de estação no mesmo adaptador sem fio físico que hospeda o SoftAP. O uso mais comum para o compartilhamento de rede é o compartilhamento de uma conexão com a Internet, em que a rede na interface pública do ICS tem acesso à Internet.

A Rede Hospedada sem fio interage com a WPS (Instalação Protegida) do Wi-Fi , outro novo recurso importante no Windows 7 e no Windows Server 2008 R2 com o Serviço lan sem fio instalado. A Rede Hospedada sem fio e o WPS suportam um cenário que provisiona um dispositivo com capacidade para WPS para uma AP de hardware não capaz de WPS. Nesse caso, o SoftAP hospedado no Windows é invocado em segundo plano para fazer push do perfil de AP de hardware para o dispositivo com capacidade para WPS.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Acesso de usuário e aplicativo à rede hospedada sem fio

Os usuários finais interagem com o recurso rede hospedada sem fio Windows aplicativos de terceiros ou **comandos netsh.** Atualmente, não há nenhuma interface do usuário nativa para configurar ou gerenciar a Rede Hospedada sem fio no Windows 7 ou no Windows Server 2008 R2 com o Serviço lan sem fio instalado.

Os aplicativos de terceiros e os **comandos netsh** se baseiam no uso das funções de Rede Hospedada sem fio pública. Esse conjunto de funções fornece um conjunto completo de recursos para gerenciar a Rede Hospedada sem fio no Windows 7 e no Windows Server 2008 R2 com o Serviço lan sem fio instalado.

Veja a seguir uma lista das funções de Rede Hospedada sem fio e as ações comuns de um ponto de vista do usuário final para a função que seria usada:



| Funções usadas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Description                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart), [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Inicie a Rede Hospedada sem fio.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop), [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Pare a Rede Hospedada sem fio.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey), [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Definir configurações de Rede Hospedada sem fio (altere o SSID, altere a chave secundária ou solicite que a chave primária seja regenerada).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus), [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey), [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Consulte as informações e as configurações de Rede Hospedada sem fio (status, SSID, chave secundária, chave primária ou uma lista dos dispositivos conectados no momento).<br/> |



 

Os **comandos netsh** destinam-se ao uso por usuários avançados ou administradores.

*Netsh.exe* tem muitos subcommands para LAN sem fio. Uma lista completa de opções para **netsh** e LAN sem fio está disponível no prompt de comando digitando o seguinte:

**netsh wlan /?**

A documentação sobre todos os comandos Netsh para LAN sem fio também está disponível online no Technet. Para obter mais informações, consulte [Comandos Netsh para WLAN (Rede de](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))Área Local Sem Fio).

A seguir estão alguns comandos **netsh** comumente usados com para LAN sem fio e a Rede Hospedada sem fio, embora haja suporte para outras combinações de comandos:



| Comando                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrição                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Inicie a Rede Hospedada sem fio.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Pare a Rede Hospedada sem fio.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ mode= \] allow \| disallow**<br/>                                                                                                                                                                                                                                                                      | Habilitar ou desabilitar a Rede Hospedada sem fio.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ ssid= \] &lt; ssid &gt; \[ key= \] &lt; passphrase &gt; \[ keyUsage= \] persistent \| temporary** <br/> | Definir as configurações de Rede Hospedada sem fio.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**netsh wlan refresh hostednetwork \[ data= \] key**<br/>                                                                                                                                                                                                                                                                                       | Atualize a chave de Rede Hospedada sem fio.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan show hostednetwork \[ \[ setting= \] security\]**<br/>                                                                                                                                                                                                                                                                     | Exibir informações de Rede Hospedada sem fio.<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**netsh wlan show settings**<br/>                                                                                                                                                                                                                                                                                                                                                       | Exibir configurações globais de LAN sem fio.<br/>           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando rede hospedada sem fio e compartilhamento de conexão com a Internet](using-hosted-network-and-internet-connection-sharing.md)
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

 

 
