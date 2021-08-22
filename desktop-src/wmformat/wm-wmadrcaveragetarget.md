---
title: WM/WMADRCAverageTarget
description: O atributo WM/WMADRCAverageTarget contém o nível de volume médio solicitado pelo usuário. Esse valor é usado por Windows Media Player controle de intervalo dinâmico.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Formato de mídia do Windows WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd08dd09b6db671a0af1d816162923624cb781148f557ce4bee21fe2dc9a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083910"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

O **atributo WM/WMADRCAverageTarget** contém o nível de volume médio solicitado pelo usuário. Esse valor é usado por Windows Media Player controle de intervalo dinâmico.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCAverageTarget

## <a name="data-type"></a>Tipo de Dados

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Comentários

Há quatro atributos usados pelo Windows Media Player para controle de intervalo dinâmico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**. Todos esses valores são definidos pelo autor com base nas informações do codec ao escrever fluxos com o codec Windows Media Audio 9 ou o codec Windows Media Audio 9 Professional. Os valores médios são definidos como o nível médio de volume do fluxo e os valores de pico são definidos para o nível máximo de volume no fluxo. Os valores de referência são somente leitura. Os valores de destino são definidos Windows Media Player quando o arquivo está sendo tocado para registrar as preferências de controle de intervalo dinâmico do usuário.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




