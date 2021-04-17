---
description: A interface IPortableDeviceValuesCollection contém uma coleção de interfaces IPortableDeviceValues indexadas com base em zero.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interface IPortableDeviceValuesCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808331"
---
# <a name="iportabledevicevaluescollection-interface"></a>Interface IPortableDeviceValuesCollection

A interface **IPortableDeviceValuesCollection** contém uma coleção de interfaces **IPortableDeviceValues** indexadas com base em zero. Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame **CoCreate** com **CLSID \_ PortableDeviceValuesCollection**.

## <a name="members"></a>Membros

A interface **IPortableDeviceValuesCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceValuesCollection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IPortableDeviceValuesCollection** tem esses métodos.



| Método                                                       | Descrição                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Agrega**](iportabledevicevaluescollection-add.md)           | Adiciona um item à coleção<br/>                                           |
| [**Formatação**](iportabledevicevaluescollection-clear.md)       | Libera todos os itens da coleção.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Recupera um item da coleção por um índice baseado em zero.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Recupera o número de itens na coleção.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Remove o elemento armazenado no local especificado pelo índice fornecido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces de coleção**](collection-interfaces.md)
</dt> </dl>

 

