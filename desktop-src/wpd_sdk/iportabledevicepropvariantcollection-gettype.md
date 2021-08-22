---
description: O método GetType recupera o tipo de dados dos itens na coleção.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'Método IPortableDevicePropVariantCollection:: GetType (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c29e47cd08b5c31012df92ca04e018d38f7adb7f8802ec534682289852f518b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963735"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>Método IPortableDevicePropVariantCollection:: GetType

O método **GetType** recupera o tipo de dados dos itens na coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pvt* \[ fora\]
</dt> <dd>

Um valor de enumeração do **VarType** do Platform SDK que indica o tipo de dados de todos os itens na coleção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                               | Descrição                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Um argumento de ponteiro necessário era **nulo**.<br/> |



 

## <a name="remarks"></a>Comentários

Todos os itens que são armazenados em um **IPortableDevicePropVariantCollection** são do mesmo tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




