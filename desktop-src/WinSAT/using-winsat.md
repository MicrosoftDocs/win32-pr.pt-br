---
title: Usando o WinSAT
description: Você pode usar Windows API do WinSAT (Ferramenta de Avaliação do Sistema) do Windows para iniciar avaliações formais e ad hoc da configuração de hardware do computador, recuperar a pontuação base para o computador e as pontuações para cada subcomponente da avaliação e recuperar detalhes da avaliação, como os detalhes do processador que foi avaliado.
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23cf26d31ccbd3eb6e51fb1717c055fb6538c57612d374b0a3b7a2a5b2382681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733776"
---
# <a name="using-winsat"></a>Usando o WinSAT

\[O WinSAT pode ser alterado ou não disponível para versões após Windows 8.1.\]

Você pode usar a API do WinSAT (Ferramenta de Avaliação do Sistema) do Windows para iniciar avaliações formais e [ad hoc](#initiating-an-assessment) da configuração de hardware do computador, recuperar a pontuação [base](#retrieving-the-scores-of-the-assessment) para o computador e as pontuações para cada subcomponente da avaliação e recuperar detalhes da avaliação, como os detalhes do processador que foi avaliado. [](#retrieving-details-of-the-assessment)

## <a name="initiating-an-assessment"></a>Iniciando uma avaliação

Após Windows 8.1 você poderá iniciar avaliações formais e ad hoc do computador. Uma avaliação formal avalia os seguintes subcomponentes do computador:

-   CPU
-   Memória
-   Disco primário
-   Cartão de vídeo

Para iniciar uma avaliação formal, chame o [**método IInitiateWinSATAssessment::InitiateFormalAssessment.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) Os resultados de avaliações formais são salvos no armazenamento de avaliação e podem ser recuperados posteriormente.

Normalmente, você usa avaliações ad hoc para avaliar apenas um subcomponente do computador, por exemplo, a CPU ou a memória. No entanto, você pode usar a **opção formal** para avaliar todos os subcomponentes. Para iniciar uma avaliação ad hoc, chame o [**método IInitiateWinSATAssessment::InitiateAssessment.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) Observe que os resultados de avaliações ad hoc não são salvos no armazenamento de avaliação.

Para recuperar a notificação quando o progresso for feito ou quando a avaliação for concluída, implemente a interface [**IWinSATInitiateEvents.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents)

Você não pode executar avaliações formais remotamente ou em um computador que está executando baterias. Você também não pode executar remotamente uma avaliação ad hoc no subcomponente de gráficos.

## <a name="retrieving-the-scores-of-the-assessment"></a>Recuperando as pontuações da avaliação

Você pode recuperar a pontuação base do computador e a pontuação para cada subcomponente da avaliação. Você pode usar a API para recuperar as pontuações apenas para avaliações formais. Para recuperar as pontuações de avaliações ad hoc, você deve incluir o argumento **-xml** na linha de comando para salvar os resultados da avaliação em um arquivo XML e, em seguida, analisar o arquivo para a pontuação do subcomponente.

A pontuação base é uma medida geral da configuração de hardware do computador. Uma pontuação base mais alta geralmente significa que o computador terá um desempenho melhor e mais rápido do que um computador com uma pontuação base inferior, especialmente ao executar tarefas mais avançadas e com uso intensivo de recursos.

Cada componente de hardware recebe um sublinhado individual. A pontuação base do computador é determinada pelo sublinhado mais baixo. Por exemplo, se o sublinhado mais baixo de um componente de hardware individual for 2,6, a pontuação base será 2,6. A pontuação base não é uma média dos sublinhados combinados.

Um usuário pode usar a pontuação base para comprar programas e outros softwares que são de acordo com a pontuação base do computador. Por exemplo, se o computador tiver uma pontuação base de 3,3, o usuário poderá comprar com segurança qualquer software projetado para esta versão do Windows que exija um computador com uma pontuação base 3 ou inferior.

Para recuperar a pontuação base, primeiro chame o método [**IQueryRecentWinSATAssessment::get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) para obter a interface [**IProvideWinSATResultsInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) Em seguida, chame [**o método IProvideWinSATResultsInfo::get \_ SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) para obter a pontuação base.

Um usuário pode usar pontuações de subcomponentes para determinar se um subcomponente do computador pode dar suporte a um tipo específico de aplicativo. Por exemplo, um usuário que gasta mais tempo lendo ou escrevendo documentos pode exigir uma pontuação mais alta para o disco do que um usuário que executa aplicativos científicos e um usuário que executa aplicativos científicos provavelmente deseja uma pontuação mais alta de subcomponente de CPU e pode não se preocupar com uma pontuação de disco inferior.

Para recuperar a pontuação de cada subcomponente, primeiro chame o método [**IQueryRecentWinSATAssessment::get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) para obter a interface [**IProvideWinSATResultsInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) Em seguida, chame o método [**IProvideWinSATResultsInfo::GetAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) para obter a interface [**IProvideWinSATAssessmentInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) Para cada subcomponente cuja pontuação você deseja recuperar, chame o método [**IProvideWinSATAssessmentInfo::get \_ Score.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score)

## <a name="retrieving-details-of-the-assessment"></a>Recuperando detalhes da avaliação

A API do WinSAT fornece a pontuação base geral e as pontuações para cada subcomponente. Para obter detalhes da avaliação (por exemplo, as métricas usadas para calcular a pontuação e os detalhes do processador que foi avaliado), você deve recuperar os dados do documento de avaliação XML. Para recuperar detalhes da avaliação formal mais recente, chame o [**método \_ XML IQueryRecentWinSATAssessment::get.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) Para recuperar os detalhes de cada avaliação no armazenamento de dados winSAT, chame o método [**IQueryAllWinSATAssessments::get \_ AllXML.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml)

Para obter informações sobre o esquema XML e os detalhes que você pode recuperar, consulte [Esquema WinSAT](winsat-schema.md).

 

 




