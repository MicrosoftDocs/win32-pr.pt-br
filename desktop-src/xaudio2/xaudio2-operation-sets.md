---
description: Esta visão geral apresenta vários métodos XAudio2 que você pode chamar como parte de um conjunto de operações.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Conjuntos de operações XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172041"
---
# <a name="xaudio2-operation-sets"></a>Conjuntos de operações XAudio2

Esta visão geral apresenta vários métodos XAudio2 que você pode chamar como parte de um conjunto de operações.

Vários métodos XAudio2 usam o argumento *operationset* , que permite que eles sejam chamados como parte de um grupo adiado. Em um momento específico, você pode aplicar um conjunto inteiro de alterações simultaneamente chamando a função [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) com o identificador *operationset* para esse grupo. O identificador é um número arbitrário. Assim, ele permite que partes separadas do código do cliente apliquem alterações atômicas separadas ao grafo sem qualquer conflito. A prática recomendada é para o cliente incrementar um contador global sempre que precisar gerar um novo identificador *operationset* exclusivo. Um conjunto de alterações no grafo, aplicado atomicamente, tem a garantia de ser preciso de exemplo. Por exemplo, as vozes serão iniciadas em sincronia.

Se você definir *operationset* como XAudio2 \_ Commit \_ agora, a alteração se aplicará imediatamente. Ela entra em vigor no primeiro passo de processamento de áudio após a chamada do método. Se você chamar [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) com XAudio2 \_ Commit \_ All, as alterações em todos os conjuntos de operações pendentes serão executadas, independentemente do seu identificador *operationset* .

Determinados métodos entram em vigor imediatamente quando são chamados de um retorno de chamada XAudio2 com um *operationset* de XAudio2 \_ Commit \_ Now. Todos os outros métodos que usam um argumento *operationset* só entrarão em vigor na próxima passagem de processamento depois que o método for chamado (se chamado com XAudio2 \_ Commit \_ Now), ou após [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) ser chamado com o mesmo *operationset*. Por isso, determinadas chamadas de método nem sempre podem ocorrer na mesma ordem em que foram chamadas.

Todas as operações pendentes são confirmadas atomicamente quando [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) é chamado. Todos os métodos que são chamados enquanto o mecanismo é interrompido entram em vigor imediatamente, independentemente do valor de *operationset* fornecido. Quando você reinicia o mecanismo, XAudio2 retorna para o modo assíncrono.

Cenários simples nos quais os conjuntos de operações são úteis incluem os exemplos a seguir.

-   Iniciando várias vozes simultaneamente.
-   Enviando simultaneamente um buffer para uma voz, definindo os parâmetros de voz e iniciando a voz.
-   Fazer uma alteração em larga escala no grafo, como conectar todas as vozes de origem a uma nova voz submix.

Consulte [como agrupar métodos de áudio como uma operação definida](how-to--group-audio-methods-as-an-operation-set.md) para obter um exemplo de como usar um conjunto de operações.

## <a name="operation-set-methods"></a>Métodos de conjunto de operações

Você pode chamar os seguintes métodos como parte de um conjunto de operações.

-   [**IXAudio2SourceVoice:: ExitLoop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice:: seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice:: iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice:: Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Conforme descrito anteriormente, o código do cliente deve, finalmente, chamar a função [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) para executar as alterações adiadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de operações](operation-sets.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Agrupar métodos de áudio como um conjunto de operações](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
