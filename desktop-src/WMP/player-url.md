---
title: Player. URL
description: A propriedade URL especifica ou recupera o nome do item de mídia a ser reproduzido.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player. URL do Windows Media Player
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
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786144"
---
# <a name="playerurl"></a>Player. URL

A propriedade **URL** especifica ou recupera o nome do item de mídia a ser reproduzido.

## <a name="syntax"></a>Syntax

*Player* . **URL** do

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação sem valor padrão.

## <a name="remarks"></a>Comentários

Essa propriedade só pode ser definida como uma URL em uma zona de segurança que seja a mesma ou menos restritiva do que a zona de segurança do programa de chamada ou da página da Web.

Os aplicativos que abrirem itens de mídia atrás de um firewall terão um desempenho melhor se o endereço for especificado usando o nome DNS (servidor de nomes de domínio) em vez do endereço IP.

Não chame esse método do código do manipulador de eventos. Solicitando *jogador*. A **URL** de um manipulador de eventos pode gerar resultados inesperados.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de entrada de texto HTML e um elemento de entrada de botão HTML. O elemento TEXT permite que o usuário digite um caminho para especificar um arquivo de mídia digital a ser reproduzido. O elemento BUTTON executa o JScript que abre o arquivo e inicia o Windows Media Player. O objeto de **jogador** foi criado com ID = "Player".


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

 

 





