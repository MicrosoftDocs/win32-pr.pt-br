---
description: Aprimoramentos de reprodução de DVD no Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Aprimoramentos de reprodução de DVD no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5757f5dd73dc547ae123490fd8de84b0606d1ade8490c9600486df0b846541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148709"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Aprimoramentos de reprodução de DVD no Windows Vista

Esta seção descreve as melhorias na reprodução e navegação de DVD no Windows Vista.

**Especificando um decodificador**

Em versões anteriores do DirectShow, era difícil especificar um decodificador MPEG-2 específico ao criar um grafo de reprodução de DVD. Começando no Windows Vista, um aplicativo pode especificar o decodificador da seguinte forma:

1.  Adicione o decodificador ao grafo antes de chamar [**IDvdGraphBuilder::RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume).
2.  Chame **RenderDvdVideoVolume e** de definido o sinalizador \_ AM DVD NÃO \_ \_ \_ LIMPAR. O Navegador de DVD dará preferência ao decodificador que você adicionou.

**Suporte para o renderador de vídeo aprimorado**

É recomendável que os aplicativos escritos para [](enhanced-video-renderer-filter.md) Windows Vista ou posterior usem o EVR (Renderização de Vídeo Aprimorado) para reprodução de vídeo. Para usar o EVR em um aplicativo de reprodução de DVD, de definir o sinalizador AM DVD EVR ONLY quando você chamar \_ \_ \_ **RenderDvdVideoVolume**.

Para configurar o EVR antes de criar o grafo, chame [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) e consulte a interface **IEVRFilterConfig** ou **IMFVideoRenderer.** (Essas interfaces estão documentadas na documentação Media Foundation do SDK.) Para obter mais informações sobre como configurar o renderador de vídeo em um grafo de reprodução de DVD, consulte Criando o [filtro de DVD](building-the-dvd-filter-graph.md)Graph .

O Navegador de DVD não usará o EVR, a menos que o método [**IAMDecoderCaps::GetDecoderCaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) do decodificador retorne o sinalizador AM \_ GETDECODERCAP \_ QUERY \_ EVR \_ SUPPORT. Esse sinalizador é definido para garantir que os aplicativos sejam compatíveis com decodificadores existentes. Se **RenderDvdVideoVolume** falhar usando o sinalizador AM \_ DVD \_ EVR ONLY, faça fall back para outro renderador de vídeo chamando o método novamente sem \_ o sinalizador .

**Reprodução reverso suave**

O Navegador de DVD agora pode executar a reprodução reverso suave. Na reprodução reverso suave, o Navegador de DVD envia VOBUs (unidades de objeto de vídeo) inteiras para o decodificador e o decodificador emite os quadros na ordem inversa. Esse recurso requer que os decodificadores deem suporte à reprodução reverso suave.

Quando o aplicativo define a velocidade de reprodução como um valor negativo, o Navegador de DVD consulta os decodificadores para a [**propriedade \_ \_ ReverseMaxFullDataRate AM RATE.**](am-rate-reversemaxfulldatarate-property.md) O valor dessa propriedade é o valor absoluto da velocidade inversa máxima x 10000. Por exemplo, se a velocidade inversa máxima for -2,0, o valor será 20000.

Se o decodificador de vídeo for compatível com a propriedade , o Navegador de DVD usará reprodução reverso suave. O fluxo de áudio será interpretado em ordem inversa se o decodificador de áudio for compatível com a propriedade ; caso contrário, o fluxo de áudio será mudo. Se o decodificador de vídeo não dá suporte à propriedade ou a taxa de reprodução excede a taxa inversa máxima do decodificador de vídeo, o Navegador de DVD alterna para o modo *de verificação*. No modo de verificação, o Navegador de DVD envia apenas quadros I para o decodificador e descarta todos os quadros B e P.

Durante a reprodução reverso suave, o Navegador de DVD envia VOBUs completas para o decodificador. O Navegador de DVD envia as VOBUs em ordem inversa, mas envia os quadros dentro de cada VOBU em sua ordem de encaminhamento normal. No início de cada VOBU, o Navegador de DVD define o sinalizador \_ ReverseBlockStart am no exemplo. No final do VOBU, o Navegador de DVD envia um exemplo vazio com o sinalizador \_ REVERSEBlockEnd am. Para recuperar esses sinalizadores, chame [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo. Os sinalizadores são definidos no **membro dwTypeSpecificFlags** da [**estrutura AM \_ SAMPLE2 \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

O decodificador armazena em cache os dados de vídeo até receber o exemplo com o sinalizador \_ REVERSEBlockEnd am. Nesse ponto, o decodificador fornece quadros decodificados em ordem inversa. Por exemplo, se o VOBU 1 contiver quadros 1 a 4 e VOBU 2 contiver quadros de 5 a 8, o Navegador de DVD enviará os quadros nesta ordem:

(Bloquear início) F5 F6 F7 F8 (final do bloco) (início do bloco) F1 F2 F3 F4 (final do bloco)

O decodificador deve processar os quadros da seguinte forma:

1.  Decodificar VOBU 2.
2.  Quadros de saída: F8 F7 F6 F5
3.  Decodificar VOBU 1.
4.  Quadros de saída: F4 F3 F2 F1

O Navegador de DVD define o carimbo de data/hora no primeiro exemplo no VOBU (F1 e F5 neste exemplo), mas o carimbo de data/hora contém a hora de apresentação do início do bloco, portanto, o decodificador deve aplicar esse tempo ao último exemplo no bloco (F4 e F8). Os tempos de apresentação aumentam durante a reprodução inversa.

Normalmente, um VOBU contém até 42 quadros e pode conter mais de um grupo de imagens (GOP). Para permitir que todo o VOBU seja decodificador, o decodificador deve armazenar em cache os quadros I e P decodificados. VOBUs em DVDs não são GOPs fechados, portanto, um quadro B em um GOP pode exigir a decodificação de todos os quadros de referência no GOP anterior. Se o decodificador não tiver superfícies suficientes para manter todos os quadros decodificados, talvez seja necessário decodificar os quadros selecionados.

**Alterações de taxa**

Por padrão, o Navegador de DVD libera o grafo entre as alterações de taxa. Se o decodificador for compatível com a propriedade [**AM \_ RATE \_ ResetOnTimeDisc,**](am-rate-resetontimedisc-property.md) no entanto, o Navegador de DVD não liberará o grafo, resultando em uma transição mais suave entre as taxas de reprodução.

O Navegador de DVD sempre marca os carimbos de data/hora para reprodução em velocidade 1x, independentemente da velocidade real de reprodução. O decodificador deve dimensionar os carimbos de data/hora nos exemplos decodificados para corresponder à velocidade de reprodução real. (Para obter detalhes, consulte [**Propriedade AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md).) Como resultado, ao tocar em velocidades que não 1x, os carimbos de data/hora nos quadros decodificados divergem daqueles nos quadros codificados. Sempre que o Navegador de DVD define o sinalizador AM SAMPLE TIMEDISCONTINUITY em um exemplo, o \_ \_ decodificador deve ressincronizar seus carimbos de data/hora. Em outras palavras, o quadro decodificado deve ter o mesmo carimbo de data/hora que o quadro de entrada. Para recuperar o sinalizador AM \_ \_ SAMPLE TIMEDISCONTINUITY, chame [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo. O sinalizador é definido no **membro dwSampleFlags** da estrutura [**AM \_ SAMPLE2 \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

**Gerenciamento de Energia**

No Windows Vista, o Navegador de DVD permite as seguintes melhorias no gerenciamento de energia:

-   Resolução de temporizador mais alta
-   Cache de dados maior

**Resolução de temporizador:** os aplicativos podem solicitar uma resolução mínima de temporizador chamando a **função timeBeginPeriod.** Uma resolução mais alta (período mais curto) aumenta a capacidade de resposta do sistema para eventos periódicos, como tempos-máximos, mas também pode aumentar a frequência de comutadores de contexto de thread.

Por padrão, o relógio de referência DirectShow a resolução do temporizador como 1 milissegundo. Nessa resolução, a CPU não entrará em nenhum modo de economia de energia. A partir do Windows Vista, o Navegador de DVD substitui o comportamento padrão do relógio de referência chamando [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) no relógio de referência. Isso remove a solicitação do relógio para uma resolução de temporizador de 1 milissegundo. Isso pode permitir que a CPU entre em um modo de economia de energia.

A resolução do temporizador é uma configuração global; Windows escolhe o menor valor solicitado. Os filtros VMR (Video Mixing Renderer) (VMR-7 e VMR-9) definirão a resolução do temporizador como 1 milissegundo. A EVR normalmente define a resolução como um valor entre 4 e 8 milissegundos, dependendo se a composição da área de trabalho está habilitada e se o EVR está no modo de tela inteira. Outros aplicativos também podem definir a resolução.

**Tamanho do** cache: os aplicativos podem especificar quantos dados o Navegador de DVD armazena em cache definindo a opção \_ CACHESizeInMB do DVD no método [**IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) Se o aplicativo define esse sinalizador como um valor grande (> 50 MB), a unidade de DVD pode girar para baixo após a pré-busca inicial, dependendo do hardware, o que pode reduzir o consumo de energia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



