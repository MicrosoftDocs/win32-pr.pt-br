---
description: Relógio de apresentação
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: Relógio de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61ad02537a2591c681db78721376651f7854ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091041"
---
# <a name="presentation-clock"></a>Relógio de apresentação

O *relógio de apresentação* é um objeto que gera a hora do relógio de uma apresentação. A hora relatada pelo relógio de apresentação é chamada de *hora de apresentação*. Todos os fluxos em uma apresentação são sincronizados com a hora da apresentação. O relógio de apresentação expõe as interfaces a seguir.



| Interface                                            | Descrição                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | Interface primária para usar o relógio de apresentação. |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | Controla a taxa de clock.                            |
| [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | Fornece um retorno de chamada do temporizador.                          |
| [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | Desliga o relógio de apresentação.                  |



 

Os coletores de mídia usam o tempo de apresentação para agendar quando renderizar exemplos. Sempre que um coletor de mídia recebe um novo exemplo, ele obtém o carimbo de data/hora do exemplo e renderiza o exemplo no horário indicado, ou o mais próximo possível do tempo possível. Como todos os coletores de mídia em uma topologia compartilham o mesmo relógio de apresentação, vários fluxos (como áudio e vídeo) são sincronizados. As fontes de mídia e as transformações não usam o relógio de apresentação, pois não agendam quando fornecer amostras. Em vez disso, eles produzem amostras sempre que o pipeline solicita um novo exemplo.

Se você estiver usando a sessão de mídia para reprodução, a sessão de mídia manipulará todos os detalhes da criação do relógio de apresentação, selecionando uma fonte de tempo e notificando os coletores de mídia. Seu aplicativo pode usar o relógio de apresentação para obter o tempo de apresentação atual durante a reprodução, mas, caso contrário, não chamará nenhum método no relógio de apresentação.

## <a name="clock-time-and-clock-states"></a>Hora do relógio e Estados do relógio

Para obter a hora do relógio mais recente do relógio de apresentação, chame [**IMFPresentationClock:: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime). Os horários de relógio estão sempre em unidades de 100 nanossegundos e, portanto, um segundo é de 10 milhões (10 ^ 7) tiques. Isso corresponde a uma frequência de 10 MHz.

O relógio de apresentação tem três Estados: em execução, em pausa e parado.

-   Para executar o relógio, chame [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start). O método **Start** especifica a hora de início do relógio. Enquanto o relógio estiver em execução, a hora do relógio será incrementada a partir da hora de início, na taxa de relógio atual.
-   Para pausar o relógio, chame [**IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause). Enquanto o relógio está pausado, a hora do relógio não avança e [**getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) retorna a hora em que o relógio foi pausado.
-   Para parar o relógio, chame [**IMFPresentationClock:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop). Quando o relógio é interrompido, a hora do relógio não avança e [**getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) retorna zero.

Por padrão, o relógio avança a uma taxa de 1,0, significando 1 tique por 100 nanossegundos. Para alterar a taxa na qual o relógio avança, consulte o relógio de apresentação para a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) e chame [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).

Os objetos podem receber notificações de alterações de estado (incluindo alterações de taxa) do relógio de apresentação. Para receber notificações, implemente a interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) e chame [**IMFPresentationClock:: AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) no relógio de apresentação. Antes de desligar, chame [**IMFPresentationClock:: RemoveClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) para cancelar o registro do objeto. Os coletores de mídia usam esse mecanismo para receber notificações do relógio.

## <a name="presentation-times"></a>Tempos de apresentação

Um coletor de mídia tenta agendar cada exemplo para que o exemplo seja renderizado no horário correto ou o mais próximo possível do tempo correto. As seguintes definições se aplicam:

-   *Hora da apresentação.* A hora em que uma amostra deve ser renderizada. O tempo é fornecido em unidades de 100 nanossegundos.
-   *Tempo de mídia.* Tempo relativo ao início do conteúdo. Por exemplo, se um arquivo de vídeo tiver 10 segundos de comprimento, a metade do ponto no arquivo terá um tempo de mídia de 5 segundos.
-   *Carimbo de data/hora.* O tempo marcado em um exemplo de mídia. Para obter o carimbo de data/hora, chame [**IMFSample:: Getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime). Quando uma origem de mídia produz um exemplo, ela define o carimbo de data/hora igual ao tempo de mídia. A sessão de mídia converte o carimbo de data/hora em tempo de apresentação.

Por padrão, a hora de mídia e a hora da apresentação são as mesmas, por exemplo, se um quadro de vídeo aparecer 5 segundos no arquivo de origem, o tempo de mídia e a hora da apresentação serão ambos 5 segundos. Se você estiver usando a [origem do Sequencer](sequencer-source.md), o modelo de tempo será um pouco mais complicado para permitir transições suaves entre os segmentos. Para obter mais informações sobre o modelo de tempo da origem do Sequencer, consulte [tempos de apresentação da sequência](sequence-presentation-times.md).

A origem da mídia sempre define o carimbo de data/hora igual ao horário da mídia. Se o tempo de apresentação não estiver alinhado com o tempo de mídia, a sessão de mídia converterá os carimbos de data/hora nos exemplos de mídia. No momento em que o coletor recebe um exemplo, o carimbo de data/hora do exemplo foi convertido em tempo de apresentação. O coletor agenda o exemplo na hora atual do relógio de apresentação. (Coletores sem tarifas são uma exceção, pois eles ignoram o relógio de apresentação.)

Se o aplicativo procurar uma nova posição, a sessão de mídia reiniciará o relógio de apresentação no tempo de busca especificado. Por exemplo, se o aplicativo busca a posição de 5 segundos no arquivo, a sessão de mídia inicia o relógio em 5 segundos. A origem da mídia pode fornecer amostras com um carimbo de data/hora ligeiramente anterior se o tempo de busca não cair em um limite de quadro de chave. Isso é necessário para que os decodificadores possam decodificar todos os quadros. A sessão de mídia descarta ou corta amostras antes que elas atinjam os coletores de mídia, a fim de corresponder ao tempo de busca solicitado. Por exemplo, se o tempo de busca for de 5 segundos, o primeiro exemplo de áudio poderá começar em 4,5 segundos. A sessão de mídia irá cortar os primeiros 0,5 segundos do primeiro exemplo de áudio decodificado.

## <a name="creating-the-presentation-clock"></a>Criando o relógio de apresentação

Para criar o relógio de apresentação, chame [**MFCreatePresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock). Para desligar o relógio, consulte a interface [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) e chame [**IMFShutdown:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown). O chamador de **MFCreatePresentationClock** é responsável por chamar o **desligamento**; na maioria dos casos, essa é a sessão de mídia em vez do aplicativo.

## <a name="presentation-time-sources"></a>Fontes de tempo de apresentação

Apesar de seu nome, o relógio de apresentação não implementa de fato um relógio. Em vez disso, ele obtém os tempos do relógio de outro objeto, chamado de *fonte de tempo de apresentação*. A fonte de tempo pode ser qualquer objeto que gere tiques de relógio precisos e expor a interface [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . A ilustração a seguir mostra este processo.

![diagrama mostrando a relação entre o relógio de apresentação e a fonte de hora da apresentação](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

Quando o relógio de apresentação é criado pela primeira vez, ele não tem uma fonte de tempo. Para definir a origem do tempo, chame [**IMFPresentationClock:: Settimename**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) com um ponteiro para a interface [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) da fonte de tempo. Uma fonte de tempo dá suporte aos mesmos Estados que o relógio de apresentação (em execução, pausado e parada) e deve implementar a interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) . O relógio de apresentação usa essa interface para notificar a fonte de tempo quando alterar o estado. Dessa forma, a fonte de tempo fornece os tiques do relógio, mas o relógio de apresentação inicia as alterações de estado no relógio.

Alguns coletores de mídia têm acesso a um relógio preciso e, portanto, expõem a interface [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . Em particular, o processador de áudio pode usar a frequência da placa de som como um relógio. Na reprodução de áudio, é útil que o processador de áudio atue como a fonte de tempo, para que o vídeo seja sincronizado com a taxa de reprodução de áudio. Isso geralmente produz resultados melhores do que tentar corresponder o áudio a um relógio externo.

Media Foundation também fornece uma fonte de tempo de apresentação com base no relógio do sistema. Para criar esse objeto, chame [**MFCreateSystemTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource). A fonte de tempo do sistema pode ser usada quando nenhum coletor de mídia fornece uma fonte de tempo.

Em geral, um coletor de mídia deve usar o relógio de apresentação fornecido a ele, independentemente de qual fonte de tempo o relógio de apresentação usa. Essa regra se aplica mesmo quando um coletor de mídia implementa [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource). Se o relógio de apresentação usar alguma outra fonte de tempo, o coletor de mídia deverá seguir essa fonte de tempo, não seu próprio relógio interno.

Há duas situações em que um coletor de mídia não segue o relógio de apresentação:

-   Alguns coletores de mídia são sem *taxa*. Se um coletor de mídia for sem taxa, ele consumirá amostras o mais rápido possível, sem agendá-los de acordo com o relógio de apresentação. Normalmente, os coletores sem taxa gravam dados em um arquivo, portanto, é desejável concluir a operação o mais rápido possível. Um coletor sem taxa retorna o sinalizador sem taxa de MEDIASINK \_ em seu método [**IMFMediaSink:: getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . Quando todos os coletores em uma topologia são sem taxa, a sessão de mídia envia dados por push pelo pipeline o mais rápido possível.

-   Alguns coletores de mídia não podem corresponder a taxas com uma fonte de tempo diferente de si mesmos. Nesse caso, o coletor retorna o MEDIASINK \_ não pode \_ corresponder ao \_ sinalizador Clock em seu método [**getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . O pipeline ainda pode usar outra fonte de tempo, mas os resultados serão menos do que o ideal. O coletor provavelmente ficará atrás e causará problemas durante a reprodução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



