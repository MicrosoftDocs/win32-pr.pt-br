---
title: WM/UniqueFileIdentifier
description: O atributo WM/UniqueFileIdentifier contém um identificador de arquivo exclusivo para o conteúdo.
ms.assetid: 3f90dd5c-0f3d-451a-a454-f8d7f25b6201
keywords:
- Formato de mídia do Windows WM/UniqueFileIdentifier
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df336fd1f2ee8afde2c79672977084893b2929133af790ff6e2f4cbe544e1d53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928836"
---
# <a name="wmuniquefileidentifier"></a>WM/UniqueFileIdentifier

O **atributo WM/UniqueFileIdentifier** contém um identificador de arquivo exclusivo para o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMUniqueFileIdentifier

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE \_ CARACTERES DE TIPO \_ WM**

## <a name="remarks"></a>Comentários

O identificador de arquivo exclusivo é uma cadeia de caracteres genérica que pode ser usada por aplicativos e serviços para identificar exclusivamente o arquivo. A cadeia de caracteres contém valores arbitrários delimitados por ponto e vírgula. Você nunca deve limpar esse atributo. Você pode anexar valores e remover seus próprios valores, mas todos os outros devem ser deixados inalterados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




