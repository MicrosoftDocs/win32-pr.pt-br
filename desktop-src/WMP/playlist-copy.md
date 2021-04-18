---
title: PLAYLIST. Copy
description: O método Copy inicia uma operação de cópia do CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- PLAYLIST. Copy Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765641"
---
# <a name="playlistcopy"></a>PLAYLIST. Copy

O método **Copy** inicia uma operação de cópia do CD.

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método copia apenas os itens marcados na lista de reprodução e funciona da mesma maneira que no painel **Copiar do CD** no modo completo do Windows Media Player. Para que esse método funcione, um CD deve estar na unidade de CD. Defina o atributo **checkboxesVisible** como true para permitir que os usuários selecionem itens individuais em um CD antes de copiar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**PLAYLIST. cópia**](playlist-copying.md)
</dt> </dl>

 

 





