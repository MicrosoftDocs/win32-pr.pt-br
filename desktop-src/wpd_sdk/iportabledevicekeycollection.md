---
description: A interface IPortableDeviceKeyCollection contém uma coleção de valores PROPERTYKEY. Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame CoCreate com CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interface IPortableDeviceKeyCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791490"
---
# <a name="iportabledevicekeycollection-interface"></a>Interface IPortableDeviceKeyCollection

A interface **IPortableDeviceKeyCollection** contém uma coleção de valores **PROPERTYKEY** . Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame **CoCreate** com **CLSID \_ PortableDeviceKeyCollection**.

## <a name="members"></a>Membros

A interface **IPortableDeviceKeyCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceKeyCollection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IPortableDeviceKeyCollection** tem esses métodos.



| Método                                                    | Descrição                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Agrega**](iportabledevicekeycollection-add.md)           | Adiciona uma chave de propriedade à coleção.<br/>                                   |
| [**Formatação**](iportabledevicekeycollection-clear.md)       | Exclui todos os itens da coleção.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Recupera um **PROPERTYKEY** da coleção por índice.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Recupera o número de chaves nesta coleção.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Remove o elemento armazenado no local especificado pelo índice fornecido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces de coleção**](collection-interfaces.md)
</dt> </dl>

 

