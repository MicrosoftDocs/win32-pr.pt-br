---
description: A interface IPortableDevicePropVariantCollection contém uma coleção de valores PROPVARIANT indexados do mesmo VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interface IPortableDevicePropVariantCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f5f6a59dfd741eb524c4b6015c5384123b6a2d491b5bdc030053bbc88ad6800a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026884"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>Interface IPortableDevicePropVariantCollection

A interface **IPortableDevicePropVariantCollection** contém uma coleção de valores **PROPVARIANT** indexados do mesmo VarType. O VARTYPE do primeiro item que é adicionado à coleção determina o VARTYPE da coleção. Uma tentativa de adicionar um item de um VARTYPE diferente poderá falhar se o valor de **PROPVARIANT** não puder ser alterado para o VarType atual da coleção. Para alterar o VARTYPE da coleção, chame **ChangeType**.

Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame **CoCreate** com **CLSID \_ PortableDevicePropVariantCollection**.

## <a name="members"></a>Membros

A interface **IPortableDevicePropVariantCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDevicePropVariantCollection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IPortableDevicePropVariantCollection** tem esses métodos.



| Método                                                                | Descrição                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Agrega**](iportabledevicepropvariantcollection-add.md)               | Adiciona um item à coleção.<br/>                                          |
| [**ChangeType**](iportabledevicepropvariantcollection-changetype.md) | Converte todos os itens da coleção no VARTYPE especificado.<br/>           |
| [**Limpar**](iportabledevicepropvariantcollection-clear.md)           | Libera e, em seguida, remove todos os itens da coleção.<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | Recupera um item da coleção por um índice baseado em zero.<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | Recupera o número de itens nesta coleção.<br/>                        |
| [**GetType**](iportabledevicepropvariantcollection-gettype.md)       | Recupera o tipo de dados dos itens na coleção.<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | Remove o elemento armazenado no local especificado pelo índice fornecido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces de coleção**](collection-interfaces.md)
</dt> </dl>

 

