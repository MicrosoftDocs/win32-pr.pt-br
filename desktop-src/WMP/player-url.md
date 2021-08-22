---
title: Player. URL
description: A propriedade URL especifica ou recupera o nome do item de mídia a ser reproduzido.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Windows Media Player Player. URL
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00a6513350ee9c39855aba8168faf9ced788a0686a0fdbe845013dcc521142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572035"
---
# <a name="playerurl"></a>Player. URL

A propriedade **URL** especifica ou recupera o nome do item de mídia a ser reproduzido.

## <a name="syntax"></a>Sintaxe

*Player* . **URL** do

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação sem valor padrão.

## <a name="remarks"></a>Comentários

Essa propriedade só pode ser definida como uma URL em uma zona de segurança que seja a mesma ou menos restritiva do que a zona de segurança do programa de chamada ou da página da Web.

Os aplicativos que abrirem itens de mídia atrás de um firewall terão um desempenho melhor se o endereço for especificado usando o nome DNS (servidor de nomes de domínio) em vez do endereço IP.

Não chame esse método do código do manipulador de eventos. Solicitando *jogador*. A **URL** de um manipulador de eventos pode gerar resultados inesperados.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de entrada de texto HTML e um elemento de entrada de botão HTML. O elemento TEXT permite que o usuário digite um caminho para especificar um arquivo de mídia digital a ser reproduzido. o elemento BUTTON executa JScript que abre o arquivo e inicia Windows Media Player. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
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

 

 





