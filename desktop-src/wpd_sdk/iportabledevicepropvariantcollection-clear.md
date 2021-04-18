---
description: O método Clear libera e, em seguida, remove todos os itens da coleção. A coleção é considerada vazia depois de chamar esse método.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'Método IPortableDevicePropVariantCollection:: Clear (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765131"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a>Método IPortableDevicePropVariantCollection:: Clear

O método **Clear** libera e, em seguida, remove todos os itens da coleção. A coleção é considerada vazia depois de chamar esse método.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Depois de chamar **Clear**, a coleção é considerada sem tipo, o que significa que o VarType definido anteriormente não está mais restringindo as operações de **adição** . Uma chamada para **Add** depois de chamar **Clear** é considerada a "primeiro" **Adicionar** para essa coleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




