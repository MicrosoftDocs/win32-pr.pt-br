---
description: Aprimoramentos na reprodução de DVD no Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Aprimoramentos na reprodução de DVD no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159056d2c7acaec18a73a30b21f79bcd6267ca33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105747368"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Aprimoramentos na reprodução de DVD no Windows Vista

Estas seções descrevem as melhorias na reprodução e na navegação em DVD no Windows Vista.

**Especificando um decodificador**

Em versões anteriores do DirectShow, era difícil especificar um decodificador MPEG-2 específico ao criar um grafo de reprodução de DVD. A partir do Windows Vista, um aplicativo pode especificar o decodificador da seguinte maneira:

1.  Adicione o decodificador ao grafo antes de chamar [**IDvdGraphBuilder:: RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume).
2.  Chame **RenderDvdVideoVolume** e defina o \_ sinalizador am \_ DVD \_ não \_ Clear. O navegador de DVD fornecerá preferência ao decodificador que você adicionou.

**Suporte para o processador de vídeo avançado**

É recomendável que os aplicativos escritos para o Windows Vista ou posterior usem o [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR) para reprodução de vídeo. Para usar o EVR em um aplicativo de reprodução de DVD, defina \_ o \_ sinalizador am DVD EVR \_ somente quando você chamar **RenderDvdVideoVolume**.

Para configurar o EVR antes de criar o grafo, chame [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) e consulte a interface **IEVRFilterConfig** ou **IMFVideoRenderer** . (Essas interfaces estão documentadas na documentação do SDK do Media Foundation.) Para obter mais informações sobre como configurar o processador de vídeo em um grafo de reprodução de DVD, consulte [criando o grafo de filtro de DVD](building-the-dvd-filter-graph.md).

O navegador de DVD não usará o EVR, a menos que o método [**IAMDecoderCaps:: GetDecoderCaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) do decodificador retorne o \_ sinalizador de suporte da consulta GETDECODERCAP am \_ \_ EVR \_ . Esse sinalizador é definido para garantir que os aplicativos sejam compatíveis com os decodificadores existentes. Se **RenderDvdVideoVolume** falhar usando o \_ sinalizador am DVD \_ EVR \_ somente, volte para outro processador de vídeo chamando o método novamente sem o sinalizador.

**Reprodução reversa suave**

O navegador de DVD agora pode executar uma reprodução reversa suave. Na reprodução reversa suave, o DVD Navigator envia as VOBUs (unidades de objeto de vídeo) inteiras para o decodificador e o decodificador emite os quadros na ordem inversa. Esse recurso requer que os decodificadores ofereçam suporte à reprodução reversa suave.

Quando o aplicativo define a velocidade de reprodução como um valor negativo, o navegador de DVD consulta os decodificadores para a propriedade [**\_ \_ ReverseMaxFullDataRate da taxa de am**](am-rate-reversemaxfulldatarate-property.md) . O valor dessa propriedade é o valor absoluto da velocidade de inversa máxima x 10000. Por exemplo, se a velocidade inversa máxima for-2,0, o valor será 20000.

Se o decodificador de vídeo der suporte à propriedade, o navegador de DVD usará a reprodução reversa suave. O fluxo de áudio será reproduzido em ordem inversa se o decodificador de áudio der suporte à propriedade; caso contrário, o fluxo de áudio ficará mudo. Se o decodificador de vídeo não oferecer suporte à propriedade ou se a taxa de reprodução exceder a taxa de inversa máxima do decodificador de vídeo, o navegador de DVD alternará para o *modo de verificação*. No modo de verificação, o navegador de DVD envia apenas quadros I para o decodificador e descarta todos os quadros B e P.

Durante a reprodução reversa suave, o navegador de DVD envia VOBUs completo para o decodificador. O navegador de DVD envia o VOBUs na ordem inversa, mas envia os quadros dentro de cada VOBU em sua ordem de encaminhamento normal. No início de cada VOBU, o navegador de DVD define o \_ sinalizador am ReverseBlockStart no exemplo. No final do VOBU, o navegador de DVD envia um exemplo vazio com o sinalizador AM \_ ReverseBlockEnd. Para recuperar esses sinalizadores, chame [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo. Os sinalizadores são definidos no membro **dwTypeSpecificFlags** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

O decodificador armazena em cache os dados de vídeo até receber o exemplo com o \_ sinalizador am ReverseBlockEnd. Nesse ponto, o decodificador entrega quadros decodificados na ordem inversa. Por exemplo, se VOBU 1 contiver quadros 1 – 4 e VOBU 2 contiver quadros de 5 a 8, o navegador de DVD enviará os quadros nesta ordem:

(Início do bloco) F5 F6 F7 F8 (bloco end) (início do bloco) F1 F2 F3 F4 (bloco end)

O decodificador deve processar os quadros da seguinte maneira:

1.  Decodifique VOBU 2.
2.  Quadros de saída: F8 F7 F6 F5
3.  Decodifique VOBU 1.
4.  Quadros de saída: F4 F3 F2 F1

O navegador de DVD define o carimbo de data/hora no primeiro exemplo no VOBU (F1 e F5 neste exemplo), mas o carimbo de data/hora contém a hora da apresentação do início do bloco, portanto, o decodificador deve aplicar esse tempo à última amostra no bloco (F4 e F8). Os tempos de apresentação aumentam durante a reprodução inversa.

Normalmente, um VOBU contém até 42 quadros e pode conter mais de um grupo de imagens (GOP). Para permitir que todo o VOBU seja decodificado, o decodificador deve armazenar em cache os quadros I e P decodificados. VOBUs em DVDs não são fechados GOPS segundos, portanto, um quadro B em uma GOP pode exigir a decodificação de todos os quadros de referência na GOP anterior. Se o decodificador não tiver superfícies suficientes para conter todos os quadros decodificados, talvez seja necessário decodificar os quadros selecionados.

**Alterações de taxa**

Por padrão, o navegador de DVD libera o grafo entre as alterações de taxa. No entanto, se o decodificador oferecer suporte à propriedade [**\_ \_ ResetOnTimeDisc de taxa am**](am-rate-resetontimedisc-property.md) , o navegador de DVD não liberará o grafo, resultando em uma transição mais suave entre as taxas de reprodução.

O navegador de DVD sempre marca os exemplos de tempo para reprodução na velocidade de 1x, independentemente da velocidade de reprodução real. O decodificador deve dimensionar os carimbos de data/hora nos exemplos decodificados para corresponder à velocidade de reprodução real. (Para obter detalhes, [**consulte \_ Propriedade timerate \_ SimpleRateChange**](am-rate-simpleratechange-property.md).) Como resultado, ao reproduzir em velocidades diferentes de 1x, os carimbos de data/hora nos quadros decodificados divergem dos quadros codificados. Sempre que o navegador de DVD define o sinalizador AM de \_ exemplo \_ TIMEDISCONTINUITY em um exemplo, o decodificador deve ressincronizar seus carimbos de data/hora. Em outras palavras, o quadro decodificado deve ter o mesmo carimbo de data/hora que o quadro de entrada. Para recuperar o \_ sinalizador am Sample \_ TIMEDISCONTINUITY, chame [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo. O sinalizador é definido no membro **dwSampleFlags** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

**Gerenciamento de Energia**

No Windows Vista, o navegador de DVD permite as seguintes melhorias no gerenciamento de energia:

-   Resolução de timer mais alta
-   Cache de dados maior

**Resolução do temporizador**: os aplicativos podem solicitar uma resolução mínima do temporizador chamando a função **timeBeginPeriod** . Uma resolução mais alta (período mais curto) aumenta a capacidade de resposta do sistema para eventos periódicos, como tempos limite, mas também pode aumentar a frequência de alternâncias de contexto de thread.

Por padrão, o relógio de referência no DirectShow define a resolução do temporizador como 1 milissegundo. Nessa resolução, a CPU não irá inserir nenhum modo de economia de energia. A partir do Windows Vista, o navegador de DVD substitui o comportamento padrão do relógio de referência chamando [**IReferenceClockTimerControl:: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) no relógio de referência. Isso remove a solicitação do relógio para uma resolução de temporizador de 1 milissegundo. Isso pode permitir que a CPU entre em um modo de economia de energia.

A resolução do temporizador é uma configuração global; O Windows escolhe o menor valor solicitado. Os filtros de processador de mixagem de vídeo (VMR) (VMR-7 e VMR-9) definem a resolução do temporizador como 1 milissegundo. O EVR normalmente define a resolução para um valor entre 4 e 8 milissegundos, dependendo se a composição de área de trabalho está habilitada e se o EVR está no modo de tela inteira. Outros aplicativos também podem definir a resolução.

**Tamanho do cache**: os aplicativos podem especificar a quantidade de dados que o navegador de DVD armazena definindo a \_ opção DVD CacheSizeInMB no método [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) . Se o aplicativo definir esse sinalizador como um valor grande (> 50 MB), a unidade de DVD poderá ser desativada após a pré-busca inicial, dependendo do hardware, o que pode reduzir o consumo de energia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



