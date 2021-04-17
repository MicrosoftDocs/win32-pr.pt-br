---
title: Atributo WM/InitialKey
description: O atributo WM/InitialKey é a chave inicial da música.
ms.assetid: 1458f1a2-3d46-4491-8b89-731276d7c024
keywords:
- Atributo WM/InitialKey do Windows Media Player
topic_type:
- apiref
api_name:
- WM/InitialKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dd4daeabe2971615518b0a3cf37223a4c623c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797988"
---
# <a name="wminitialkey-attribute"></a>Atributo WM/InitialKey

O atributo **WM/InitialKey** é a chave inicial da música.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMInitialKey.

**InitialKey** é um alias para este atributo.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





