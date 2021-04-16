---
title: THEME. playSound
description: O método playSound reproduz o arquivo de som especificado.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- TEMA. playSound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758090"
---
# <a name="themeplaysound"></a>THEME. playSound

O método **PlaySound** reproduz o arquivo de som especificado.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

Uma **cadeia de caracteres** que especifica o nome do arquivo de som a ser reproduzido.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método permite que você adicione efeitos sonoros a uma capa, por exemplo, quando os botões são clicados. O som é reproduzido pelo sistema operacional diretamente e não pelo Windows Media Player. Isso significa que o som não pode ser controlado com as configurações e métodos do Windows Media Player, mas pode ser reproduzido enquanto o Windows Media Player está reproduzindo outro arquivo de mídia digital.

Esse método oferece suporte apenas a arquivos WAV.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





