---
title: Is_Trusted
description: O \_ atributo is Trusted é um atributo de nível de arquivo que especifica se a URL de aquisição de licença no arquivo é confiável.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted o formato Windows Media
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916820"
---
# <a name="is_trusted"></a>É \_ confiável

O atributo **is \_ Trusted** é um atributo de nível de arquivo que especifica se a URL de aquisição de licença no arquivo é confiável.

## <a name="global-constant"></a>Constante global

g \_ wszWMTrusted

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

Antes de navegar para uma URL de aquisição de licença contida em um arquivo protegido por DRM, um aplicativo deve primeiro verificar se essa propriedade é verdadeira. Se for false, o aplicativo deverá notificar o usuário de que a URL possivelmente foi adulterada.

Este atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




