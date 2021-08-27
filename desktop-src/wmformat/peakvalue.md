---
title: PeakValue
description: O atributo PeakValue contém um valor de amplitude de 16 bits que designa o nível de volume de pico do conteúdo de áudio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- Formato de mídia do Windows PeakValue
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3089ac6d4b789d740f256a5c44c1911eb3501bc654c3b94d0006d405616572
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110256"
---
# <a name="peakvalue"></a>PeakValue

O **atributo PeakValue** contém um valor de amplitude de 16 bits que designa o nível de volume de pico do conteúdo de áudio. Com [**AverageLevel**](averagelevel.md), esse atributo é usado para normalização. Normalização é o processo de ajustar o nível de volume de reprodução de arquivos de áudio para que as partes mais altas dos arquivos reproduzam no mesmo nível e o volume médio de cada um seja o mesmo..

## <a name="global-constant"></a>Constante global

g \_ wszPeakValue

## <a name="data-type"></a>Tipo de Dados

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Comentários

Esse atributo é definido pelo objeto writer com base nas informações do codec. Somente os fluxos compactados com um dos codecs Windows Media Audio têm um valor definido automaticamente.

**PeakValue** não é somente leitura. No entanto, se o arquivo for interpretado pelo Windows Media Player, você não deverá alterar esse valor. O Windows Media Player usa isso para normalizar os níveis de arquivos em uma playlist.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




