---
title: HasAttachedImages
description: O atributo HasAttachedImages é um atributo em nível de arquivo que especifica se o arquivo é um arquivo MP3 com quadros APIC ID3 anexados.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Formato de mídia do Windows HasAttachedImages
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105811527"
---
# <a name="hasattachedimages"></a>HasAttachedImages

O atributo **HasAttachedImages** é um atributo em nível de arquivo que especifica se o arquivo é um arquivo MP3 com quadros APIC ID3 anexados.

## <a name="global-constant"></a>Constante global

g \_ wszWMHasAttachedImages

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

Este atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.

O **HasAttachedImages** foi projetado para informar um aplicativo de que as imagens estavam presentes para que pudessem ser recuperadas usando a interface [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) . Agora que as imagens têm suporte usando o atributo [**WM/Picture**](wmpicture.md) , o **HasAttachedImages** não é mais necessário.

Para determinar se um arquivo contém imagens, chame [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) especificando o atributo **WM/Picture** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




