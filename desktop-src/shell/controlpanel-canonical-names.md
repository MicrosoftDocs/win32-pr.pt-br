---
description: A partir do Windows Vista, os itens do painel de controle incluídos no Windows recebem um nome canônico que pode ser usado em uma chamada à API ou em uma instrução de linha de comando para iniciar esse item programaticamente.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Nomes canônicos de itens do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920754"
---
# <a name="canonical-names-of-control-panel-items"></a>Nomes canônicos de itens do painel de controle

A partir do Windows Vista, os itens do painel de controle incluídos no Windows recebem um nome canônico que pode ser usado em uma [chamada à API ou em uma instrução de linha de comando](executing-control-panel-items.md) para iniciar esse item programaticamente. A partir do Windows 7 e do Windows Server 2008 R2, os nomes canônicos podem ser usados em uma política de grupo para ocultar itens específicos do painel de controle. Este tópico fornece detalhes para cada item do painel de controle: nome canônico, GUID, nome do módulo e versões do sistema operacional que reconhecem o nome canônico.

> [!Note]  
> Os nomes canônicos dos itens do painel de controle não têm suporte antes do Windows Vista.

 

-   [Nomes canônicos do painel de controle](#control-panel-canonical-names)
-   [Nomes canônicos do painel de controle preteridos](#deprecated-control-panel-canonical-names)
-   [Usando nomes canônicos no Política de Grupo](#using-canonical-names-in-local-group-policy)
-   [Comentários](#remarks)

## <a name="control-panel-canonical-names"></a>Nomes canônicos do painel de controle

Pontos a serem lembrados ao trabalhar com esses valores:

-   Por definição, os nomes canônicos não são alterados com base no idioma do sistema; Eles estão sempre em inglês, mesmo se o idioma do sistema não for.
-   Nem todos os itens do painel de controle estão presentes em todas as variedades do Windows.
-   Alguns itens do painel de controle só aparecerão se o hardware correto for detectado no sistema.
-   Terceiros também podem adicionar itens do painel de controle. Os nomes canônicos listados aqui são apenas para itens do painel de controle que estão incluídos no Windows.

A seguir estão os itens do painel de controle disponíveis no Windows 8.1:

-   [Central de ações](#action-center)
-   [Ferramentas administrativas](#administrative-tools)
-   [AutoPlay](#autoplay)
-   [Dispositivos biométricos](#biometric-devices)
-   [Criptografia de Unidade de Disco BitLocker](#bitlocker-drive-encryption)
-   [Gerenciamento de cores](#color-management)
-   [Gerenciador de Credenciais](#credential-manager)
-   [Data e hora](#date-and-time)
-   [Programas padrão](#default-programs)
-   [Gerenciador de Dispositivos](#device-manager)
-   [Dispositivos e impressoras](#devices-and-printers)
-   [Exibição](#display)
-   [Central de facilidade de acesso](#ease-of-access-center)
-   [Segurança da família](#family-safety)
-   [Histórico de arquivos](#file-history)
-   [Opções de Pasta](#folder-options)
-   [Fontes](#fonts)
-   [HomeGroup](#homegroup)
-   [Opções de indexação](#indexing-options)
-   [Infravermelho](#infrared)
-   [Opções da Internet](#internet-options)
-   [Iniciador iSCSI](#iscsi-initiator)
-   [iSNS Server](#isns-server)
-   [Teclado](#keyboard)
-   [Configurações de local](#location-settings)
-   [Mouse](#mouse)
-   [MPIOConfiguration](#mpioconfiguration)
-   [Centro de compartilhamento e de rede](#network-and-sharing-center)
-   [Ícones da área de notificação](#notification-area-icons)
-   [Caneta e toque](#pen-and-touch)
-   [Personalização](#personalization)
-   [Telefone e modem](#phone-and-modem)
-   [Opções de Energia](#power-options)
-   [Programas e Recursos](#programs-and-features)
-   [Recuperação](#recovery)
-   [Região](#region)
-   [Conexões de RemoteApp e Área de Trabalho](#remoteapp-and-desktop-connections)
-   [Som](#sound)
-   [Reconhecimento de fala](#speech-recognition)
-   [Espaços de armazenamento](#storage-spaces)
-   [Central de Sincronização](#sync-center)
-   [System](#system)
-   [Configurações do Tablet PC](#tablet-pc-settings)
-   [Barra de tarefas e navegação](#taskbar-and-navigation)
-   [Solução de problemas](#troubleshooting)
-   [TSAppInstall](#tsappinstall)
-   [Contas de Usuário](#user-accounts)
-   [Windows Anytime Upgrade](#windows-anytime-upgrade)
-   [Windows Defender](#windows-defender)
-   [Firewall do Windows](#windows-firewall)
-   [Centro de Mobilidade do Windows](#windows-mobility-center)
-   [Windows To Go](#windows-to-go)
-   [Windows Update](#windows-update)
-   [Pastas de trabalho](#work-folders)

### <a name="action-center"></a>Central de Ações

-   **Nome canônico**: Microsoft. ActionCenter
-   **GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\ActionCenterCPL.dll,-1
-   **Páginas**

    | Nome da Página           | Abre                      |
    |---------------------|----------------------------|
    | MaintenanceSettings | Manutenção automática      |
    | pageProblems        | Relatórios de problemas            |
    | pageReliabilityView | Monitor de confiabilidade        |
    | pageResponseArchive | Mensagens arquivadas          |
    | pageSettings        | Configurações de relatório de problemas |

    

     

### <a name="administrative-tools"></a>Ferramentas Administrativas

-   **Nome canônico**: Microsoft. AdministrativeTools
-   **GUID**: {D20EA4E1-3957-11D2-A40B-0C5020524153}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\shell32.dll,-22982

### <a name="autoplay"></a>Reprodução Automática

-   **Nome canônico**: Microsoft. AutoPlay
-   **GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\autoplay.dll,-1

### <a name="biometric-devices"></a>Dispositivos biométricos

-   **Nome canônico**: Microsoft. BiometricDevices
-   **GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\biocpl.dll,-1

### <a name="bitlocker-drive-encryption"></a>Criptografia de Unidade de Disco BitLocker

-   **Nome canônico**: Microsoft. BitLockerDriveEncryption
-   **GUID**: {D9EF8727-CAC2-4E60-809E-86F80A666C91}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\fvecpl.dll,-1

### <a name="color-management"></a>Gerenciamento de cores

-   **Nome canônico**: Microsoft. ColorManagement
-   **GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\colorcpl.exe,-6

### <a name="credential-manager"></a>Gerenciador de Credenciais

-   **Nome canônico**: Microsoft. CredentialManager
-   **GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\Vault.dll,-1
-   **Páginas**

    | Nome da Página                   | Abre               |
    |-----------------------------|---------------------|
    | ? SelectedVault = CredmanVault | as Credenciais do Windows |

    

     

### <a name="date-and-time"></a>Data e hora

-   **Nome canônico**: Microsoft. DateAndTime
-   **GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\timedate.cpl,-51
-   **Páginas**

    | Nome da Página | Abre             |
    |-----------|-------------------|
    | 1         | Relógios adicionais |

    

     

### <a name="default-programs"></a>Programas padrão

-   **Nome canônico**: Microsoft. defaultprograms
-   **GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\sud.dll,-1
-   **Páginas**

    | Nome da Página          | Abre                |
    |--------------------|----------------------|
    | pageDefaultProgram | Definir programas padrão |
    | pageFileAssoc      | Definir associações     |

    

     

### <a name="device-manager"></a>Gerenciador de Dispositivos

-   **Nome canônico**: Microsoft. DeviceManager
-   **GUID**: {74246bfc-4c96-11D0-ABEF-0020af6b0b7a}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\devmgr.dll,-4

### <a name="devices-and-printers"></a>Dispositivos e Impressoras

-   **Nome canônico**: Microsoft. DevicesAndPrinters
-   **GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\DeviceCenter.dll,-1000

### <a name="display"></a>Monitor

-   **Nome canônico**: Microsoft. display
-   **GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\Display.dll,-1
-   **Páginas**

    | Nome da Página | Abre             |
    |-----------|-------------------|
    | Configurações  | Resolução de tela |

    

     

### <a name="ease-of-access-center"></a>Central de facilidade de acesso

-   **Nome canônico**: Microsoft. EaseOfAccessCenter
-   **GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\accessibilitycpl.dll,-10
-   **Páginas**

    | Nome da Página               | Abre                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | pageEasierToClick       | Facilitar o uso do mouse                                        |
    | pageEasierToSee         | Facilitar a visualização do computador                                     |
    | pageEasierWithSounds    | Usar alternativas de texto ou visuais para sons                          |
    | pageFilterKeysSettings  | Configurar chaves de filtro                                                  |
    | pageKeyboardEasierToUse | Facilitar o uso do teclado                                     |
    | pageNoMouseOrKeyboard   | Usar o computador sem mouse ou teclado                        |
    | pageNoVisual            | Usar o computador sem uma exibição                                  |
    | pageQuestionsCognitive  | Obtenha recomendações para facilitar o uso do seu computador (cognitiva) |
    | pageQuestionsEyesight   | Obtenha recomendações para facilitar o uso do seu computador (eyesight)  |

    

     

### <a name="family-safety"></a>Segurança da família

-   **Nome canônico**: Microsoft. ParentalControls
-   **GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\wpccpl.dll,-100
-   **Páginas**

    | Nome da Página   | Abre                                  |
    |-------------|----------------------------------------|
    | pageUserHub | Escolher um usuário e configurar a proteção da família |

    

     

### <a name="file-history"></a>Histórico de arquivos

-   **Nome canônico**: Microsoft. filehistory
-   **GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}
-   **Sistema operacional com suporte**: Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\fhcpl.dll,-52
-   O histórico de arquivos inclui uma versão mais recente do item de backup e restauração, mas o nome canônico do item antigo não é remapeado para o histórico de arquivos.

### <a name="folder-options"></a>Opções de Pasta

-   **Nome canônico**: Microsoft. FOLDEROPTIONS
-   **GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\shell32.dll,-22985

### <a name="fonts"></a>Fontes

-   **Nome canônico**: Microsoft. Fonts
-   **GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\FontExt.dll,-8007

### <a name="homegroup"></a>HomeGroup

-   **Nome canônico**: Microsoft. grupo doméstico
-   **GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\hgcpl.dll,-1

### <a name="indexing-options"></a>Opções de Indexação

-   **Nome canônico**: Microsoft. IndexingOptions
-   **GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\srchadmin.dll,-601

### <a name="infrared"></a>Infravermelho

-   **Nome canônico**: Microsoft. infravermelho
-   **GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\irprops.cpl,-1

### <a name="internet-options"></a>Opções da Internet

-   **Nome canônico**: Microsoft. InternetOptions
-   **GUID**: {A3DD4F92-658A-410f-84FD-6FBBBEF2FFFE}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @C: \\ Windows \\ System32 \\inetcpl.cpl,-4312
-   **Páginas**

    | Nome da Página | Abre       |
    |-----------|-------------|
    | 1         | Segurança    |
    | 2         | Privacidade     |
    | 3         | Conteúdo     |
    | 4         | conexões |
    | 5         | Programas    |
    | 6         | Avançado    |

    

     

### <a name="iscsi-initiator"></a>Iniciador iSCSI

-   **Nome canônico**: Microsoft. iSCSIInitiator
-   **GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\iscsicpl.dll,-5001

### <a name="isns-server"></a>iSNS Server

-   **Nome canônico**: Microsoft. iSNSServer
-   **GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\isnssrv.dll,-5005
-   Este item do painel de controle será visto apenas nas versões de servidor do Windows.

### <a name="keyboard"></a>Keyboard

-   **Nome canônico**: Microsoft. Keyboard
-   **GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\main.cpl,-102

### <a name="location-settings"></a>Configurações de local

-   **Nome canônico**: Microsoft. LocationSettings
-   **GUID**: {E9950154-C418-419E-A90A-20C5287AE24B}
-   **Sistema operacional com suporte**: Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\SensorsCpl.dll,-1

### <a name="mouse"></a>Mouse

-   **Nome canônico**: Microsoft. mouse
-   **GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\main.cpl,-100
-   **Páginas**

    | Nome da Página | Abre           |
    |-----------|-----------------|
    | 1         | Ponteiros        |
    | 2         | Opções de ponteiro |
    | 3         | Wheel           |
    | 4         | Hardware        |

    

     

### <a name="mpioconfiguration"></a>MPIOConfiguration

-   **Nome canônico**: Microsoft. MPIOConfiguration
-   **GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\mpiocpl.dll,-1000
-   Este item do painel de controle será visto apenas nas versões de servidor do Windows.

### <a name="network-and-sharing-center"></a>Centro de compartilhamento e de rede

-   **Nome canônico**: Microsoft. NetworkAndSharingCenter
-   **GUID**: {8E908FC9-BECC-40F6-915B-F4CA0E70D03D}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\netcenter.dll,-1
-   **Páginas**

    | Nome da Página  | Abre                     |
    |------------|---------------------------|
    | Avançado   | Configurações de compartilhamento avançadas |
    | ShareMedia | Opções de streaming de mídia   |

    

     

### <a name="notification-area-icons"></a>Ícones da área de notificação

-   **Nome canônico**: Microsoft. NotificationAreaIcons
-   **GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\taskbarcpl.dll,-1

### <a name="pen-and-touch"></a>Caneta e toque

-   **Nome canônico**: Microsoft. PenAndTouch
-   **GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\tabletpc.cpl,-10103
-   **Páginas**

    | Nome da Página | Abre       |
    |-----------|-------------|
    | 1         | Movimentos      |
    | 2         | Handwriting |

    

     

### <a name="personalization"></a>Personalização

-   **Nome canônico**: Microsoft. Personalization
-   **GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\themecpl.dll,-1
-   **Páginas**

    | Nome da Página        | Abre                |
    |------------------|----------------------|
    | pageColorization | Cor e aparência |
    | pageWallpaper    | Segundo plano da área de trabalho   |

    

     

### <a name="phone-and-modem"></a>Telefone e modem

-   **Nome canônico**: Microsoft. PhoneAndModem
-   **GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\telephon.cpl,-1
-   A janela que esse valor inicia é intitulada "informações de local" em versões do Windows anteriores ao Windows 8. A interface do usuário do item é consideravelmente alterada a partir do Windows 8.

### <a name="power-options"></a>Opções de Energia

-   **Nome canônico**: Microsoft. poweroptions
-   **GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\powercpl.dll,-1
-   **Páginas**

    | Nome da Página          | Abre              |
    |--------------------|--------------------|
    | pageGlobalSettings | Configurações do sistema    |
    | pagePlanSettings   | Editar configurações do plano |

    

     

### <a name="programs-and-features"></a>Programas e Recursos

-   **Nome canônico**: Microsoft. ProgramsAndFeatures
-   **GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\appwiz.cpl,-159
-   **Páginas**

    | Nome da Página                                | Abre             |
    |------------------------------------------|-------------------|
    | ::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD} | Atualizações instaladas |

    

     

### <a name="recovery"></a>Recuperação

-   **Nome canônico**: Microsoft. Recovery
-   **GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\recovery.dll,-101

### <a name="region"></a>Região

-   **Nome canônico**: Microsoft. RegionAndLanguage
-   **GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\intl.cpl,-1
-   A região e o item de idioma encontrados no Windows 7 foram divididos a partir do Windows 8. O Microsoft. RegionAndLanguage agora inicia o item de região. Para iniciar o item de idioma, use [Microsoft. Language](#location-settings).
-   **Páginas**

    | Nome da Página | Abre          |
    |-----------|----------------|
    | 1         | Localização       |
    | 2         | Administrativa |

    

     

### <a name="remoteapp-and-desktop-connections"></a>Conexões de RemoteApp e Área de Trabalho

-   **Nome canônico**: Microsoft. RemoteAppAndDesktopConnections
-   **GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\tsworkspace.dll,-15300

### <a name="sound"></a>Som

-   **Nome canônico**: Microsoft. Sound
-   **GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\mmsys.cpl,-300

### <a name="speech-recognition"></a>Reconhecimento de fala

-   **Nome canônico**: Microsoft. SpeechRecognition
-   **GUID**: {58E3C745-D971-4081-9034-86E34B30836A}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\ Speech \\ SpeechUX \\speechuxcpl.dll,-1

### <a name="storage-spaces"></a>Espaços de Armazenamento

-   **Nome canônico**: Microsoft. StorageSpaces
-   **GUID**: {F942C606-0914-47AB-BE56-1321B8035096}
-   **Sistema operacional com suporte**: Windows 8, Windows 8.1
-   **Nome do módulo**: @C: \\ Windows \\ System32 \\SpaceControl.dll,-1

### <a name="sync-center"></a>Central de Sincronização

-   **Nome canônico**: Microsoft. SyncCenter
-   **GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\SyncCenter.dll,-3000

### <a name="system"></a>Sistema

-   **Nome canônico**: Microsoft.System
-   **GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\systemcpl.dll,-1

### <a name="tablet-pc-settings"></a>Configurações do Tablet PC

-   **Nome canônico**: Microsoft. TabletPCSettings
-   **GUID**: {80F3F1D5-Feca-45F3-BC32-752C152E456E}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\tabletpc.cpl,-10100

### <a name="taskbar-and-navigation"></a>Barra de tarefas e navegação

-   **Nome canônico**: Microsoft. Taskbar
-   **GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}
-   **Sistema operacional com suporte**: Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\shell32.dll,-32517

### <a name="troubleshooting"></a>Solução de problemas

-   **Nome canônico**: Microsoft. Troubleshooting
-   **GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\DiagCpl.dll,-1
-   **Páginas**

    | Nome da Página   | Abre   |
    |-------------|---------|
    | HistoryPage | Histórico |

    

     

### <a name="tsappinstall"></a>TSAppInstall

-   **Nome canônico**: Microsoft. TSAppInstall
-   **GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}
-   **Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\tsappinstall.exe,-2001

### <a name="user-accounts"></a>Contas de usuário

-   **Nome canônico**: Microsoft. Accounts
-   **GUID**: {60632754-C523-4b62-b45c-4172da012619}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\usercpl.dll,-1

### <a name="windows-anytime-upgrade"></a>Windows Anytime Upgrade

-   **Nome canônico**: Microsoft. WindowsAnytimeUpgrade
-   **GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @ $ (resourcestring. \_ \_Caminho sys mod \_ ),-1

### <a name="windows-defender"></a>Windows Defender

-   **Nome canônico**: Microsoft. WindowsDefender
-   **GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% ProgramFiles% \\ Windows Defender \\MsMpRes.dll,-104

### <a name="windows-firewall"></a>Firewall do Windows

-   **Nome canônico**: Microsoft. WindowsFirewall
-   **GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @C: \\ Windows \\ System32 \\FirewallControlPanel.dll,-12122
-   **Páginas**

    | Nome da Página         | Abre        |
    |-------------------|--------------|
    | pageConfigureApps | Aplicativos permitidos |

    

     

### <a name="windows-mobility-center"></a>Centro de Mobilidade do Windows

-   **Nome canônico**: Microsoft. MobilityCenter
-   **GUID**: {5ea4f148-308C-46d7-98a9-49041b1dd468}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\mblctr.exe,-1002

### <a name="windows-to-go"></a>Windows To Go

-   **Nome canônico**: Microsoft. PortableWorkspaceCreator
-   **GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}
-   **Sistema operacional com suporte**: Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\pwcreator.exe,-151

### <a name="windows-update"></a>Windows Update

-   **Nome canônico**: Microsoft. windowsupdate
-   **GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}
-   **Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nome do módulo**: @% SystemRoot% \\ System32 \\wucltux.dll,-1
-   **Páginas**

    | Nome da Página         | Abre               |
    |-------------------|---------------------|
    | pageSettings      | Alterar configurações     |
    | pageUpdateHistory | Exibir histórico de atualizações |

    

     

### <a name="work-folders"></a>Pastas de trabalho

-   **Nome canônico**: Microsoft. WorkFolders
-   **GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}
-   **Sistema operacional com suporte**: Windows 8.1
-   **Nome do módulo**: @C: \\ Windows \\ System32 \\WorkfoldersControl.dll,-1

## <a name="deprecated-control-panel-canonical-names"></a>Nomes canônicos do painel de controle preteridos

Veja a seguir os nomes canônicos que não estão mais em uso a partir de Windows 8.1 ou posterior. Alguns foram completamente removidos. Outros foram remapeados nessas situações:

-   Um item do painel de controle é renomeado. O item renomeado recebe um novo nome canônico, mas mantém o mesmo GUID. Nesse caso, o antigo nome canônico inicia o item do painel de controle renomeado. Lembre-se de que o item que é iniciado pode não usar a mesma interface do usuário que a versão mais antiga do item.
-   A funcionalidade de um ou mais itens do painel de controle é movida ou consolidada em um novo item. Nesse caso, o nome canônico antigo é mapeado para o novo item mais apropriado do painel de controle.

> [!Note]  
> Existem remapeamentos para compatibilidade com versões anteriores. Você não deve usar valores preteridos no novo código.

 



| Nome canônico preterido                                   | Item do painel de controle                | GUID                                   | Observações                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft. addduro                                       | Adicionar hardware                      | {7A979262-40CE-46ff-AEEE-7884AC3B6136} | Mapeia para [Microsoft. DevicesAndPrinters](#devices-and-printers) a partir do Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft. AudioDevicesAndSoundThemes                        | Som                             | {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D} | Mapeia para [Microsoft. Sound](#sound) a partir do Windows 7.                                                                                                                                                                                                                                                                                                        |
| Microsoft. BackupAndRestoreCenter/Microsoft. BackupAndRestore | Centro de backup e restauração         | {B98A2BEA-7D42-4558-8BD1-832F41BAC6FD} | O Microsoft. BackupAndRestoreCenter é mapeado para Microsoft. BackupAndRestore no Windows 7. Ambos são removidos a partir do Windows 8; em vez disso, use [o Microsoft. filehistory](#file-history) .                                                                                                                                                                                   |
| Microsoft. CardSpace                                         | Windows CardSpace                 | {78CB147A-98EA-4AA6-B0DF-C8681F69341C} | Removido do Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. DesktopGadgets                                    | Gadgets de área de trabalho                   | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Removido do Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. GetProgramsOnline                                 | Windows Marketplace               | {3e7efb4c-faf1-453d-89eb-56026875ef90} | Removido do Windows 7.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. Infravermelhooptions                                   | Infravermelho                          | {A0275511-0E86-4ECA-97C2-ECD8F1221D08} | Mapeia para [Microsoft. infravermelho](#infrared) a partir do Windows 7.                                                                                                                                                                                                                                                                                                  |
| Microsoft. Language                                          | Idioma                          | {BF782CC9-5A52-4A17-806C-2A894FFEEAC5} | Removido a partir do Windows 10, versão 1803                                                                                                                                                                                                                                                                                                                    |
| Microsoft. LocationAndOtherSensors                           | Local e outros sensores        | {E9950154-C418-419e-A90A-20C5287AE24B} | Mapeia para [Microsoft. LocationSettings](#infrared) a partir do Windows 8.                                                                                                                                                                                                                                                                                          |
| Microsoft. PenAndInputDevices                                | Caneta e dispositivos de entrada             | {F82DF8F7-8B9F-442E-A48C-818EA735FF9B} | Mapeia para [Microsoft. PenAndTouch](#pen-and-touch) a partir do Windows 7.                                                                                                                                                                                                                                                                                          |
| Microsoft. PeopleNearMe                                      | Pessoas ao meu redor                    | {5224F545-A443-4859-BA23-7B5A95BDC8EF} | Removido do Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. PerformanceInformationAndTools                    | Ferramentas e informações de desempenho | {78F3955E-3B90-4184-BD14-5397C15F1EFC} | Removido a partir de Windows 8.1.                                                                                                                                                                                                                                                                                                                                |
| Microsoft. PhoneAndModemOptions                              | Telefone e modem                   | {40419485-C444-4567-851A-2DD7BFA1684D} | Mapeia para [Microsoft. PhoneAndModem](#phone-and-modem) a partir do Windows 7.                                                                                                                                                                                                                                                                                      |
| Microsoft. Printers                                          | Impressoras                          | {2227A280-3AEA-1069-A2DE-08002B30309D} | Mapeia para [Microsoft. DevicesAndPrinters](#devices-and-printers) a partir do Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft. ProblemReportsAndSolutions                        | Relatórios de problemas e soluções     | {FCFEECAE-EE1B-4849-AE50-685DCF7717EC} | Mapeia para [Microsoft. ActionCenter](#action-center) a partir do Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft. RegionalAndLanguageOptions                        | Opções regionais e de idioma     | {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0} | Mapeia para [Microsoft. RegionAndLanguage](#region) a partir do Windows 7. Observe que, a partir do Windows 8, a região e o idioma foram cada um dado ao seu próprio item do painel de controle. O Microsoft. RegionalAndLanguageOptions e o Microsoft. RegionAndLanguage atualmente abrem o item de região. Você deve usar o [Microsoft. Language](#location-settings) para acessar o item de idioma. |
| Microsoft. SecurityCenter                                    | Central de Segurança do Windows           | {087DA31B-0DD3-4537-8E23-64A18591F88B} | Mapeia para [Microsoft. ActionCenter](#action-center) a partir do Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft. SpeechRecognitionOptions                          | Opções de reconhecimento de fala        | {58E3C745-D971-4081-9034-86E34B30836A} | Mapeia para [Microsoft. SpeechRecognition](#speech-recognition) a partir do Windows 7.                                                                                                                                                                                                                                                                               |
| Microsoft. TaskbarAndStartMenu                               | Barra de tarefas e menu iniciar            | {0DF44EAA-FF21-4412-828E-260A8728E7F1} | Mapeia para [Microsoft. Taskbar](#speech-recognition) a partir do Windows 8.                                                                                                                                                                                                                                                                                         |
| Microsoft. WelcomeCenter                                     | Centro de boas-vindas                    | {CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1} | Mapeia para Microsoft. GettingStarted no Windows 7. Inicia o painel de controle home page a partir do Windows 8.                                                                                                                                                                                                                                                      |
| Microsoft. WindowsSidebarProperties                          | Propriedades da barra lateral do Windows        | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Mapeia para Microsoft. DesktopGadgets no Windows 7. Removido do Windows 8.                                                                                                                                                                                                                                                                                   |
| Microsoft. WindowsSideShow                                   | Windows SideShow                  | {E95A4861-D57A-4be1-AD0F-35267E261739} | Recurso preterido no Windows 8, removido a partir de Windows 8.1.                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a>Usando nomes canônicos no Política de Grupo local

A partir do Windows 7, você pode usar nomes canônicos para restringir o acesso a itens individuais do painel de controle por meio da diretiva de grupo. Esse mesmo procedimento pode ser usado no Windows Vista, mas você precisa usar o nome do módulo em vez do nome canônico.

### <a name="hiding-individual-control-panel-items"></a>Ocultando itens individuais do painel de controle

Use esse método se desejar mostrar mais itens do painel de controle do que você deseja ocultar.

1.  Execute o arquivo gpedit. msc para iniciar o Editor de Política de Grupo Local. Você também pode digitar "política de grupo" na tela iniciar Windows 8.1 e selecionar **Editar política de grupo** nos resultados da pesquisa.
2.  Selecione **configuração do usuário**  >  **modelos administrativos**  >  **painel de controle**.
3.  Selecione **ocultar itens do painel de controle especificados**.
4.  Na janela **ocultar itens do painel de controle especificados** que é aberta, clique em **habilitado**.
5.  Clique no botão **Mostrar** no painel de opções para mostrar a lista de itens de painel de controle não permitidos.
6.  Na janela **Mostrar conteúdo** que é aberta, digite um nome canônico na coluna **valor** . Repita conforme necessário.
7.  Clique em **OK**.

### <a name="showing-individual-control-panel-items"></a>Mostrando itens individuais do painel de controle

Use esse método se desejar ocultar mais itens do painel de controle do que você deseja mostrar.

1.  Execute o arquivo gpedit. msc para iniciar o Editor de Política de Grupo Local. Você também pode digitar "política de grupo" na tela iniciar Windows 8.1 e selecionar **Editar política de grupo** nos resultados da pesquisa.
2.  Selecione **configuração do usuário**  >  **modelos administrativos**  >  **painel de controle**.
3.  Selecione **Mostrar somente itens do painel de controle especificados**.
4.  Na janela **Mostrar apenas itens do painel de controle especificados** que abre, clique em **habilitado**. Isso oculta tudo no painel de controle.
5.  Clique no botão **Mostrar** no painel de opções para mostrar a lista de itens de painel de controle permitidos.
6.  Na janela **Mostrar conteúdo** que é aberta, digite um nome canônico na coluna **valor** . Repita conforme necessário.
7.  Clique em **OK**.

Se você quiser remover todas as entradas que adicionou a uma lista Mostrar ou ocultar itens do painel de controle, retorne à tela na etapa 4 e selecione **não configurado** para limpar a lista. Se você quiser manter suas entradas, mas suspender as restrições, selecione **desabilitado**.

## <a name="remarks"></a>Comentários

Você pode ver os itens no painel de controle que não estão listados aqui. Esses itens não fazem parte do Windows, mas, em vez disso, são adicionados durante a instalação de vários softwares e hardwares, como Microsoft Office ou uma placa de vídeo. Os itens do painel de controle que não são do Windows podem ou não ter um nome canônico. Para localizar o nome canônico de um item do painel de controle não listado aqui, examine o registro nestes caminhos:

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

Para obter mais informações que podem ajudá-lo a descobrir os CLSIDs necessários, consulte [como registrar itens do painel de controle do executável](how-to-register-an-executable-control-panel-item-registration-.md) e [como registrar itens do painel de controle da dll](how-to-register-dll-control-panel-item-registration-.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Executando itens do painel de controle](executing-control-panel-items.md)
</dt> <dt>

[**IOpenControlPanel**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



