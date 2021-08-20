---
title: Player. PlayState
description: a propriedade playstate recupera um valor que indica o estado da operação de Windows Media Player.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Windows Media Player Player. PlayState
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0241f8ab538e985a64835065e1eb6bca0a831164cd66fbb7d9166724a72680e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835115"
---
# <a name="playerplaystate"></a>Player. PlayState

a propriedade **playstate** recupera um valor que indica o estado da operação de Windows Media Player.

## <a name="syntax"></a>Syntax

*Player* . **PlayState**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**). A constante de enumeração de estilo C pode ser derivada pela prefixação do valor de estado com "wmpps". Por exemplo, a constante para o estado de execução é **wmppsPlaying**.



| Valor | Estado         | Descrição                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | Indefinido     | Windows Media Player está em um estado indefinido.                                                                              |
| 1     | Parado       | A reprodução do item de mídia atual foi interrompida.                                                                              |
| 2     | Em Pausa        | A reprodução do item de mídia atual está em pausa. Quando um item de mídia é pausado, retomar a reprodução começa no mesmo local. |
| 3     | Reproduzindo       | O item de mídia atual está sendo reproduzido.                                                                                          |
| 4     | ScanForward   | O item de mídia atual é encaminhamento rápido.                                                                                  |
| 5     | ScanReverse   | O item de mídia atual é rebobinado rápido.                                                                                   |
| 6     | de resposta     | O item de mídia atual está obtendo dados adicionais do servidor.                                                          |
| 7     | Aguardando       | A conexão é estabelecida, mas o servidor não está enviando dados. Aguardando a sessão começar.                                |
| 8     | MediaEnded    | O item de mídia concluiu a reprodução.                                                                                          |
| 9     | Transição | Preparando novo item de mídia.                                                                                                   |
| 10    | Ready         | Pronto para começar a jogar.                                                                                                     |
| 11    | Reconexão  | Reconectando ao fluxo.                                                                                                     |



 

## <a name="remarks"></a>Comentários

não há garantia de que os estados de Windows Media Player ocorram em uma ordem específica. Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos. Você não deve escrever código que dependa da ordem de estado.

## <a name="examples"></a>Exemplos

o código de JScript a seguir mostra o uso do *player*. Propriedade **PlayState** . Um elemento de texto HTML, chamado "MyText", exibe o status atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> </dl>

 

 





