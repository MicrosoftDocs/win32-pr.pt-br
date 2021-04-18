---
title: Atributo WM/ProtectionType
description: O atributo WM/ProtectionType é o tipo de proteção usado no conteúdo.
ms.assetid: aab36b57-5b4e-4a3f-80cf-872ec8369c49
keywords:
- Atributo WM/ProtectionType Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProtectionType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bf2b9c4700cb45ca5daf2c7d9290456beefbf1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810866"
---
# <a name="wmprotectiontype-attribute"></a>Atributo WM/ProtectionType

O atributo **WM/ProtectionType** é o tipo de proteção usado no conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**ProtectionType** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMProtectionType.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





