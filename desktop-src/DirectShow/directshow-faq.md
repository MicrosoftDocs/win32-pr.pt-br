---
description: Perguntas frequentes do DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: Perguntas frequentes do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500486"
---
# <a name="directshow-faq"></a>Perguntas frequentes do DirectShow

Este artigo responde muitas perguntas frequentes sobre o Microsoft DirectShow.

**A quais sistemas operacionais o DirectShow dá suporte?**

O DirectShow está disponível em todas as versões do Windows com suporte.

**Quanto conhecimento de COM eu preciso para programar com o DirectShow?**

Para o desenvolvimento de aplicativos, você precisa entender as noções básicas do trabalho com objetos COM: como instanciá-los, acessar as interfaces que eles expõem e gerenciar contagens de referência nessas interfaces. O desenvolvimento de filtro requer mais conhecimento COM.

**A quais formatos o DirectShow dá suporte?**

Consulte [formatos com suporte no DirectShow](supported-formats-in-directshow.md).

**Há uma HCL (lista de compatibilidade de hardware) do DirectShow?**

Não. O DirectShow usa o Microsoft DirectDraw e os recursos de hardware do Microsoft DirectSound se eles estiverem disponíveis. Quando não há nenhum hardware especial disponível, o DirectShow usa GDI para desenhar vídeo e as APIs de multimídia do **WaveOut** \* para reproduzir áudio.

**Quais linguagens posso usar para escrever um aplicativo DirectShow?**

O DirectShow foi projetado principalmente para desenvolvimento em C++. Um pequeno subconjunto da API do DirectShow é exposto por meio do Visual Basic 6,0; no entanto, esse recurso foi preterido.

**O DirectShow nunca estará acessível por meio de código gerenciado?**

A Microsoft não tem planos atuais para implementar uma API do DirectShow gerenciada.

**Que compilador preciso para o desenvolvimento do DirectShow?**

Qualquer compilador capaz de gerar objetos COM (Component Object Model) deve funcionar depois que o ambiente do compilador tiver sido configurado corretamente.

**Como o DirectShow se relaciona com o Microsoft DirectX?**

Internamente, o DirectShow usa o DirectSound e o DirectDraw quando o hardware dá suporte a ele. O processador de vídeo e os filtros de mixagem de sobreposição usam superfícies do DirectDraw 3 e do DirectDraw 5. O processador de mixagem de vídeo 7 (somente Windows XP) usa superfícies do DirectDraw 7. O processador de mixagem de vídeo 9 e o processador de vídeo aprimorado usam as APIs mais recentes do Microsoft Direct3D. Você não precisa usar as outras APIs do DirectX para gravar um aplicativo do DirectShow, embora seja possível combiná-los.

**Como o DirectShow está relacionado ao Microsoft ActiveMovie?**

O ActiveMovie foi o nome original do DirectShow. O termo que o ActiveMovie não é mais usado.

**O código-fonte para o utilitário GraphEdit está disponível? GraphEdit pode ser redistribuído?**

Não, a origem não está disponível e Graphedt.exe não é redistribuível.

**DMOs substituir filtros do DirectShow?**

O Microsoft DirectX Media Objects (DMOs) pode ser usado em um aplicativo do DirectShow. Para codificadores, decodificadores e efeitos, você é incentivado a escrever um DMO em vez de um filtro do DirectShow. (Observação: se você quiser usar a aceleração de vídeo do DirectX em seu decodificador, deverá implementá-lo como um filtro.) Para outras finalidades, um filtro do DirectShow pode ser mais apropriado. Para obter mais informações sobre DMOs, consulte [DirectX Media Objects](directx-media-objects.md).

**Estou executando um arquivo de formato AVI com o Windows Media Player. Posso ouvir o áudio, mas parece que não há nenhum vídeo, eu simplesmente vejo preto. Qual é o problema?**

Provavelmente, o arquivo foi codificado com um codec que não está presente no seu sistema. Embora o formato de arquivo AVI seja comum, os arquivos AVI podem ser criados com vários formatos de compactação (codecs) diferentes. Se você tentar reproduzir um arquivo AVI que usa um codec sem suporte, poderá ouvir o componente de áudio, mas o vídeo será exibido como uma tela preta ou o conteúdo da tela permanecerá inalterado.

> [!Note]  
> O Windows Media Player muitas vezes tenta baixar e instalar um codec, caso ele não esteja presente no sistema.

 

**Como fazer compilar meu aplicativo? De quais bibliotecas e arquivos de cabeçalho eu preciso?**

Consulte [Configurando o ambiente de compilação](setting-up-the-build-environment.md).

**O GraphEdit exibe muitos filtros que não estão documentados. O que são esses filtros?**

GraphEdit enumera todos os filtros registrados em seu sistema em uma categoria de filtro. Isso pode incluir filtros instalados por aplicativos de terceiros ou instalados por outras tecnologias da Microsoft, como o Windows Media ou o NetMeeting. Além disso, alguns filtros do DirectShow atuam como wrappers para codecs ou dispositivos de hardware, com cada codec ou dispositivo exibido como um filtro distinto. O codec de vídeo Microsoft H. 263 é usado pelo NetMeeting e não tem mais suporte no DirectShow. Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).

**Estou tendo problemas para criar meu gráfico personalizado programaticamente.**

Primeiro, tente criar o grafo de filtro com GraphEdit. Essa ferramenta permite simular muitas possibilidades rapidamente. GraphEdit é sempre um ótimo lugar para testar o grafo antes de tentar compilá-lo com o código-fonte.

Para obter mais informações sobre a criação de gráficos, consulte os seguintes artigos:

-   [Criando o grafo de filtro](building-the-filter-graph.md)
-   [Enumerando objetos em um grafo de filtro](enumerating-objects-in-a-filter-graph.md)

**Como posso detectar se o DirectShow está instalado em determinado computador?**

Chame **CoCreateInstance** para criar uma instância do Gerenciador do grafo de filtro. Se essa chamada for realizada com sucesso, o DirectShow será instalado no computador. O código a seguir mostra como fazer isso:


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



**Como fazer alterar as configurações de um filtro sem exibir a página de propriedades?**

A maioria dos filtros expõe uma ou mais interfaces para definir propriedades no filtro. Consulte a página de referência para o filtro em questão. (Consulte [filtros do DirectShow](directshow-filters.md).)

**Posso testar meu filtro com o GraphEdit?**

Enquanto você estiver desenvolvendo um filtro, o GraphEdit poderá ajudá-lo a visualizar as conexões entre os filtros. Ele também pode fornecer um teste rápido da funcionalidade de um filtro. No entanto, ela não se destina como uma plataforma de teste robusta.

**Em que os filtros do anel de privilégio são executados?**

Os filtros são executados no anel 3, embora alguns filtros controlem os dispositivos de streaming executados em anel 0. Para obter mais informações, consulte [como os dispositivos de hardware participam do grafo de filtro](how-hardware-devices-participate-in-the-filter-graph.md).

**Preciso usar um depurador de kernel?**

Isso depende de seu projeto específico. A instalação das bibliotecas de tempo de execução de depuração do DirectX significa que você está instalando os drivers de depuração e outros componentes do modo kernel, e que, se seu aplicativo causar uma asserção de depuração em um desses componentes, seu computador será reinicializado automaticamente, a menos que você tenha um depurador de kernel anexado ao seu processo.

**Quando executo meu aplicativo no depurador, ele falha.**

Alguns decodificadores foram projetados para não funcionar enquanto o aplicativo está anexado ao depurador. Tente executar o aplicativo fora do depurador.

**Como funciona a macro de GUID de definição \_ ?**

A macro **definir \_ GUID** resolve o problema de declaração de `extern` referências a valores GUID em seu código-fonte. Por exemplo, suponha que seu projeto tenha três arquivos de origem, Src1. cpp, Src2. cpp e Src3. cpp, e que todos os três arquivos usem um determinado valor de GUID que você definiu. O valor de GUID deve ser definido exatamente uma vez no seu projeto e os outros arquivos de origem devem declarar `extern` referências a ele. Com a macro **definir \_ GUID** , você pode usar o mesmo arquivo de cabeçalho para ambas as finalidades. No arquivo de cabeçalho, declare o GUID da seguinte maneira:


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



(Em que esse exemplo tem zeros, coloque os valores de GUID reais.) Você pode usar o utilitário Guidgen.exe para criar um novo GUID e colá-lo no arquivo de cabeçalho no formato **definir \_ GUID** . Inclua esse arquivo de cabeçalho em todos os arquivos de origem que fazem referência ao GUID. Em exatamente um dos arquivos de origem, inclua o arquivo de cabeçalho Initguid. h antes do arquivo de cabeçalho. Por exemplo:


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



Sempre que o arquivo de cabeçalho Initguid. h não for incluído, a macro **definir \_ GUID** criará uma `extern` referência ao valor de GUID. Quando o arquivo de cabeçalho Initguid. h é incluído, ele redefine a macro **definir \_ GUID** para que **definir o \_ GUID** crie uma declaração de definição do GUID.

Se você não incluir Initguid. h em nenhum dos arquivos de origem, receberá um erro de link "símbolo externo não resolvido". Se você incluir Initguid. h duas vezes para o mesmo GUID, receberá um erro de compilação "redefinição; inicialização múltipla ". Para resolver esses erros, verifique se Initguid. h está incluído exatamente uma vez. Além disso, não inclua Initguid. h dentro de um arquivo de cabeçalho pré-compilado, pois, em vigor, o cabeçalho pré-compilado é incluído em todos os arquivos de origem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução ao DirectShow](introduction-to-directshow.md)
</dt> </dl>

 

 



