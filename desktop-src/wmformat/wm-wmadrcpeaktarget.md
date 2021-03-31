---
title: WM/WMADRCPeakTarget
description: O atributo WM/WMADRCPeakTarget contém o nível máximo de volume solicitado pelo usuário. Esse valor é usado pelo Windows Media Player para controle de intervalo dinâmico.
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
ms.openlocfilehash: 55eac4ea68cd61e2cfa0b5c185dc1a4ad17e5ce8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638605"
---
# <a name="wmwmadrcpeaktarget"></a>WM/WMADRCPeakTarget

O atributo **WM/WMADRCPeakTarget** contém o nível máximo de volume solicitado pelo usuário. Esse valor é usado pelo Windows Media Player para controle de intervalo dinâmico.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCPeakTarget

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

Há quatro atributos usados pelo Windows Media Player para o controle de intervalo dinâmico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**. Todos esses valores são definidos pelo gravador com base nas informações do codec ao gravar fluxos com o codec do Windows Media Audio 9 ou o Windows Media Audio 9 Professional. Os valores médios são definidos como o nível médio de volume do fluxo e os valores de pico são definidos para o nível máximo do volume no fluxo. Os valores de referência são somente leitura. Os valores de destino são definidos pelo Windows Media Player quando o arquivo está sendo reproduzido para registrar as preferências de controle de intervalo dinâmico do usuário.

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

 

 




