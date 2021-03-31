---
title: Método Counters. Remove
description: Remove uma instância de monoitem da coleção.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Remover o método SysMon
- Método de remoção SysMon, classe de contadores
- Classe Counters SysMon, método remove
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918318"
---
# <a name="countersremove-method"></a>Método Counters. Remove

Remove uma instância de [**monoitem**](counteritem.md) da coleção.

## <a name="syntax"></a>Sintaxe


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

Índice do objeto de [**coitem**](counteritem.md) a ser removido da coleção. O índice é baseado em um.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="exceptions"></a>Exceções



| Tipo de exceção                                  | Condição                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | O índice especificado não é válido. O valor Err. Number é???. |



 

## <a name="remarks"></a>Comentários

Para remover todos os contadores da coleção, você pode chamar [**SystemMonitor. Reset**](systemmonitor-reset.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Contadores**](counters.md)
</dt> <dt>

[**SystemMonitor. Reset**](systemmonitor-reset.md)
</dt> </dl>

 

 





