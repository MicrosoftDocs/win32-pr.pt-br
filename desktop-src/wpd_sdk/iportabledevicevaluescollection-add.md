---
description: 'Método IPortableDeviceValuesCollection:: Add – o método add adiciona um item à coleção.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'Método IPortableDeviceValuesCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9cc105ae553d78dd6c8a12219be8e2c42cba1e236c25a0392457b36553bd4e40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839316"
---
# <a name="iportabledevicevaluescollectionadd-method"></a>Método IPortableDeviceValuesCollection:: Add

O método **Add** adiciona um item à coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valores principais* \[ no\]
</dt> <dd>

Ponteiro para uma interface **IPortableDeviceValues** para adicionar à coleção. A interface não é realmente copiada, mas **AddRef** é chamado nela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória suficiente disponível para adicionar o valor à coleção.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




