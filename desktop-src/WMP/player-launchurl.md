---
title: Método Player. launchURL
description: O método launchURL envia uma URL para o navegador padrão do usuário a ser renderizado. | Método Player. launchURL
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- Windows Media Player do método launchURL
- método launchURL Windows Media Player, classe Player
- classe de jogador Windows Media Player, método launchURL
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d22c65a29aaee9c849677dfa42acb5769bf30d2fb7079e305ee79632ef22e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134819"
---
# <a name="playerlaunchurl-method"></a>Método Player. launchURL

O método **launchURL** envia uma URL para o navegador padrão do usuário a ser renderizado.

## <a name="syntax"></a>Sintaxe


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*URL* \[ do no\]
</dt> <dd>

Valor da **cadeia de caracteres** que representa a URL a ser iniciada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método abre apenas as páginas da Web usando os protocolos HTTP ou HTTPS.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que, quando clicado, exibe o site da Microsoft em uma nova janela do navegador. O elemento **Player** foi criado com ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





