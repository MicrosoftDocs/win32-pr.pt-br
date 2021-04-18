---
description: O método GetAt recupera um PROPERTYKEY da coleção por índice.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'Método IPortableDeviceKeyCollection:: GetAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810895"
---
# <a name="iportabledevicekeycollectiongetat-method"></a>Método IPortableDeviceKeyCollection:: GetAt

O método **GetAt** recupera um **PROPERTYKEY** da coleção por índice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ no\]
</dt> <dd>

**DWORD** que contém o índice da chave a ser recuperada.

</dd> <dt>

*pKey* \[ fora\]
</dt> <dd>

Ponteiro para um objeto **PROPERTYKEY** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O índice passado estava fora do intervalo.<br/>     |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Um argumento de ponteiro necessário era **nulo**.<br/> |



 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[Recuperando eventos de serviço com suporte](retrieving-supported-events.md)
</dt> <dt>

[Recuperando métodos de serviço com suporte](retrieving-supported-methods.md)
</dt> </dl>

 

 




