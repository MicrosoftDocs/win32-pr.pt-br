---
title: Visão geral do eco de exemplo
description: Visão geral do eco de exemplo
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Plug-ins do Windows Media Player, visão geral do eco de exemplo
- plug-ins, visão geral do eco de exemplo
- plug-ins de processamento de sinal digital, visão geral do eco de exemplo
- Plug-ins do DSP, visão geral do eco de exemplo
- Exemplo de plug-in do eco DSP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811117"
---
# <a name="echo-sample-overview"></a>Visão geral do eco de exemplo

Este guia cria um plug-in de DSP do Windows Media Player que cria um efeito de eco no áudio PCM durante a reprodução. As metas para o plug-in são as seguintes:

-   O plug-in processa apenas áudio PCM de 8 ou 16 bits.
-   Ele dá suporte a um tempo de atraso entre 10 milissegundos (MS) e 2000 MS (2 segundos). Isso representa um intervalo prático para a maioria dos aplicativos.
-   Ele dá suporte à combinação do sinal original com o sinal de atraso.
-   Ele fornece uma implementação de página de propriedades que permite ao usuário fornecer um valor para o tempo de atraso e um valor para a porcentagem de sinal de atraso em relação ao nível de sinal de áudio geral.
-   O código é criado modificando o exemplo de plug-in do assistente de plug-in do DSP do Windows Media Player.

O exemplo de eco não está incluído no SDK do Windows Media Player; é um exemplo que você cria. Para criar o exemplo de eco, você deve começar com o projeto padrão do assistente de plug-in do Windows Media Player. Você pode nomear o projeto como desejar; Esta documentação pressupõe que o projeto é denominado Echo. Para obter detalhes sobre como usar o assistente, consulte [criando um plug-in do DSP](building-a-dsp-plug-in.md).

A seção a seguir fornece uma visão geral de como o exemplo cria um efeito de eco:

-   [Como funciona o exemplo de eco](how-the-echo-sample-works.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de eco**](the-echo-sample.md)
</dt> </dl>

 

 




