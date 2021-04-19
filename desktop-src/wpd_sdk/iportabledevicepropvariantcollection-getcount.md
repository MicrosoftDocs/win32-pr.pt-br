---
description: O método GetCount recupera o número de itens nesta coleção.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'Método IPortableDevicePropVariantCollection:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793996"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a>Método IPortableDevicePropVariantCollection:: GetCount

O método **GetCount** recupera o número de itens nesta coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcElems* \[ no\]
</dt> <dd>

Ponteiro para um **DWORD** que contém o número de itens na coleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                               | Descrição                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Um argumento de ponteiro necessário era **nulo**.<br/> |



 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Recuperando eventos de serviço com suporte](retrieving-supported-events.md)
</dt> <dt>

[Recuperando formatos de serviço com suporte](retrieving-supported-formats.md)
</dt> <dt>

[Recuperando métodos de serviço com suporte](retrieving-supported-methods.md)
</dt> <dt>

[Recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Definindo propriedades para vários objetos](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




