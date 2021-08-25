---
title: THEME. playSound
description: O método playSound reproduz o arquivo de som especificado.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- Windows Media Player de THEME. playSound
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9e6ac0cb7bdf4f8951bafbc89a0a41bf368afcd1021666eb7875739d1cd912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001746"
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

Esse método permite que você adicione efeitos sonoros a uma capa, por exemplo, quando os botões são clicados. O som é reproduzido diretamente pelo sistema operacional e não por Windows Media Player. isso significa que o som não pode ser controlado com Windows Media Player configurações e métodos, mas pode ser reproduzido enquanto Windows Media Player estiver executando outro arquivo de mídia digital.

Esse método oferece suporte apenas a arquivos WAV.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





