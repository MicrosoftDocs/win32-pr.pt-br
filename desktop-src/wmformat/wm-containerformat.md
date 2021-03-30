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
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638599"
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

Este atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




