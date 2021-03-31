---
description: Redefine o estado de integridade de todos os aplicativos em uma máquina virtual.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'Método IVmApplicationHealthMonitor:: ResetAllApplicationState'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827613"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>Método IVmApplicationHealthMonitor:: ResetAllApplicationState

Redefine o estado de integridade de todos os aplicativos em uma máquina virtual. Se for bem-sucedido, o estado de integridade de todos os aplicativos monitorados será definido como **ApplicationStateHealthy**.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                      |
| Versão<br/>                  | Componentes de integração do Windows 8<br/>                                                           |
| INSERI<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




