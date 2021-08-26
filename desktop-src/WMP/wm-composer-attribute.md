---
title: atributo do WM/Composer
description: o atributo WM/Composer é o nome do compositor da música.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Windows Media Player de atributo do WM/Composer
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f41e92e1f343ecbd532769560a6d2d555c275e147ab2386ae574c2dea8bc411c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001166"
---
# <a name="wmcomposer-attribute"></a>atributo do WM/Composer

o atributo **WM/Composer** é o nome do compositor da música.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

Esse atributo pode ter vários valores. Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar o método **Media. getItemInfoByType** , não o método **Media. getItemInfo** .

**Composer** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMComposer.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





