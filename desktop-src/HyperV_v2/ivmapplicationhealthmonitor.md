---
description: Relata o status de integridade de um aplicativo que está sendo executado em uma máquina virtual para os componentes de integração do Hyper-V em execução na mesma máquina virtual.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Interface IVmApplicationHealthMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759877"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>Interface IVmApplicationHealthMonitor

Relata o status de integridade de um aplicativo que está sendo executado em uma máquina virtual para os componentes de integração do Hyper-V em execução na mesma máquina virtual. O estado dos aplicativos em execução na máquina virtual é refletido no valor da propriedade **OperationalStatus** \[ 1 \] da classe [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) . Essa interface também fornece uma maneira de redefinir todo o estado do aplicativo acumulado no Hyper-V.

Essa interface é implementada pelos componentes de integração do Hyper-V do Windows 8. Uma instância dessa interface é obtida com a criação de uma instância do CLSID do **397a2e5f-348c-482D-b9a3-57d383b483cd** .

## <a name="members"></a>Membros

A interface **IVmApplicationHealthMonitor** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVmApplicationHealthMonitor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IVmApplicationHealthMonitor** tem esses métodos.



| Método                                                                                   | Descrição                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ResetAllApplicationState**](ivmapplicationhealthmonitor-resetallapplicationstate.md) | Redefine o estado de integridade de todos os aplicativos em uma máquina virtual.<br/>            |
| [**Setapplicationstate**](ivmapplicationhealthmonitor-setapplicationstate.md)           | Define o estado de integridade de um aplicativo que está sendo executado em uma máquina virtual.<br/> |



 

## <a name="remarks"></a>Comentários

Para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                                                                                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                                                                                           |
| Versão<br/>                  | Componentes de integração do Windows 8<br/>                                                                                                                                |
| INSERI<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ IVmApplicationHealthMonitor é definido como 267a0284-848f-447e-a096-5e10a1a76bca<br/> O identificador de objeto é definido como 397a2e5f-348c-482D-b9a3-57d383b483cd<br/> |



 

