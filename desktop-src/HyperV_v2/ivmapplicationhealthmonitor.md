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
ms.openlocfilehash: 3cc565c43fd61ebed6183cbfa2f4fdf7ece7d39872f23718fb1a12a3b591d531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694316"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>Interface IVmApplicationHealthMonitor

Relata o status de integridade de um aplicativo que está sendo executado em uma máquina virtual para os componentes de integração do Hyper-V em execução na mesma máquina virtual. O estado dos aplicativos em execução na máquina virtual é refletido no valor da propriedade **OperationalStatus** \[ 1 \] da classe [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) . Essa interface também fornece uma maneira de redefinir todo o estado do aplicativo acumulado no Hyper-V.

essa interface é implementada pelo Windows 8 componentes de integração do Hyper-V. Uma instância dessa interface é obtida com a criação de uma instância do CLSID do **397a2e5f-348c-482D-b9a3-57d383b483cd** .

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

para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                                                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                                                                                           |
| Versão<br/>                  | Componentes de integração para Windows 8<br/>                                                                                                                                |
| INSERI<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ IVmApplicationHealthMonitor é definido como 267a0284-848f-447e-a096-5e10a1a76bca<br/> O identificador de objeto é definido como 397a2e5f-348c-482D-b9a3-57d383b483cd<br/> |



 

