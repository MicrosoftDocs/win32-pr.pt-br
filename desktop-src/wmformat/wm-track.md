---
title: WM/Track
description: O atributo WM/Track contém o número de faixa do conteúdo. Esse atributo é baseado em zero e tem suporte para compatibilidade com backward. Em vez disso, o novo conteúdo deve usar o atributo WM/TrackNumber.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- Formato de mídia do Windows WM/Track
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1113fde7b0b29b6f1f7618e9d531df83070725b9e05e70e09f64f93b027abfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026934"
---
# <a name="wmtrack"></a>WM/Track

O **atributo WM/Track** contém o número de faixa do conteúdo. Esse atributo é baseado em zero e tem suporte para compatibilidade com backward. Em vez disso, o novo conteúdo deve usar o atributo [**WM/TrackNumber.**](wm-tracknumber.md)

## <a name="global-constant"></a>Constante global

g \_ wszWMTrack

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

Muitos aplicativos existentes escrevem o valor **para WM/Track** como **um DWORD.** Se você criar um aplicativo que reproduz arquivos de fontes desconhecidas, deverá incluir código para manipular valores de cadeia de caracteres e **DWORD.**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




