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
ms.openlocfilehash: 46ec38d0961ffc6ffc50434cdecf69e6dde663dfeaff5e331455a9575b3426e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930856"
---
# <a name="hasattachedimages"></a>HasAttachedImages

O atributo **HasAttachedImages** é um atributo em nível de arquivo que especifica se o arquivo é um arquivo MP3 com quadros APIC ID3 anexados.

## <a name="global-constant"></a>Constante global

g \_ wszWMHasAttachedImages

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

Este atributo não pode ser duplicado no nível do arquivo. se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do formato de mídia Windows.

O **HasAttachedImages** foi projetado para informar um aplicativo de que as imagens estavam presentes para que pudessem ser recuperadas usando a interface [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) . Agora que as imagens têm suporte usando o atributo [**WM/Picture**](wmpicture.md) , o **HasAttachedImages** não é mais necessário.

Para determinar se um arquivo contém imagens, chame [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) especificando o atributo **WM/Picture** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




