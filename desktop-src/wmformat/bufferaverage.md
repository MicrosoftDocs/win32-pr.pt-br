---
title: BufferAverage
description: O atributo BufferAverage contém o tamanho médio do buffer necessário para um fluxo de taxa de bits variável (VBR).
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
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084216"
---
# <a name="bufferaverage"></a>BufferAverage

O atributo **BufferAverage** contém o tamanho médio do buffer necessário para um fluxo de taxa de bits variável (VBR).

## <a name="global-constant"></a>Constante global

g \_ wszBufferAverage

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

Ao acessar a interface **IWMHeaderInfo3** do objeto gravador, você pode adicionar ou alterar esse valor. Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura.

O gravador grava automaticamente um valor de **BufferAverage** para cada fluxo de VBR.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




