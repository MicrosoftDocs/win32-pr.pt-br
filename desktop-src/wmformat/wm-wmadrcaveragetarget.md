---
title: WM/WMADRCAverageTarget
description: O atributo WM/WMADRCAverageTarget contém o nível médio de volume solicitado pelo usuário. Esse valor é usado pelo Windows Media Player para controle de intervalo dinâmico.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Formato de mídia do Windows do WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105797589"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

O atributo **WM/WMADRCAverageTarget** contém o nível médio de volume solicitado pelo usuário. Esse valor é usado pelo Windows Media Player para controle de intervalo dinâmico.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCAverageTarget

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

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




