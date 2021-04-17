---
title: Método Player. launchURL
description: O método launchURL envia uma URL para o navegador padrão do usuário a ser renderizado. | Método Player. launchURL
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- método launchURL Windows Media Player
- método launchURL Windows Media Player, classe Player
- Classe de jogador Windows Media Player, método launchURL
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
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761795"
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

## <a name="return-value"></a>Retornar valor

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

 

 





