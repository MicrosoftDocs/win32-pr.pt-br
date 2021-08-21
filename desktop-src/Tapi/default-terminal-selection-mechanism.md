---
description: O conceito de terminal multitrack torna ainda mais desejável para a TAPI fornecer um método simplificado para selecionar um terminal em um fluxo ou fluxos. O mecanismo de seleção de terminal padrão foi projetado para resolver isso.
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: Mecanismo de seleção de terminal padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb295c9ea54b0f8572b3ab87f3c8eb9b33ee10773191e3904070c2618b593175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867409"
---
# <a name="default-terminal-selection-mechanism"></a>Mecanismo de seleção de terminal padrão

O conceito de [terminal multitrack](multitrack-terminals.md) torna ainda mais desejável para a TAPI fornecer um método simplificado para selecionar um terminal em um fluxo ou fluxos. O mecanismo de seleção de terminal padrão foi projetado para resolver isso.

## <a name="selecting-a-terminal-on-a-call"></a>Selecionando um terminal em uma chamada

O recurso de seleção de terminal padrão é fornecido por meio da capacidade de selecionar um terminal em uma chamada.

O [objeto de chamada](call-object.md) expõe uma nova interface, [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2). A interface expõe os mesmos métodos que [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), além de três novos métodos: [**RequestTerminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)e [**UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall).

**ITBasicCallControl2:: RequestTerminal** cria um terminal, considerando a classe de terminal, a direção e o tipo de mídia. Ele examina as listas de terminais estáticos e dinâmicos com suporte para localizar e criar o terminal solicitado.

[**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) seleciona o terminal (ou, no caso de um terminal multitrack, enumera, cria se necessário e seleciona os terminais de faixa) no fluxo (ou fluxos) disponíveis na chamada.

O algoritmo para correspondência de fluxos de chamada para o terminal (ou as faixas disponíveis no terminal) é descrito na documentação para [**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).

Chamar [**ITBasicCallControl2:: UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) faz com que o terminal (controle único ou multitrack) seja desmarcado da chamada. Consulte a documentação do método para obter mais detalhes.

## <a name="selecting-a-terminal-on-itstream"></a>Selecionando um terminal no ITStream

Selecionar um terminal de controle único em [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (chamando [**ITStream:: SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)) seleciona o terminal no fluxo. Este é o procedimento de seleção de terminal do TAPI 3 usual.

Somente os terminais de faixas únicas podem ser selecionados em um fluxo. A seleção de um terminal multitrack em um fluxo falhará, pois o fluxo não reconhecerá o tipo de mídia e a direção.

 

 
