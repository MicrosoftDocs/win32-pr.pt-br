---
title: Interface IVMGuestOS (VPCCOMInterfaces. h)
description: Define o sistema operacional convidado em execução dentro de uma máquina virtual.
ms.assetid: fb31f294-94ad-4545-8d59-849a5f2fe780
keywords:
- Virtual PC de interface IVMGuestOS
- Virtual PC de interface IVMGuestOS, descrito
topic_type:
- apiref
api_name:
- IVMGuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a36c6c579209903c45e3888a11f17d40c168bbb2e215c60fb25e5b12330962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593994"
---
# <a name="ivmguestos-interface"></a>Interface IVMGuestOS

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define o sistema operacional convidado em execução dentro de uma máquina virtual. Essa interface permite que você interaja com os componentes de integração em execução dentro do sistema operacional convidado. O **IVMGuestOS** para uma máquina virtual pode ser recuperado usando a propriedade [**IVMVirtualMachine:: GuestOS**](ivmvirtualmachine-guestos.md) .

## <a name="members"></a>Membros

A interface **IVMGuestOS** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMGuestOS** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMGuestOS** tem esses métodos.



| Método                                                                          | Descrição                                                                                             |
|:--------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetOsVersionInfo**](ivmguestos-getosversioninfo.md)                         | Recupera informações de versão para o sistema operacional convidado em execução na máquina virtual.<br/> |
| [**GetParameter**](ivmguestos-getparameter.md)                                 | Recupera um parâmetro nomeado dentro do convidado.<br/>                                                |
| [**InstallIntegrationComponents**](ivmguestos-installintegrationcomponents.md) | Localiza e instala os componentes de integração mais recentes no sistema operacional convidado.<br/>      |
| [**IsUserLoggedOn**](ivmguestos-isuserloggedon.md)                             | Determina se a sessão solicitada está presente.<br/>                                         |
| [**Verbos**](ivmguestos-logoff.md)                                             | Faz logoff de todos os usuários do sistema operacional convidado.<br/>                                          |
| [**Reiniciar**](ivmguestos-restart.md)                                           | Reinicia o sistema operacional convidado.<br/>                                                         |
| [**SetParameter**](ivmguestos-setparameter.md)                                 | Define um parâmetro nomeado dentro do convidado.<br/>                                                     |
| [**Desligar**](ivmguestos-shutdown.md)                                         | Desliga o sistema operacional convidado.<br/>                                                       |



 

### <a name="properties"></a>Propriedades

A interface **IVMGuestOS** tem essas propriedades.



| Propriedade                                                                                   | Tipo de acesso           | Descrição                                                                                                                                 |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanShutdown**](ivmguestos-canshutdown.md)<br/>                                   | Somente leitura<br/>  | Indica se o sistema operacional convidado pode ser desligado corretamente (requer componentes de integração).<br/>                         |
| [**ComputerName**](ivmguestos-computername.md)<br/>                                 | Somente leitura<br/>  | O nome do computador do sistema operacional convidado em execução na máquina virtual.<br/>                                                  |
| [**CSDVersion**](ivmguestos-csdversion.md)<br/>                                     | Somente leitura<br/>  | O CSDVersion do sistema operacional convidado em execução na máquina virtual.<br/>                                                     |
| [**HeartbeatPercentage**](ivmguestos-heartbeatpercentage.md)<br/>                   | Somente leitura<br/>  | A porcentagem de pulsações esperadas recebidas no último minuto.<br/>                                                             |
| [**IntegrationComponentsVersion**](ivmguestos-integrationcomponentsversion.md)<br/> | Somente leitura<br/>  | A versão dos componentes de integração instalados no sistema operacional convidado.<br/>                                               |
| [**Ispulsação**](ivmguestos-isheartbeating.md)<br/>                             | Somente leitura<br/>  | Indica se a máquina virtual tem uma pulsação.<br/>                                                                           |
| [**IsHostTimeSyncEnabled**](ivmguestos-ishosttimesyncenabled.md)<br/>               | Leitura/gravação<br/> | Indica se os componentes de integração nesta máquina virtual devem sincronizar o relógio do convidado com o relógio do host.<br/> |
| [**MultipleUserSessionsAllowed**](ivmguestos-multipleusersessionsallowed.md)<br/>   | Somente leitura<br/>  | Indica se várias sessões de usuário simultâneas são permitidas no sistema operacional convidado.<br/>                                 |
| [**OSBuildNumber**](ivmguestos-osbuildnumber.md)<br/>                               | Somente leitura<br/>  | O número de Build do sistema operacional convidado em execução na máquina virtual.<br/>                                                   |
| [**OSMajorVersion**](ivmguestos-osmajorversion.md)<br/>                             | Somente leitura<br/>  | A versão principal do sistema operacional convidado em execução na máquina virtual.<br/>                                                  |
| [**OSMinorVersion**](ivmguestos-osminorversion.md)<br/>                             | Somente leitura<br/>  | A versão secundária do sistema operacional convidado em execução na máquina virtual.<br/>                                                  |
| [**OSName**](ivmguestos-osname.md)<br/>                                             | Somente leitura<br/>  | O nome do sistema operacional convidado em execução na máquina virtual.<br/>                                                           |
| [**OSPlatformId**](ivmguestos-osplatformid.md)<br/>                                 | Somente leitura<br/>  | O identificador de plataforma do sistema operacional convidado em execução na máquina virtual.<br/>                                            |
| [**OSVersion**](ivmguestos-osversion.md)<br/>                                       | Somente leitura<br/>  | A versão do sistema operacional convidado em execução na máquina virtual.<br/>                                                        |
| [**ProductType**](ivmguestos-producttype.md)<br/>                                   | Somente leitura<br/>  | O tipo de produto do sistema operacional convidado em execução na máquina virtual.<br/>                                                   |
| [**ScreenLocked**](ivmguestos-screenlocked.md)<br/>                                 | Somente leitura<br/>  | Indica se a tela está bloqueada no sistema operacional convidado.<br/>                                                            |
| [**ServicePackMajor**](ivmguestos-servicepackmajor.md)<br/>                         | Somente leitura<br/>  | A versão principal do service pack do sistema operacional convidado em execução na máquina virtual.<br/>                              |
| [**ServicePackMinor**](ivmguestos-servicepackminor.md)<br/>                         | Somente leitura<br/>  | A versão secundária do service pack do sistema operacional convidado em execução na máquina virtual.<br/>                              |
| [**SuiteMask**](ivmguestos-suitemask.md)<br/>                                       | Somente leitura<br/>  | O SuiteMask do sistema operacional convidado em execução na máquina virtual.<br/>                                                      |
| [**TerminalServerPort**](ivmguestos-terminalserverport.md)<br/>                     | Somente leitura<br/>  | Porta usada por Serviços de Área de Trabalho Remota no sistema operacional convidado.<br/>                                                              |
| [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md)<br/>   | Somente leitura<br/>  | O status da inicialização dos Serviços de Terminal no sistema operacional convidado.<br/>                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



 

