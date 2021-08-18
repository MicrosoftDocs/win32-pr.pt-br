---
description: Um efeito de áudio é um objeto que recebe dados de áudio de entrada e executa alguma operação nos dados antes de passá-los. Você pode usar um efeito para executar uma variedade de tarefas, incluindo adicionar o reverb a um fluxo de áudio e monitorar os níveis de volume de pico.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: Efeitos de áudio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886edb81718f772f7dec31f799b1612ca701c2327468ad554fe80a17c1f69ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082850"
---
# <a name="xaudio2-audio-effects"></a>Efeitos de áudio XAudio2

Um efeito de áudio é um objeto que recebe dados de áudio de entrada e executa alguma operação nos dados antes de passá-los. Você pode usar um efeito para executar uma variedade de tarefas, incluindo adicionar o reverb a um fluxo de áudio e monitorar os níveis de volume de pico.

## <a name="effect-chains"></a>Cadeias de efeito

Qualquer voz XAudio2 pode hospedar uma cadeia de efeitos de áudio. Você pode usar uma matriz de estruturas [**XAUDIO2 \_ EFFECT \_ DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) para especificar cadeias de efeito. Cada descritor contém um ponteiro para um objeto de efeito fornecido pelo cliente. Esses objetos devem implementar as interfaces do APO (Objeto de Processamento de Áudio). Consulte a [Visão geral do XAPO](xapo-overview.md) para obter mais informações sobre o modelo de APO.

Cadeias de efeito podem ser modificadas pelo cliente dinamicamente (enquanto o mecanismo XAudio2 está em execução), os efeitos podem ser habilitados ou desabilitados individualmente e os parâmetros de efeito podem ser alterados, tudo sem nenhuma interrupção do áudio. Sempre que qualquer aspecto do grafo de efeito mudar, o XAudio2 otimizará o grafo novamente para evitar o processamento desnecessário. Consulte [**IXAudio2Voice::SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)e [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Depois que um efeito é anexado a uma voz XAudio2, o XAudio2 assume o controle do efeito e o cliente não deve fazer nenhuma chamada a ela. A maneira mais simples de garantir isso é liberar todos os ponteiros para o efeito.

Os efeitos na cadeia de efeito de uma determinada voz XAudio2 devem consumir e produzir áudio de ponto flutuante na taxa de amostra de processamento dessa voz. O único aspecto do formato de áudio que eles podem alterar é a contagem de canais (por exemplo, um efeito reverb pode converter dados mono em 5.1). O cliente pode usar o [**DESCRITOR DE EFEITO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor).**Campo OutputChannels** para especificar o número de canais que cada efeito deve produzir. A cadeia de efeito falhará se qualquer um dos efeitos não puder atender a esses requisitos ou se um efeito produzir vários canais que o próximo efeito não poderá manipular. Qualquer [**chamada IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) ou [**IXAudio2Voice::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) que faz com que a cadeia de efeitos pare de atender a esses requisitos falhará.

As interfaces APO usadas no XAudio2 devem ser *destrutivas.* Isso significa que eles sempre substituim todos os dados que encontram em seus buffers de saída. Caso contrário, o áudio resultante poderá estar incorreto porque XAudio2 não garante que esses buffers foram inicializados anteriormente com silêncio.

## <a name="xaudio2-built-in-effects"></a>Efeitos integrados do XAudio2

A tabela a seguir lista o conjunto de efeitos de áudio integrados fornecidos pelo XAudio2 e seus métodos de criação. 

| Efeito       | Método de criação                                              |
|--------------|--------------------------------------------------------------|
| Reverb       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Medidor de Volume | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Para ver um exemplo de criação e uso de uma instância de um efeito de áudio, consulte [Como criar uma cadeia de efeitos](how-to--create-an-effect-chain.md).

## <a name="custom-effects-in-xaudio2"></a>Efeitos personalizados no XAudio2

A API [XAPO](xapo-overview.md) fornece uma estrutura para criar efeitos de áudio personalizados que você pode usar no XAudio2. Para ver um exemplo de criação de um efeito personalizado com o XAPO, consulte [Como criar um XAPO.](how-to--create-an-xapo.md)

## <a name="xapo-effect-library-xapofx"></a>Biblioteca de Efeito XAPO (XAPOFX)

[O XAPOFX](xapofx-overview.md) fornece uma biblioteca adicional de XAPOs e um mecanismo comum para sua criação. Para ver um exemplo de como usar XAPOFX com XAudio2, consulte [Como usar XAPOFX no XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> </dl>

 

 
