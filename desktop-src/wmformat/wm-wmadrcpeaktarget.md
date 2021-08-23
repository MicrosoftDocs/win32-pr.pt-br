---
title: WM/WMADRCPeakTarget
description: O atributo WM/WMADRCPeakTarget contém o nível máximo de volume solicitado pelo usuário. esse valor é usado por Windows Media Player para controle de intervalo dinâmico.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- Formato de mídia do Windows do WM/WMADRCPeakTarget
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c87c8d62316bfa3e732d0cdc00e0fcb5295c30e675fd9c21fcd5ac766f239f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590676"
---
# <a name="wmwmadrcpeaktarget"></a>WM/WMADRCPeakTarget

O atributo **WM/WMADRCPeakTarget** contém o nível máximo de volume solicitado pelo usuário. esse valor é usado por Windows Media Player para controle de intervalo dinâmico.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCPeakTarget

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

há quatro atributos usados por Windows Media Player para o controle de intervalo dinâmico: **wm/WMADRCAverageReference**, **wm/WMADRCPeakReference**, **wm/WMADRCAverageTarget** e **wm/WMADRCPeakTarget**. todos esses valores são definidos pelo gravador com base nas informações do codec durante a gravação de fluxos com o Windows codec de áudio de mídia 9 ou Windows codec de áudio de mídia 9 Professional. Os valores médios são definidos como o nível médio de volume do fluxo e os valores de pico são definidos para o nível máximo do volume no fluxo. Os valores de referência são somente leitura. os valores de destino são definidos por Windows Media Player quando o arquivo está sendo reproduzido para registrar as preferências de controle de intervalo dinâmico do usuário.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




