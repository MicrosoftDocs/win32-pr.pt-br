---
title: BufferAverage
description: O atributo BufferAverage contém o tamanho médio do buffer necessário para um fluxo de VBR (taxa de bits variável).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- Formato de mídia do Windows BufferAverage
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd839bff96f5ba327e585f8608bd4612fc047d354c24fee972e507ea5ca681f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656116"
---
# <a name="bufferaverage"></a>BufferAverage

O **atributo BufferAverage** contém o tamanho médio do buffer necessário para um fluxo de VBR (taxa de bits variável).

## <a name="global-constant"></a>Constante global

g \_ wszBufferAverage

## <a name="data-type"></a>Tipo de Dados

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Comentários

Ao acessar a interface **IWMHeaderInfo3** do objeto writer, você pode adicionar ou alterar esse valor. Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura.

O autor grava automaticamente um **valor BufferAverage** para cada fluxo VBR.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




