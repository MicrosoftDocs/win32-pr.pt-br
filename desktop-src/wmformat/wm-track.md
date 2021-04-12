---
title: WM/Track
description: O atributo WM/Track contém o número de faixa do conteúdo. Esse atributo é baseado em zero e tem suporte para compatibilidade com versões anteriores. Em vez disso, o novo conteúdo deve usar o atributo WM/TrackNumber.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- Formato de mídia do WM/Track Windows
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364591"
---
# <a name="wmtrack"></a>WM/Track

O atributo **WM/Track** contém o número de faixa do conteúdo. Esse atributo é baseado em zero e tem suporte para compatibilidade com versões anteriores. Em vez disso, o novo conteúdo deve usar o atributo [**WM/TrackNumber**](wm-tracknumber.md) .

## <a name="global-constant"></a>Constante global

g \_ wszWMTrack

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Muitos aplicativos existentes gravam o valor do **WM/Track** como um **DWORD**. Se você criar um aplicativo que reproduza arquivos de fontes desconhecidas, deverá incluir o código para lidar com valores de cadeia de caracteres e **DWORD** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




