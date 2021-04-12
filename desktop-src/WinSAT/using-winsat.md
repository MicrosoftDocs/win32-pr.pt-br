---
title: Usando o WinSAT
description: Você pode usar a API do WinSAT (ferramenta de avaliação do sistema do Windows) para iniciar avaliações formais e ad hoc da configuração de hardware do computador, recuperar a pontuação básica do computador e pontuações de cada Subcomponente da avaliação e recuperar detalhes da avaliação, como os detalhes do processador que foi avaliado.
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a23ab35d989a736fa61833e678c0a4c79954e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363902"
---
# <a name="using-winsat"></a>Usando o WinSAT

\[O WinSAT pode ser alterado ou indisponível para versões após a Windows 8.1.\]

Você pode usar a API do WinSAT (ferramenta de avaliação do sistema do Windows) para [Iniciar avaliações formais e ad hoc](#initiating-an-assessment) da configuração de hardware do computador, [recuperar a pontuação básica do computador](#retrieving-the-scores-of-the-assessment) e pontuações de cada Subcomponente da avaliação e [recuperar detalhes da avaliação](#retrieving-details-of-the-assessment), como os detalhes do processador que foi avaliado.

## <a name="initiating-an-assessment"></a>Iniciando uma avaliação

Depois de Windows 8.1 você pode iniciar avaliações formais e ad hoc do computador. Uma avaliação formal avalia os seguintes subcomponentes do computador:

-   CPU
-   Memória
-   Disco primário
-   Placa de vídeo

Para iniciar uma avaliação formal, chame o método [**IInitiateWinSATAssessment:: InitiateFormalAssessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) . Os resultados de avaliações formais são salvos no repositório de avaliação e podem ser recuperados em uma data posterior.

Normalmente, você usa avaliações ad hoc para avaliar apenas um subcomponente do computador, por exemplo, a CPU ou a memória. No entanto, você pode usar a opção **formal** para avaliar todos os subcomponentes. Para iniciar uma avaliação ad hoc, chame o método [**IInitiateWinSATAssessment:: InitiateAssessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) . Observe que os resultados de avaliações ad hoc não são salvos no repositório de avaliação.

Para recuperar a notificação quando o andamento for feito ou quando a avaliação for concluída, implemente a interface [**IWinSATInitiateEvents**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents) .

Você não pode executar avaliações formais remotamente ou em um computador que esteja sendo executado em baterias. Você também não pode executar remotamente uma avaliação ad hoc no subcomponente gráficos.

## <a name="retrieving-the-scores-of-the-assessment"></a>Recuperando as pontuações da avaliação

Você pode recuperar a pontuação básica do computador e a pontuação de cada Subcomponente da avaliação. Você pode usar a API para recuperar as pontuações apenas para avaliações formais. Para recuperar as pontuações de avaliações ad hoc, você deve incluir o argumento **-XML** na linha de comando para salvar os resultados da avaliação em um arquivo XML e, em seguida, analisar o arquivo para a Pontuação do subcomponente.

A pontuação básica é uma medida geral da configuração de hardware do computador. Uma pontuação básica mais alta geralmente significa que o computador terá um desempenho melhor e mais rápido do que um computador com uma pontuação básica mais baixa, especialmente ao executar tarefas mais avançadas e com uso intensivo de recursos.

Cada componente de hardware recebe uma sublinhado individual. A pontuação base do seu computador é determinada pela sublinhagem mais baixa. Por exemplo, se a subpontuação mais baixa de um componente de hardware individual for 2,6, a pontuação base será 2,6. A pontuação base não é uma média dos subtotais combinados.

Um usuário pode usar a pontuação básica para comprar com confiança programas e outros softwares que correspondam à pontuação base do computador. Por exemplo, se o computador tiver uma pontuação básica de 3,3, o usuário poderá comprar com confiança qualquer software criado para esta versão do Windows que exija um computador com uma pontuação básica de 3 ou mais.

Para recuperar a pontuação base, primeiro chame o método [**IQueryRecentWinSATAssessment:: get \_ info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) para obter a interface [**IProvideWinSATResultsInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) . Em seguida, chame o método [**IProvideWinSATResultsInfo:: get \_ SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) para obter a pontuação básica.

Um usuário pode usar pontuações de subcomponente para determinar se um subcomponente do computador pode dar suporte a um tipo específico de aplicativo. Por exemplo, um usuário que passa mais tempo lendo ou gravando documentos pode exigir uma pontuação mais alta para o disco do que um usuário que executa aplicativos científicos, e um usuário que executa aplicativos científicos provavelmente desejaria uma pontuação maior de subcomponente de CPU e pode não se preocupar com uma pontuação de disco inferior.

Para recuperar a pontuação de cada Subcomponente, primeiro chame o método [**IQueryRecentWinSATAssessment:: get \_ info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) para obter a interface [**IProvideWinSATResultsInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) . Em seguida, chame o método [**IProvideWinSATResultsInfo:: GetAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) para obter a interface [**IProvideWinSATAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) . Para cada Subcomponente cuja Pontuação você deseja recuperar, chame o método [**IProvideWinSATAssessmentInfo:: get \_ Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .

## <a name="retrieving-details-of-the-assessment"></a>Recuperando detalhes da avaliação

A API do WinSAT fornece a pontuação base e as pontuações gerais para cada Subcomponente. Para obter detalhes da avaliação (por exemplo, as métricas usadas para computar a pontuação e os detalhes do processador que foi avaliado), você deve recuperar os dados do documento de avaliação XML. Para recuperar detalhes da avaliação formal mais recente, chame o método [**\_ XML IQueryRecentWinSATAssessment:: Get**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) . Para recuperar os detalhes de cada avaliação no repositório de dados do WinSAT, chame o método [**IQueryAllWinSATAssessments:: get \_ AllXML**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml) .

Para obter informações sobre o esquema XML e os detalhes que você pode recuperar, consulte [esquema do WinSAT](winsat-schema.md).

 

 




