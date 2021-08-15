---
title: Is_Trusted
description: O atributo Is Trusted é um atributo de nível de arquivo que especifica se a URL de aquisição \_ de licença no arquivo é confiável.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted formato de mídia do Windows
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e255c91c5779eb44da8e587601fdfd9264f10888a46a7f216ae2af619ff9f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198272"
---
# <a name="is_trusted"></a>É \_ confiável

O **atributo \_ Is Trusted** é um atributo de nível de arquivo que especifica se a URL de aquisição de licença no arquivo é confiável.

## <a name="global-constant"></a>Constante global

g \_ wszWMTrusted

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentários

Esse é um atributo codificado.

Antes de navegar até uma URL de aquisição de licença contida em um arquivo protegido por DRM, um aplicativo deve primeiro verificar se essa propriedade é verdadeira. Se for false, o aplicativo deverá notificar o usuário de que a URL possivelmente foi adulterada.

Esse atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK Windows Formato de Mídia.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




