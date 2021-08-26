---
description: A interface IPortableDeviceValuesCollection contém uma coleção de interfaces IPortableDeviceValues indexadas com base em zero.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interface IPortableDeviceValuesCollection (PortableDeviceTypes.h)
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
ms.openlocfilehash: cd6547a96013b2b83ce9962a62f0837dd01cacac6f3e64adc3b964754c148c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928376"
---
# <a name="iportabledevicevaluescollection-interface"></a>Interface IPortableDeviceValuesCollection

A interface **IPortableDeviceValuesCollection** contém uma coleção de interfaces **IPortableDeviceValues** indexadas com base em zero. Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame **CoCreate** com **CLSID \_ PortableDeviceValuesCollection**.

## <a name="members"></a>Membros

A interface **IPortableDeviceValuesCollection** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceValuesCollection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IPortableDeviceValuesCollection** tem esses métodos.



| Método                                                       | Descrição                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Adicionar**](iportabledevicevaluescollection-add.md)           | Adiciona um item à coleção<br/>                                           |
| [**Limpar**](iportabledevicevaluescollection-clear.md)       | Libera todos os itens da coleção.<br/>                                  |
| [**Getat**](iportabledevicevaluescollection-getat.md)       | Recupera um item da coleção por um índice baseado em zero.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Recupera o número de itens na coleção.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Remove o elemento armazenado no local especificado pelo índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces de coleção**](collection-interfaces.md)
</dt> </dl>

 

