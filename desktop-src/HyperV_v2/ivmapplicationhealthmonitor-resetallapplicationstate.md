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
ms.openlocfilehash: 4e97d5d16200501d77acf8b0b02cc5562d51706fcc46298421ad7f7e8fc0dfac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694346"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>Método IVmApplicationHealthMonitor:: ResetAllApplicationState

Redefine o estado de integridade de todos os aplicativos em uma máquina virtual. Se for bem-sucedido, o estado de integridade de todos os aplicativos monitorados será definido como **ApplicationStateHealthy**.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                      |
| Versão<br/>                  | Componentes de integração para Windows 8<br/>                                                           |
| INSERI<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




