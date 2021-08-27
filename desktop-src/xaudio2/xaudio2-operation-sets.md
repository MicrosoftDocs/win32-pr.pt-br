---
description: Esta visão geral apresenta vários métodos XAudio2 que você pode chamar como parte de um conjunto de operações.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Conjuntos de operações XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a7f16edfa461d9944691bc4535debc05f820150dadf746caece85cb68c9f97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089406"
---
# <a name="xaudio2-operation-sets"></a>Conjuntos de operações XAudio2

Esta visão geral apresenta vários métodos XAudio2 que você pode chamar como parte de um conjunto de operações.

Vários métodos XAudio2 levam o *argumento OperationSet,* que permite que eles sejam chamados como parte de um grupo adiado. Em um momento específico, você pode aplicar um conjunto inteiro de alterações simultaneamente chamando a função [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) com o identificador *OperationSet* para esse grupo. O identificador é um número arbitrário. Portanto, ele permite que partes separadas do código do cliente apliquem alterações atômicas separadas ao grafo sem nenhum conflito. A prática recomendada é que o cliente incremente um contador global sempre que precisar gerar um novo identificador *de OperationSet* exclusivo. Um conjunto de alterações no grafo, aplicado atomicamente, tem a garantia de ser preciso em amostra. Por exemplo, as vozes começarão em sincronia.

Se você definir *OperationSet* como XAUDIO2 \_ COMMIT \_ NOW, a alteração será aplicada imediatamente. Ele entra em vigor na primeira passagem de processamento de áudio após a chamada de método. Se você chamar [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) com XAUDIO2 COMMIT ALL, as alterações em todos os conjuntos de operações pendentes serão executadas, independentemente do \_ \_ identificador *operationSet.*

Determinados métodos têm efeito imediatamente quando são chamados de um retorno de chamada XAudio2 com *um OperationSet* de XAUDIO2 \_ COMMIT \_ NOW. Todos os outros métodos que levam um argumento *OperationSet* só tem efeito na próxima passagem de processamento depois que o método é chamado (se chamado com XAUDIO2 COMMIT NOW) ou depois que \_ \_ [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) é chamado com o mesmo *OperationSet*. Por isso, determinadas chamadas de método nem sempre ocorrem na mesma ordem em que foram chamadas.

Todas as operações pendentes são comprometidas atomicamente [**quando IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) é chamado. Todos os métodos que são chamados enquanto o mecanismo é interrompido têm efeito imediatamente, independentemente do *valor operationSet* fornecido. Quando você reinicia o mecanismo, xAudio2 retorna para o modo assíncrono.

Cenários simples nos quais os conjuntos de operações são úteis incluem os exemplos a seguir.

-   Iniciando várias vozes simultaneamente.
-   Enviando simultaneamente um buffer para uma voz, definindo os parâmetros de voz e iniciando a voz.
-   Fazer uma alteração em grande escala no grafo, como conectar todas as vozes de origem a uma nova voz de submix.

Consulte [Como agrupar métodos de áudio como um conjunto de operações](how-to--group-audio-methods-as-an-operation-set.md) para ver um exemplo de como usar um conjunto de operações.

## <a name="operation-set-methods"></a>Métodos de conjunto de operações

Você pode chamar os métodos a seguir como parte de um conjunto de operações.

-   [**IXAudio2SourceVoice::ExitLoop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice::Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Conforme descrito anteriormente, o código do cliente deve, em última análise, chamar a função [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) para executar as alterações adiadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de operações](operation-sets.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Agrupar métodos de áudio como um conjunto de operações](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
