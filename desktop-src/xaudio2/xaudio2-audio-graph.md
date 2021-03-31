---
description: O conjunto de todas as vozes, com seus efeitos contidos e suas interconexões, é conhecido como grafo de processamento de áudio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: Grafo de áudio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172044"
---
# <a name="xaudio2-audio-graph"></a>Grafo de áudio XAudio2

O conjunto de todas as vozes, com seus efeitos contidos e suas interconexões, é conhecido como grafo de processamento de áudio. O grafo usa um conjunto de fluxos de áudio do cliente como entrada, processa-os e entrega o resultado final a um dispositivo de áudio. Todo o processamento de áudio ocorre em um thread separado com uma periodicidade definida pelo Quantum do grafo (atualmente, 10 milissegundos no Microsoft Windows e 5 1/3 milissegundos no Xbox 360). Todos os milissegundos do Quantum, o thread ativa e distribui milissegundos do quantum de dados de áudio por todo o grafo. Para obter um exemplo de criação de um gráfico de áudio básico, consulte como [compilar um grafo básico de processamento de áudio](how-to--build-a-basic-audio-processing-graph.md).

Um grafo de áudio simples:

![um grafo de áudio simples](images/xaudio2-audio-graph.png)

O cliente pode controlar o estado do grafo dinamicamente enquanto ele está em execução. As ações de controle podem incluir adição e remoção de entradas e saídas, alteração dos efeitos internos e interconexões, definição de parâmetros nos efeitos, habilitação e desabilitação de partes do grafo e assim por diante. Para obter um exemplo de alteração dinâmica de um gráfico de áudio, consulte [como: Adicionar ou remover vozes dinamicamente de um grafo de áudio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).

## <a name="processing-the-graph"></a>Processando o grafo

Qualquer chamada de método que afete qualquer objeto no grafo é considerada como efeito uma alteração de estado do grafo. As alterações de estado do grafo incluem o seguinte:

-   Criando e destruindo vozes
-   Iniciando ou parando vozes
-   Alterando os destinos de uma voz
-   Modificando cadeias de efeito
-   Habilitando ou desabilitando efeitos
-   Definindo parâmetros nos efeitos ou na SRCs interna, nos filtros, nos volumes e nos mixers

Qualquer conjunto de alterações de estado do grafo pode ser combinado e executado como uma transação atômica. Essas operações atômicas são conhecidas como conjuntos de operações. Eles são discutidos na visão geral dos [conjuntos de operações do XAudio2](xaudio2-operation-sets.md) .

## <a name="internal-data-representation"></a>Representação de dados interna

Os dados de áudio no grafo XAudio2 são sempre armazenados e processados no formato PCM de ponto flutuante de 32 bits. No entanto, a contagem de canais e a taxa de amostragem podem variar dentro do grafo. O formato no qual uma determinada voz processa o áudio é determinado pelo tipo de voz e pelos parâmetros usados para criar a voz.



| Tipo de voz                                                                                                      | Parâmetros                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | A contagem de canais e a taxa de amostra das vozes para as quais a voz de origem envia áudio.         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | Os argumentos *InputChannels* e *InputSampleRate* usados para criar a voz de submix/mestre. |



 

## <a name="format-conversion"></a>Conversão de formato

XAudio2 lida com qualquer taxa de amostragem ou conversões de canal que são necessárias à medida que o áudio viaja de uma voz para outra, com as seguintes limitações:

-   Todas as vozes de destino de uma determinada voz devem estar em execução com a mesma taxa de amostragem
-   Os efeitos em uma cadeia de efeito podem alterar a contagem de canais do áudio, mas não sua taxa de amostragem
-   A contagem de canais de saída de uma cadeia de efeitos deve corresponder à das vozes às quais ele envia
-   Nenhuma alteração dinâmica de grafo pode ser feita, o que quebraria as regras acima

No lado da entrada, as vozes de origem podem ler dados em qualquer formato PCM válido ou em qualquer um dos formatos compactados com suporte do XAudio2. Se os dados de entrada forem compactados, eles serão decodificados para o PCM de ponto flutuante antes de qualquer processamento adicional ser feito.

No lado da saída, as vozes de dominar só podem produzir dados PCM. Esses dados sempre atenderão às mesmas restrições descritas acima para dados de entrada PCM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gráficos de áudio](audio-graphs.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Como: Adicionar ou remover dinamicamente vozes de um gráfico de áudio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[Como: Usar vozes de submixagem](how-to--use-submix-voices.md)
</dt> <dt>

[Como: Criar uma cadeia de efeitos](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



