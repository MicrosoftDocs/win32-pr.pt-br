---
title: WM/ContainerFormat
description: O atributo WM/ContainerFormat especifica o tipo de arquivo que é carregado no objeto de chamada.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Formato de mídia do Windows do WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e0d5cc430b0580c6719d212d664d8c19ddc65eee64e5877a8e6aba80d94a6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839436"
---
# <a name="wmcontainerformat"></a>WM/ContainerFormat

O atributo **WM/containerFormat** especifica o tipo de arquivo que é carregado no objeto de chamada.

## <a name="global-constant"></a>Constante global

g \_ wszWMContainerFormat

## <a name="data-type"></a>Tipo de Dados

[**WMT \_ \_formato de armazenamento**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT \_ tipo \_ Binary**)

## <a name="remarks"></a>Comentários

Esse atributo é usado em vez de **IWMProfile3:: GetStorageFormat** e **IWMProfile3:: SetStorageFormat**, que não têm mais suporte.

Este é um atributo codificado.

Este atributo não pode ser duplicado no nível do arquivo. se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do formato de mídia Windows.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




