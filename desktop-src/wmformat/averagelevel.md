---
title: AverageLevel
description: O atributo AverageLevel contém um valor de amplitude de 16 bits que designa o nível médio de volume de conteúdo de áudio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- Formato de mídia do Windows AverageLevel
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd8745c5983eca67a02506b6cdeeabaca0a61a4c3f8b2a6993a73359d87adba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028154"
---
# <a name="averagelevel"></a>AverageLevel

O atributo **AverageLevel** contém um valor de amplitude de 16 bits que designa o nível médio de volume de conteúdo de áudio. Com o [**picovalue**](peakvalue.md), esse atributo é usado para normalização. A normalização é o processo de ajustar o nível de volume de reprodução de arquivos de áudio para que as partes mais alta da reprodução de arquivos no mesmo nível e o volume médio de cada um seja o mesmo.

## <a name="global-constant"></a>Constante global

g \_ wszAverageLevel

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

Esse atributo é definido pelo objeto do gravador com base nas informações do codec. somente os fluxos compactados com um dos Windows codecs de áudio de mídia têm um valor definido automaticamente.

**AverageLevel** não é somente leitura. no entanto, se o arquivo for reproduzido pelo Windows Media Player, você não deverá alterar esse valor. o Windows Media Player usa isso para normalizar os níveis de arquivos em uma lista de reprodução.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




