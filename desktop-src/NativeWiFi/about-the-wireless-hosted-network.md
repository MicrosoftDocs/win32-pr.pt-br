---
description: Sobre a rede hospedada sem fio
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Sobre a rede hospedada sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15be48bb5ef10754b11a0b3d4bb7d8e31ace9752
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170041"
---
# <a name="about-the-wireless-hosted-network"></a>Sobre a rede hospedada sem fio

A rede hospedada sem fio é um novo recurso de WLAN com suporte no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado. Esse recurso implementa duas funções principais:

-   A virtualização de um adaptador sem fio físico em mais de um adaptador sem fio virtual, às vezes chamado de Wi-Fi virtual.
-   Um AP (ponto de acesso sem fio) baseado em software é, às vezes, chamado de SoftAP que usa um adaptador sem fio virtual designado.

Essas duas funções coexistem em um sistema Windows juntos. Habilitar ou desabilitar a rede hospedada sem fio habilita ou desabilita o Wi-Fi virtual e o SoftAP. Não é possível habilitar ou desabilitar essas duas funções separadamente no Windows.

Com esse recurso, um computador com Windows pode usar um único adaptador sem fio físico para se conectar como um cliente a um ponto de acesso de hardware (AP), ao mesmo tempo em que atua como um AP de software, permitindo que outros dispositivos com capacidade de conexão sem fio se conectem a ele. Esse recurso requer que um adaptador sem fio compatível com a rede hospedada esteja instalado no computador local. O driver para o adaptador sem fio deve implementar o modelo de driver de dispositivo de LAN sem fio definido pela Microsoft para uso no Windows 7. Para receber o logotipo do Windows 7, um driver sem fio deve implementar o recurso de rede hospedada sem fio.

Há no máximo uma rede hospedada sem fio habilitada a qualquer momento no computador local e apenas um adaptador sem fio será usado pela rede hospedada sem fio. Se houver mais de um adaptador sem fio compatível com a rede hospedada, o Windows escolherá um adaptador para uso com a rede hospedada sem fio. Quando as APIs de rede hospedadas são usadas, o adaptador sem fio compatível com a rede hospedada é virtualizado para no máximo 3 adaptadores lógicos:

-   Um adaptador de estação (STA) para uso por aplicativos sem fio cliente ou ad hoc. O adaptador STA herda todas as configurações do adaptador sem fio físico original e exibe os mesmos comportamentos que o adaptador físico. Conceitualmente, é possível exibir o adaptador STA como idêntico ao adaptador físico após a virtualização. O adaptador STA está sempre no sistema, contanto que o adaptador físico sem fio correspondente esteja presente.
-   Um adaptador AP para uso pela rede hospedada sem fio para hospedar SoftAP. O adaptador AP está presente no sistema Windows somente depois que a rede hospedada sem fio é invocada pela primeira vez (quando a função [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)ou [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) é chamada primeiro). Depois de criado, o adaptador AP permanecerá no sistema até que a rede hospedada sem fio esteja desabilitada. Se a rede hospedada sem fio estiver habilitada posteriormente, o adaptador AP será exibido novamente no sistema.
-   Um VSTA (adaptador de estação virtual) para uso por fornecedores de hardware para estender o recurso de rede hospedada sem fio no Windows. O adaptador do VSTA é opcional e só pode ser criado no sistema pelo serviço do IHV correspondente. Ao contrário do adaptador AP, o adaptador do VSTA existe no sistema Windows somente a partir do momento em que o serviço do IHV Inicializa o adaptador até o momento em que o serviço de IHV libera o adaptador.

O Wi-Fi virtual mapeia os adaptadores lógicos para portas NDIS. A Associação dos adaptadores STA, AP e VSTA a portas NDIS específicas é decidida pelo Windows. O adaptador STA sempre está associado à porta 0. O adaptador AP está associado à próxima porta NDIS disponível quando a virtualização é iniciada e a associação permanece a mesma até que a virtualização seja encerrada quando a rede hospedada sem fio estiver desabilitada. O adaptador do VSTA é associado à próxima porta NDIS disponível quando é inicializado pelo serviço IHV correspondente e a associação permanece a mesma até ser liberada pelo serviço IHV.

É possível que o adaptador do VSTA seja criado para uso por IHVs sem criar o adaptador SoftAP.

As seguintes combinações são válidas para um adaptador físico com virtualização:

-   Adaptador STA.
-   Adaptadores STA e PA.
-   Adaptadores STA e VSTA.
-   Adaptadores STA, AP e VSTA.

Exceto para o caso do adaptador STA, todas as outras combinações só são válidas quando a rede hospedada sem fio está habilitada. Para o caso do único adaptador STA, ele será o adaptador físico se a rede hospedada sem fio estiver desabilitada. Se a rede hospedada sem fio estiver habilitada, ela será o adaptador STA quando a rede hospedada sem fio nunca tiver sido invocada no sistema.

A ponte de camada 2 é proibida entre o adaptador AP e quaisquer outros adaptadores no sistema. A mesma restrição se aplica ao adaptador do VSTA quando ele está presente no sistema.

O recurso de rede hospedada sem fio no Windows implementa um SoftAP. No entanto, esse SoftAP não foi projetado para substituir dispositivos AP sem fio baseados em hardware. Em particular, se a rede hospedada sem fio estiver em execução quando o computador entrar em suspensão (em espera), hibernar ou antes da reinicialização do computador, a rede hospedada sem fio será interrompida. A rede hospedada sem fio não será reiniciada automaticamente depois que o computador for retomado do modo de suspensão, hibernação ou reinicialização. Além disso, o SoftAP não fornece a resolução DNS. No caso em que um servidor DNS externo não é disponibilizado usando o compartilhamento de conexão com a Internet (consulte a discussão do ICS abaixo), a resolução de FQDN (nome de domínio totalmente qualificado) entre dois computadores ou dispositivos conectados com o SoftAP, incluindo o computador que hospeda o SoftAP, funcionaria apenas se as duas entidades marcassem o tipo de rede da rede SoftAP como particular (casa ou trabalho no pop-up da categoria de rede). Como a máquina que hospeda o SoftAP sempre marca o tipo de rede SoftAP como particular, somente os computadores ou dispositivos conectados ao SoftAP precisam marcar o tipo de rede SoftAP como particular para que a resolução do FQDN funcione.

As redes SoftAP e ad hoc são mutuamente exclusivas no mesmo adaptador físico. Se SoftAP estiver em execução no adaptador AP e um usuário ou aplicativo iniciar a rede ad hoc no adaptador STA, o SoftAP será desligado. A rede ad hoc IIF está em execução no adaptador STA, uma tentativa de iniciar o SoftAP no adaptador AP falhará.

Para fornecer proteção para as comunicações sem fio entre o computador que hospeda o SoftAP e os dispositivos que se conectam ao SoftAP, a rede hospedada sem fio requer que todos os dispositivos conectados usem o pacote de codificação WPA2-PSK/AES. A chave compartilhada é um valor de 63 caracteres gerado pelo Windows quando a rede hospedada sem fio é invocada pela primeira vez (quando a função [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)ou [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) é chamada primeiro). Um usuário ou aplicativo não pode alterar o valor dessa chave compartilhada, mas um aplicativo pode solicitar que o sistema operacional gere novamente uma nova chave chamando a função [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) ou um usuário pode solicitar que o sistema operacional regenere uma nova chave usando comandos **netsh wlan** . Essa chave compartilhada é chamada de chave primária ou de sistema para a rede hospedada sem fio e é persistente no início e na interrupção da rede hospedada sem fio. Essa chave primária é chamada de "chave de segurança do sistema" em comandos **netsh wlan** .

Para facilitar o uso, a rede hospedada sem fio também dá suporte ao conceito de uma chave de segurança secundária ou de usuário mais amigável, mas pode ser menos segura. Essa chave secundária é chamada de "chave de segurança do usuário" em comandos **netsh wlan** . A chave secundária não é gerada pelo Windows. O usuário deve fornecer o valor para essa chave. Um usuário ou aplicativo pode definir ou alterar o valor da chave chamando a função [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) ou usando os comandos **netsh wlan** . A chave secundária pode ser definida para ser persistente ou temporária. Para uma chave temporária, se a rede hospedada sem fio já estiver em execução, a chave secundária será válida até que a rede hospedada sem fio seja interrompida. Para uma chave temporária, se a rede hospedada sem fio não estiver em execução, ela será válida somente entre a próxima rede hospedada sem fio iniciar e parar.

Há exatamente uma chave primária e, no máximo, uma chave secundária para o Hetwork hospedado sem fio em qualquer computador. Qualquer dispositivo provisionado por meio da configuração do Wi-Fi protected (WPS) receberá a chave primária. Outros dispositivos configurados manualmente podem usar qualquer chave. Sempre que uma chave for alterada, qualquer dispositivo com o valor de chave antigo não será capaz de se conectar à rede hospedada sem fio sem ser reprovisionado com a nova chave. No entanto, os dispositivos com a outra chave inalterada devem continuar a ser capazes de se conectar à rede hospedada sem fio.

Um aplicativo pode se registrar para notificações de rede hospedadas sem fio, portanto, uma notificação de WLAN será enviada ao retorno de chamada do aplicativo quando as propriedades forem alteradas na rede hospedada sem fio. Um aplicativo é registrado para notificações de rede hospedada sem fio chamando o [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) com o parâmetro *dwNotifSource* definido para incluir o \_ \_ bit HNWK da fonte de notificação de WLAN \_ .

O Windows fornece duas maneiras para os administradores de ti gerenciarem o recurso de rede hospedada sem fio. Para computadores que são membros de um domínio, os administradores podem usar a diretiva de grupo para não permitir a rede hospedada sem fio. Usando comandos **netsh wlan** , um administrador pode habilitar ou desabilitar a rede hospedada sem fio localmente no computador.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Cenários com suporte para rede hospedada sem fio

A rede hospedada sem fio permite dois cenários principais para computadores Windows:

• A capacidade de fornecer uma rede de área pessoal sem fio (PAN sem fio) para uso com vários outros dispositivos sem fio.

• Compartilhamento de conexão de rede para uso por outros computadores e dispositivos.

A PAN sem fio é o cenário principal habilitado pela rede hospedada sem fio por conta própria. Depois que a rede hospedada sem fio for iniciada em um computador, qualquer dispositivo compatível com sem fio que ofereça suporte a WPA2-PSK/AES poderá se conectar ao softAP como se ele estiver se conectando a um AP de hardware normal. Os dispositivos conectados à rede hospedada sem fio formam uma PAN sem fio, onde são capazes de trocar informações com o computador Windows que hospeda o SoftAP, bem como entre si.

O compartilhamento de conexão de rede para uso por outros computadores e dispositivos requer o uso do ICS (compartilhamento de conexão com a Internet). Nesse cenário, a interface pública do ICS é a conexão compartilhada enquanto a interface privada é o adaptador virtual que hospeda o SoftAP. A conexão compartilhada pode ser uma Ethernet, LAN sem fio ou conexão WAN sem fio. No caso de uma conexão de LAN sem fio, a interface pública do ICS pode ser de outro adaptador de LAN sem fio ou do adaptador virtual de estação no mesmo adaptador sem fio físico que hospeda o SoftAP. O uso mais comum para o compartilhamento de rede é o compartilhamento de uma conexão com a Internet, onde a rede na interface pública do ICS tem acesso à Internet.

A rede hospedada sem fio interage com o WPS (configuração protegida Wi-Fi), outro novo recurso importante no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado. A rede hospedada sem fio e a WPS dão suporte a um cenário que provisiona um dispositivo compatível com WPS para um AP de hardware não compatível com WPS. Nesse caso, o SoftAP hospedado no Windows é invocado em segundo plano para enviar por push o perfil de AP de hardware para o dispositivo compatível com WPS.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Acesso de usuário e aplicativo à rede hospedada sem fio

Os usuários finais interagem com o recurso de rede hospedada sem fio no Windows usando aplicativos de terceiros ou comandos **netsh** . Atualmente, não há nenhuma interface do usuário nativa para configurar ou gerenciar a rede hospedada sem fio no Windows 7 ou no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.

Os aplicativos de terceiros e os comandos **netsh** se baseiam no uso de funções de rede hospedadas sem fio públicas. Esse conjunto de funções fornece um conjunto completo de recursos para gerenciar a rede hospedada sem fio no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.

Veja a seguir uma lista das funções de rede hospedadas sem fio e as ações comuns de um ponto de vista do usuário final que a função que seria usada para:



| Funções usadas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart), [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Inicie a rede hospedada sem fio.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop), [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Pare a rede hospedada sem fio.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings), [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey), [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Definir configurações de rede hospedada sem fio (alterar o SSID, alterar a chave secundária ou solicitar que a chave primária seja regenerada).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus), [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey), [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Consulte as configurações e informações da rede hospedada sem fio (status, SSID, chave secundária, chave primária ou uma lista dos dispositivos conectados no momento).<br/> |



 

Os comandos **netsh** destinam-se ao uso por usuários avançados ou administradores.

*Netsh.exe* tem muitos subcomandos para LAN sem fio. Uma lista completa de opções para **netsh** e LAN sem fio está disponível no prompt de comando, digitando o seguinte:

**netsh wlan/?**

A documentação sobre todos os comandos netsh para LAN sem fio também está disponível online no TechNet. Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

A seguir estão alguns comandos **netsh** comumente usados com para LAN sem fio e rede hospedada sem fio, embora haja suporte para outras combinações de comandos:



| Comando                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrição                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan Start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Inicie a rede hospedada sem fio.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan Stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Pare a rede hospedada sem fio.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ mode = \] permitir \| não permitir**<br/>                                                                                                                                                                                                                                                                      | Habilite ou desabilite a rede hospedada sem fio.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ SSID = \] <ssid> \[ Key = \] <passphrase> \[ KeyUsage = \] \| temporário persistente** <br/> | Defina as configurações de rede hospedada sem fio.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**netsh wlan Refresh hostednetwork \[ Data = \] Key**<br/>                                                                                                                                                                                                                                                                                       | Atualize a chave de rede hospedada sem fio.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan show hostednetwork \[ \[ Setting = \] Security\]**<br/>                                                                                                                                                                                                                                                                     | Exibir informações de rede hospedada sem fio.<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**netsh wlan show Settings**<br/>                                                                                                                                                                                                                                                                                                                                                       | Exibir configurações globais de LAN sem fio.<br/>           |



 

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

 

 
