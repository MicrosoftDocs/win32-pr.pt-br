---
description: Define o estado de integridade de um aplicativo que está sendo executado em uma máquina virtual.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'Método IVmApplicationHealthMonitor:: setapplicationstate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 785b5e6254bde84497f4fcf72d15b20ff16ccd7319ecc3631c0864b3e4992655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392351"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>Método IVmApplicationHealthMonitor:: setapplicationstate

Define o estado de integridade de um aplicativo que está sendo executado em uma máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Uma representação **BSTR** do **GUID** que identifica o aplicativo. É responsabilidade do aplicativo de chamada criar e manter os identificadores que ele usa para os aplicativos que estão sendo monitorados.

</dd> <dt>

*Nome* \[ do no\]
</dt> <dd>

O nome de exibição do aplicativo. Esse nome é usado em uma entrada de log de eventos informativa para a alteração de estado.

</dd> <dt>

*Estado* \[ no\]
</dt> <dd>

Um valor da enumeração [**de \_ estado do aplicativo**](application-state.md) que especifica o novo estado de integridade do aplicativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O estado dos aplicativos em execução na máquina virtual é refletido no valor da propriedade **OperationalStatus** \[ 1 \] da classe [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .

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

 

 




