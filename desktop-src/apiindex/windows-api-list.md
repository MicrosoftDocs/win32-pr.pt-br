---
description: Uma lista do conteúdo de referência para a API do Windows.
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Índice de API do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cace235af1c729e450bdf99b276eca1bfc000
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105807288"
---
# <a name="windows-api-index"></a>Índice de API do Windows

A seguir está uma lista do conteúdo de referência para a API (interface de programação de aplicativo) do Windows para aplicativos de desktop e de servidor.

Usando a API do Windows, você pode desenvolver aplicativos que são executados com êxito em todas as versões do Windows, aproveitando os recursos e as funcionalidades exclusivos de cada versão. (Observe que isso era chamado anteriormente de API do Win32. O nome API do Windows reflete com mais precisão suas raízes no Windows de 16 bits e seu suporte no Windows de 64 bits.)

## <a name="user-interface"></a>Interface do usuário

A API da interface do usuário do Windows cria e usa o Windows para exibir a saída, solicitar a entrada do usuário e executar as outras tarefas que dão suporte à interação com o usuário. A maioria dos aplicativos cria pelo menos uma janela.

-   [Acessibilidade](../winauto/windows-accessibility-features-reference.md)
-   [Gerenciador de Janelas da Área de Trabalho (DWM)](../dwm/reference.md)
-   [Serviços de globalização](../intl/globalization-services.md)
-   [DPI alto](../hidpi/high-dpi-reference.md)
-   [MUI (Multilingual User interface)](../intl/multilingual-user-interface-reference.md)
-   [NLS (suporte ao idioma nacional)](../intl/national-language-support-reference.md)
-   [Elementos da interface do usuário](../devnotes/user-interface.md):

    -   [Botões](../controls/bumper-button-button-control-reference.md)
    -   [Interpolação](../menurc/caret-functions.md)
    -   [Caixas de combinação](../controls/bumper-combobox-combobox-control-reference.md)
    -   [Caixas de diálogo comuns](../dlgbox/common-dialog-box-reference.md)
    -   [Controles comuns](../controls/individual-control-info.md)
    -   [Cursores](../menurc/cursor-reference.md)
    -   [Caixas de diálogo](../dlgbox/dialog-box-reference.md)
    -   [Editar controles](../controls/bumper-edit-control-edit-control-reference.md)
    -   [Controles de cabeçalho](../controls/bumper-header-control-header-control-reference.md)
    -   [Ícones](../menurc/icon-reference.md)
    -   [Aceleradores de teclado](../menurc/keyboard-accelerator-reference.md)
    -   [Caixas de listagem](../controls/bumper-list-box-list-box-control-reference.md)
    -   [Controles de exibição de lista](../controls/bumper-list-view-list-view-control-reference.md)
    -   [Menus](../menurc/menu-reference.md)
    -   [Barras de progresso](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [Folhas de propriedades](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [Controles de edição avançados](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [Barras de rolagem](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [Controles estáticos](../controls/bumper-static-control-static-control-reference.md)
    -   [Cadeias de caracteres](../menurc/string-reference.md)
    -   [Barras de Ferramentas](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [Dicas de ferramentas](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [Trackbars](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [Controles de exibição de árvore](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [Gerenciador de animação do Windows](../uianimation/windows-animation-reference.md)
-   [Estrutura da faixa de dasgem do Windows](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a>Ambiente do Windows (Shell)

-   [Sistema de propriedades do Windows](../properties/property-system-reference.md)
-   [Shell do Windows](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))
-   [Windows Search](../search/-search-reference-entry-page.md)
-   [Consoles](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a>Entrada e mensagens do usuário

-   [Interação do usuário](../user-interaction.md)
    -   [Manipulação direta](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [Entrada à tinta](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [Configuração de comentários de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [Contexto de interação](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [Pilha de entrada do dispositivo ponteiro](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [Notificações e mensagens de entrada do ponteiro](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [Entrada do controlador radial](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [Estrutura de serviços de texto](../tsf/text-services-framework.md)
    -   [Teste de colisão de toque](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [Injeção de toque](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [Interação do usuário herdada](../legacy-user-interaction-features.md)
    -   [Entrada por toque](../wintouch/windows-touch-portal.md)
    -   [Entrada de teclado](../inputdev/keyboard-input.md)
    -   [Entrada do mouse](../inputdev/mouse-input.md)
    -   [Entrada bruta](../inputdev/raw-input.md)
-   [Windows e mensagens](../winmsg/windowing.md):

    -   [Mensagens e filas de mensagens](../winmsg/message-and-message-queue-reference.md)
    -   [Windows](../winmsg/window-reference.md)
    -   [Classes de janela](../winmsg/window-class-reference.md)
    -   [Procedimentos de janela](../winmsg/window-procedure-reference.md)
    -   [Temporizadores](../winmsg/timer-reference.md)
    -   [Propriedades da janela](../winmsg/window-property-reference.md)
    -   [Ganchos](../winmsg/hook-reference.md)

## <a name="data-access-and-storage"></a>Armazenamento e acesso a dados

-   [BITS (serviço de Transferência Inteligente em Segundo Plano)](../bits/bits-reference.md)
-   [Backup de dados](../backup/backup.md)
    -   [Backup](../backup/backup-reference.md)
    -   [Eliminação de Duplicação de Dados](/previous-versions/windows/desktop/dedup/data-deduplication-api-reference)
    -   [Cópias de Sombra de Volume](../vss/volume-shadow-copy-reference.md)
    -   [Backup do Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-api-interfaces)
-   [Troca de dados](../dataxchg/data-exchange.md):

    -   [Área de transferência](../dataxchg/clipboard-reference.md)
    -   [Troca dinâmica de dados (DDE)](../dataxchg/dynamic-data-exchange-reference.md)
    -   [Gerenciamento de troca dinâmica de dados (DDEML)](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [Gerenciamento de diretórios](../fileio/directory-management-reference.md)
-   [Gerenciamento de disco](../fileio/disk-management-reference.md)
-   [DFS (Sistema de Arquivos Distribuído)](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [Replicação DFS](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [Mecanismo de armazenamento extensível](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [Arquivos e e/s (sistema de arquivos local)](../fileio/file-management-reference.md)
-   [API da biblioteca de descoberta do iSCSI](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
-   [Arquivos Offline](/previous-versions/windows/desktop/offlinefiles/offline-files-reference)
-   [Empacotamento](/previous-versions/windows/desktop/opc/packaging-programming-reference)
-   [Compressão diferencial remota](/previous-versions/windows/desktop/rdc/remote-differential-compression-reference)
-   [NTFS transacional](../fileio/transactional-ntfs-reference.md)
-   [Gerenciamento de volume](../fileio/volume-management-reference.md)
-   [VHD (disco rígido virtual)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))
-   [Gerenciamento de Armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Windows Data Access Components](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))
    -   [Microsoft ODBC (Open Database Connectivity)](/sql/odbc/reference/syntax/odbc-reference)
    -   [Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))
    -   [Microsoft ADO (ActiveX Data Objects)](/sql/ado/reference/ado-programmer-s-reference)

## <a name="diagnostics"></a>Diagnósticos

A API de [diagnóstico](/previous-versions//bb648685(v=vs.85)) permite solucionar problemas de aplicativos ou do sistema e monitorar o desempenho.

-   [Reinicialização e recuperação de aplicativos](../recovery/application-recovery-and-restart-reference.md)
-   [Depuração](../debug/debugging-reference.md)
-   [Tratamento de erro](../debug/error-handling-reference.md)
-   [Log de eventos](../eventlog/event-logging-reference.md)
-   [Rastreamento de eventos](../etw/event-tracing-reference.md)
-   [Criação de perfil de contador de hardware (HCP)](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [NDF (estrutura de diagnóstico de rede)](../ndf/ndf-reference.md)
-   [Monitor de Rede](../netmon2/reference.md)
-   [Contadores de desempenho](../perfctrs/performance-counters-reference.md)
-   [Logs e Alertas de Desempenho (PLA)](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [Processar instantâneos](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [Status do processo (PSAPI)](../psapi/psapi-reference.md)
-   [Tratamento de exceções estruturado](../debug/structured-exception-handling-reference.md)
-   [Monitor do Sistema](../sysmon/system-monitor-reference.md)
-   [Passagem de cadeia de espera](../debug/wait-chain-traversal.md)
-   [Relatório de Erros do Windows (WER)](../wer/wer-reference.md)
-   [Log de eventos do Windows](../wes/windows-event-log-reference.md)
-   [Plataforma de solução de problemas do Windows](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a>Gráficos e multimídia

As APIs de [gráficos, multimídia](/previous-versions//aa969176(v=vs.85)) , [áudio e vídeo](../audio-and-video.md) permitem que os aplicativos incorporem texto formatado, gráficos, áudio e vídeo.

-   [Áudio principal](../coreaudio/programming-reference.md)
-   [Direct2D](../direct2d/reference.md)
-   [DirectComposition](../directcomp/reference.md)
-   [DirectShow](../directshow/directshow-reference.md)
-   [DirectWrite](../directwrite/reference.md)
-   [DirectX](../directx-sdk--august-2009-.md)
-   [Graphics Device Interface (GDI)](../gdi/windows-gdi.md)
-   [GDI+](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [Streaming de mídia](../mediastreaming/media-streaming-api-portal.md)
-   [Microsoft Media Foundation](../medfound/media-foundation-programming-reference.md)
-   [Tecnologias de TV da Microsoft](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [OpenGL](../opengl/opengl-reference.md)
-   [Configuração do monitor](../monitor/monitor-configuration-reference.md)
-   [Vários monitores de exibição](../gdi/multiple-display-monitors-reference.md)
-   [Aquisição de imagem](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Sistema de cores do Windows](../wcs/reference.md)
-   [Windows Imaging Component (WIC)](../wic/-wic-codec-reference.md)
-   [Codec de áudio e vídeo do Windows Media e DSP](/previous-versions//dd443208(v=vs.85))
-   [Windows Media Center](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Formato de mídia do Windows](../wmformat/programming-reference.md)
-   [Serviços de compartilhamento da biblioteca do Windows Media](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [Windows Media Player](../wmp/windows-media-player-object-model-reference.md)
-   [Serviços de mídia do Windows](/previous-versions/windows/desktop/dd893580(v=vs.85))
-   [Windows Movie Maker](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [Multimídia do Windows](../multimedia/multimedia-reference.md)

## <a name="devices"></a>Dispositivos

-   [AllJoyn](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [Recursos de comunicação](../devio/communications-reference.md)
-   [Acesso ao dispositivo](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [Gerenciamento de dispositivo](../devio/device-management-reference.md)
-   [Armazenamento Avançado](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [Descoberta de função](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [Mestre de imagem](../imapi/imapi-reference.md)
-   [Localidade](../locationapi/windows-location-programming-reference.md)
-   [Banco de dados de associação PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [Impressão](/windows-hardware/drivers/print/introduction-to-printing)
    -   [Spooler de impressão](../printdocs/printing-and-print-spooler-reference.md)
    -   [Imprimir pacote de documentos](../printdocs/tailored-app-printing-api.md)
    -   [Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [Tíquete de impressão](../printdocs/print-ticket-api.md)
    -   [Impressão XPS](../printdocs/xpsprint-api.md)
-   [Sensores](../sensorsapi/sensor-api-programming-reference.md)
-   [Serviço de notificação de eventos do sistema (SENS)](../sens/sens-reference.md)
-   [Ajuda da ferramenta](../toolhelp/tool-help-reference.md)
-   [UPnP](../upnp/universal-plug-and-play-start-page.md)
-   [Serviços Web em dispositivos](../wsdapi/web-services-for-devices-reference.md)
-   [WIA (Windows Image Acquisition)](../wia/-wia-reference.md)
-   [Gerenciador de Dispositivos de mídia do Windows](../wmdm/programming-reference.md)
-   [Dispositivos portáteis do Windows](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a>Serviços do sistema

As APIs de [Serviços do sistema](/previous-versions//aa969179(v=vs.85)) fornecem aos aplicativos acesso aos recursos do computador e aos recursos do sistema operacional subjacente, como memória, sistemas de arquivos, dispositivos, processos e threads.

-   [INTERFACES](../com/reference.md)
-   [COM+](../cossdk/com--reference.md)
-   [API de compactação](../cmpapi/-compression-portal.md)
-   [DTC (Coordenador de Transações Distribuídas)](/previous-versions/windows/desktop/ms686108(v=vs.85))
-   [Bibliotecas de vínculo dinâmico (DLLs)](../dlls/dynamic-link-library-functions.md)
-   [API de ajuda](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   [Comunicações entre processos](../ipc/interprocess-communications.md):
    -   [Processadores](../ipc/mailslot-functions.md)
    -   [Pipes](../ipc/pipe-functions.md)
-   [KTM (kernel Transaction Manager)](../ktm/ktm-reference.md)
-   [Gerenciamento de memória](../memory/memory-management-reference.md)
-   [Gravador de operação](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [Gerenciamento de Energia](../power/power-management-reference.md)
-   [Serviços de área de trabalho remota](../termserv/terminal-services-reference.md)
-   [Processos](../procthread/process-and-thread-reference.md)
-   [Serviços](../services/service-reference.md)
-   [Sincronização](../sync/synchronization-reference.md)
-   [Threads](../procthread/process-and-thread-reference.md)
-   [Compartilhamento de área de trabalho do Windows](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [Informações do sistema Windows](../sysinfo/windows-system-information.md)
    -   [Identificador e objetos](../sysinfo/handle-and-object-functions.md)
    -   [Registro](../sysinfo/registry-reference.md)
    -   [Hora](../sysinfo/time-reference.md)
    -   [Provedor de tempo](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a>Segurança e identidade

As APIs de [segurança e identidade](../devnotes/security.md) habilitam a autenticação de senha durante o logon, proteção condicional para todos os objetos do sistema compartilháveis, controle de acesso privilegiado, Rights Management e auditoria de segurança.

-   [Autenticação](../secauthn/authentication-reference.md)
-   [Autorização](../secauthz/authorization-reference.md)
-   [Registro de certificado](../seccertenroll/certificate-enrollment-api-reference.md)
-   [Criptografia](../seccrypto/cryptography-reference.md)
-   [CNG (criptografia próxima geração)](../seccng/cng-reference.md)
-   [Serviços de diretório](/previous-versions//ms682458(v=vs.85))
    -   [Active Directory Domain Services](../ad/active-directory-domain-services-reference.md)
    -   [ADSI (interfaces de serviço Active Directory)](../adsi/adsi-reference.md)
-   [Protocolo EAP (Extensible Authentication Protocol)](../eap/extensible-authentication-protocol-reference.md)
-   [Host de protocolo de autenticação extensível (EAPHost)](../eaphost/about-eap-host.md)
-   [Gerenciamento de senhas MS-CHAP](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [NAP (proteção de acesso à rede)](../nap/nap-reference.md)
-   [NPS (extensões do servidor de políticas de rede)](../nps/ias-internet-authentication-service-reference.md)
-   [Controles dos pais](../parcon/parental-controls-reference.md)
-   [Provedores WMI de segurança](../secprov/security-wmi-providers-reference.md)
-   [Serviços de base do TPM (TBS)](../tbs/tbs-reference.md)
-   [Windows Biometric Framework](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a>Instalação e manutenção de aplicativos

-   [Explorador de jogos](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))
-   [Assemblies lado a lado](../sbscs/side-by-side-assemblies-reference.md)
-   [APIs de empacotamento, implantação e consulta](../appxpkg/api-reference.md
)
-   [Licença de desenvolvedor](../devlic/developer-license-apis.md)
-   [Gerenciador de reinicialização](../rstmgr/restart-manager-reference.md)
-   [Windows Installer](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a>Administração e gerenciamento do sistema

As interfaces de [Administração do sistema](../srvnodes/system-administration.md) permitem instalar, configurar e fazer a manutenção de aplicativos ou sistemas.

-   [Provedor WMI de Dados de Configuração da Inicialização](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [Clusters de failover](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [Gerenciador de Recursos de Servidor de Arquivos (FSRM)](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [Política de Grupo](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [MMC (console de gerenciamento Microsoft) 2,0](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [NetShell](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [Infraestrutura de gerenciamento de configurações](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Log de Inventário de Software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [Licenciamento de software](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md)
-   [Infraestrutura de gerenciamento de configurações](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Restauração do Sistema](../sr/system-restore-portal.md)
-   [Desligamento do sistema](../shutdown/system-shutdown.md)
-   [Agendador de Tarefas](../taskschd/task-scheduler-start-page.md)
-   [Log de acesso do usuário](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [Windows Virtual PC](../vpc/virtual-pc-reference.md)
-   [Servidor virtual da Microsoft](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [Provedor de balanceamento de carga de rede](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [WMI do Windows Defender v2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [Windows Deployment Services](../wds/windows-deployment-services-portal.md)
-   [Vantagem do Windows Genuine](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [Infraestrutura de gerenciamento do Windows](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [WMI (Instrumentação de Gerenciamento do Windows)](../wmisdk/wmi-reference.md)
-   [Gerenciamento Remoto do Windows](../winrm/portal.md)
-   [Proteção de Recursos do Windows](../wfp/windows-resource-protection-portal.md)
-   [Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))
-   [Ferramenta de avaliação do sistema do Windows](../winsat/winsat-reference.md)
-   [Windows Update Agent](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a>Rede e Internet

As APIs de [rede](../devnotes/networking.md) permitem a comunicação entre aplicativos em uma rede. Você também pode criar e gerenciar o acesso a recursos compartilhados, como diretórios e impressoras de rede.

-   [Sistema de nome de domínio (DNS)](../dns/dns-reference.md)
-   [Protocolo DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
-   [Serviço de fax](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [Assistente para Conexão](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [Servidor HTTP](../http/http-server-api-reference.md)
-   [Firewall e compartilhamento de conexão com a Internet](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [Auxiliar de IP](../iphlp/ip-helper-function-reference.md)
-   [Firewall de conexão com a Internet IPv6](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [Base de informações de gerenciamento](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   [Serviço de enfileiramento de mensagens (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))
-   [Protocolo de alocação de cliente dinâmico (MADCAP) de endereço multicast](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [NAT (conversão de endereços de rede)](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [NLM (Gerenciador de lista de rede)](../nla/network-list-manager-api-reference.md)
-   [Gerenciamento de rede](../netmgmt/network-management-reference.md)
-   [Gerenciamento de compartilhamento de rede](../netshare/network-share-management-reference.md)
-   [Ponto a ponto](../p2psdk/portal.md)
-   [QOS (qualidade de serviço)](/previous-versions/windows/desktop/qos/qos-reference)
-   [Chamada de Procedimento Remoto](../rpc/reference.md)
-   [Serviço de roteamento e acesso remoto (RAS)](../rras/portal.md)
-   [Protocolo SNMP](../snmp/snmp-reference.md)
-   [Gerenciamento de SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [TAPI (interfaces de programação de aplicativo) de telefonia](../tapi/telephony-application-programming-interfaces.md)
-   [WebDAV](../webdav/webdav-api-reference.md)
-   [Componente de protocolo WebSocket](../websock/web-socket-protocol-component-api-portal.md)
-   Rede sem fio:
    -   [Bluetooth](../bluetooth/bluetooth-reference.md)
    -   [IrDA](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [Banda larga móvel](../mbn/mobile-broadband-networks-api-reference.md)
    -   [WiFi nativo](../nativewifi/native-wifi-reference.md)
    -   [Windows Connect agora](../wcn/windows-connect-now-reference.md)
    -   [Gerenciador de Conexão do Windows](../wcm/windows-connection-manager-reference.md)
-   [Plataforma de filtragem do Windows](../fwp/fwp-reference.md)
-   [Firewall do Windows com Advanced Security](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [WinHTTP (serviços HTTP do Windows)](../winhttp/winhttp-reference.md)
-   [Internet do Windows (WinINet)](../wininet/wininet-reference.md)
-   [Sistema de rede do Windows (WNet)](../wnet/windows-networking-reference.md)
-   [Virtualização de rede do Windows](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   [Plataforma Windows RSS](/previous-versions/windows/desktop/ms684702(v=vs.85))
-   [Windows Sockets (Winsock)](../winsock/winsock-reference.md)
-   [Serviços Web do Windows](../wsw/windows-web-services-reference.md)
-   [Solicitação estendida HTTP XML](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a>APIs preteridas ou herdadas

Veja a seguir as tecnologias e as APIs que estão desatualizadas ou foram substituídas ou preteridas dos sistemas operacionais cliente e servidor do Windows.

-   [DirectMusic](/previous-versions/ms807133(v=msdn.10))
-   [DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))
-   O Microsoft [UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10)) agora está incluído com [o Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).
-   [Troca dinâmica de dados de rede (DDE)](../ipc/network-dde-reference.md)
-   [Serviço de instalação remota](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)): em vez disso, use os [serviços de implantação do Windows](../wds/windows-deployment-services-portal.md) .
-   [VDS (serviço de disco virtual)](../vds/vds-reference.md): Use o [Gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) .
-   Serviços de terminal: use [serviços de área de trabalho remota](../termserv/terminal-services-reference.md).
-   [Gerenciador de direitos do Windows Media](/previous-versions//bb614742(v=vs.85))
-   [Sistema de mensagens do Windows (MAPI)](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi): use [MAPI do Office](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) em vez disso.
-   [Plataforma de gadget do Windows](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal): Crie aplicativos UWP em vez disso.
-   [Barra lateral do Windows](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry): Crie aplicativos UWP em vez disso.
-   [Windows SideShow](/previous-versions//ms744179(v=vs.85)): sem substituição.
-   [Efeitos de bitmap do WPF](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
