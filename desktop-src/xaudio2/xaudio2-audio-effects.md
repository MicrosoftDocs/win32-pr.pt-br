---
description: Um efeito de áudio é um objeto que usa dados de áudio de entrada e executa alguma operação nos dados antes de passá-los. Você pode usar um efeito para executar uma variedade de tarefas, incluindo adicionar reverberação a um fluxo de áudio e monitorar os níveis de volume de pico.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: Efeitos de áudio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8de87a65ea4321b5e8d73a837f79a3e56e8e3a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772731"
---
# <a name="xaudio2-audio-effects"></a>Efeitos de áudio XAudio2

Um efeito de áudio é um objeto que usa dados de áudio de entrada e executa alguma operação nos dados antes de passá-los. Você pode usar um efeito para executar uma variedade de tarefas, incluindo adicionar reverberação a um fluxo de áudio e monitorar os níveis de volume de pico.

## <a name="effect-chains"></a>Cadeias de efeito

Qualquer voz XAudio2 pode hospedar uma cadeia de efeitos de áudio. Você pode usar uma matriz de estruturas de [**\_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) para especificar cadeias de efeito. Cada descritor contém um ponteiro para um objeto de efeito fornecido pelo cliente. Esses objetos devem implementar as interfaces do objeto de processamento de áudio (APO). Consulte a [visão geral do XAPO](xapo-overview.md) para obter mais informações sobre o modelo APO.

Cadeias de efeitos podem ser modificadas dinamicamente pelo cliente (enquanto o mecanismo XAudio2 está em execução), os efeitos podem ser habilitados ou desabilitados individualmente, e os parâmetros de efeito podem ser alterados, tudo isso sem qualquer interrupção do áudio. Sempre que qualquer aspecto do efeito do gráfico é alterado, o XAudio2 otimiza o grafo novamente para evitar o processamento desnecessário. Consulte [**IXAudio2Voice:: SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice:: EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)e [**IXAudio2Voice:: seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Depois que um efeito é anexado a uma voz do XAudio2, o XAudio2 assume o controle do efeito e o cliente não deve fazer mais nenhuma chamada a ele. A maneira mais simples de garantir isso é liberar todos os ponteiros para o efeito.

Os efeitos em uma cadeia de efeitos de uma voz XAudio2 específica devem consumir e produzir áudio de ponto flutuante na taxa de amostragem de processamento dessa voz. O único aspecto do formato de áudio que eles podem alterar é a contagem de canais (por exemplo, um efeito de reverberação pode converter dados mono em 5,1). O cliente pode usar o [**\_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor).**Campo OutputChannels** para especificar o número de canais que cada efeito deve produzir. A cadeia de efeitos falhará se qualquer um dos efeitos não puder atender a esses requisitos, ou se um efeito produzir vários canais que o próximo efeito não possa manipular. Qualquer [**IXAudio2Voice:: EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) ou [**IXAudio2Voice::D isableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) chamadas que fazem com que a cadeia de efeitos pare de atender a esses requisitos falharão.

As interfaces APO usadas em XAudio2 devem ser *destrutivas*. Isso significa que eles sempre substituem os dados encontrados em seus buffers de saída. Caso contrário, o áudio resultante pode estar incorreto porque XAudio2 não garante que esses buffers tenham sido inicializados anteriormente com silêncio.

## <a name="xaudio2-built-in-effects"></a>XAudio2 efeitos internos

A tabela a seguir lista o conjunto de efeitos de áudio internos fornecidos pelo XAudio2 e seus métodos de criação. 

| Efeito       | Método de criação                                              |
|--------------|--------------------------------------------------------------|
| Reverberação       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Medidor de volume | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Para obter um exemplo de como criar e usar uma instância de um efeito de áudio, consulte [como: criar uma cadeia de efeito](how-to--create-an-effect-chain.md).

## <a name="custom-effects-in-xaudio2"></a>Efeitos personalizados em XAudio2

A API [XAPO](xapo-overview.md) fornece uma estrutura para a criação de efeitos de áudio personalizados que você pode usar em XAudio2. Para obter um exemplo de como criar um efeito personalizado com XAPO, consulte [como: criar um XAPO](how-to--create-an-xapo.md).

## <a name="xapo-effect-library-xapofx"></a>XAPOFX (XAPO Effect Library)

O [xapofx](xapofx-overview.md) fornece uma biblioteca adicional de XAPOs e mecanismos comuns para criá-los. Para obter um exemplo de como usar XAPOFX com XAudio2, consulte [como: usar xapofx no XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> </dl>

 

 
