---
title: WM/WMADRCAverageReference
description: O atributo WM/WMADRCAverageReference contém o nível médio de volume do arquivo como codificado.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Formato de mídia do Windows do WM/WMADRCAverageReference
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9948d71739aaee4f5f24f54701f8e335f8b7b79486c8820f7a5fdf48c068e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026944"
---
# <a name="wmwmadrcaveragereference"></a>WM/WMADRCAverageReference

O atributo **WM/WMADRCAverageReference** contém o nível médio de volume do arquivo como codificado.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCAverageReference

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

há quatro atributos usados por Windows Media Player para o controle de intervalo dinâmico: **wm/WMADRCAverageReference**, **wm/WMADRCPeakReference**, **wm/WMADRCAverageTarget** e **wm/WMADRCPeakTarget**. todos esses valores são definidos pelo gravador com base nas informações do codec durante a gravação de fluxos com o Windows codec de áudio de mídia 9 ou Windows codec de áudio de mídia 9 Professional. Os valores médios são definidos como o nível médio de volume do fluxo e os valores de pico são definidos para o nível máximo do volume no fluxo. Os valores de referência são somente leitura. os valores de destino são definidos por Windows Media Player quando o arquivo está sendo reproduzido para registrar as preferências de controle de intervalo dinâmico do usuário.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




