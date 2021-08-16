---
title: Is_Protected
description: O \_ atributo is Protected é um atributo de nível de arquivo que especifica se o conteúdo no arquivo foi protegido usando o DRM (gerenciamento de direitos digitais).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected o formato Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0759dfc781409a1331403c3b02c2645f6ad843925584eab2a55f31a0c8d31af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847413"
---
# <a name="is_protected"></a>É \_ protegido

O atributo **is \_ Protected** é um atributo de nível de arquivo que especifica se o conteúdo no arquivo foi protegido usando o DRM (gerenciamento de direitos digitais).

## <a name="global-constant"></a>Constante global

g \_ wszWMProtected

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado. A recuperação dessa propriedade fornece as mesmas informações que chamam [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).

Este atributo não pode ser duplicado no nível do arquivo. se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do formato de mídia Windows.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




