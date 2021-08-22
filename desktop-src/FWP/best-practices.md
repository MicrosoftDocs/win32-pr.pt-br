---
title: Práticas recomendadas (Windows de filtragem)
description: A lista a seguir contém as práticas recomendadas para o desenvolvimento de aplicativos usando a API do WFP (Windows Filtering Platform).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0ddb6038a9fe43070f1c16e545dbd7ac8929f3363fc88556aac391428175ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069456"
---
# <a name="best-practices-windows-filtering-platform"></a>Práticas recomendadas (Windows de filtragem)

A lista a seguir contém as práticas recomendadas para o desenvolvimento de aplicativos usando a API do WFP (Windows Filtering Platform).

-   Use sessões dinâmicas.

    Muitos aplicativos adicionam objetos de política de filtragem no início e, em seguida, excluem esses objetos na parada. Usando uma sessão dinâmica, você garante que esses objetos sejam excluídos mesmo se o aplicativo falhar. Além disso, simplesmente fechar o identificador do mecanismo na parada é mais eficiente do que fazer chamadas individuais para excluir cada objeto.

-   Lidar com os tempos-alto da transação normalmente ou definir a **sessão txnWaitTimeoutInMSec** como infinita para evitar tempos-fim.

    Mesmo se você não usar transações explícitas, a maioria das chamadas ainda será executada em uma transação implícita e, portanto, poderá ter um tempo máximo.

-   Use transações explícitas para combinar operações relacionadas de a adicionar ou excluir em uma única transação.

    Isso é mais eficiente e facilita a limpeza de resultados parciais em caminhos de erro.

-   Use cadeias de caracteres em conformidade com a MUI.

    Todas as cadeias de caracteres localizáveis são armazenadas em uma estrutura de dados comum: [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). As cadeias de caracteres dentro dessa estrutura podem ser cadeias de caracteres indiretas do tipo com suporte por [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring). Antes que uma estrutura **\_ DISPLAY \_ DATA0 do FWPM** seja retornada por qualquer uma das funções, as cadeias de caracteres indiretas são resolvidas para o recurso de cadeia de caracteres especificado usando a localidade do chamador.

-   Associe todos os objetos a um provedor.

    Quando vários provedores são instalados no sistema, isso torna mais fácil para as ferramentas de diagnóstico determinar quem adicionou o quê.

-   Adicione filtros ao seu próprio subcamada.

    Depois que um filtro de terminação em uma subcamada for atingido, não serão avaliados mais filtros nessa subcamada. Portanto, se você adicionar seus filtros ao mesmo subcamada que outro provedor, poderá impedir que os filtros uns dos outros seja invocados, resultando em resultados inesperados.

-   Use a ALE (Imposição de Camada de Aplicativo) em vez da filtragem orientada a pacotes.

    A filtragem na camada de pacote está lenta.

-   Filtre erros ICMP e eventos RST antes que eles sejam gerados.

    Isso é mais eficiente que filtrar esses eventos depois que eles são gerados.

-   Execute a inspeção de pacotes na camada de Dados de Fluxo/Datagrama em vez de na camada de transporte.

    Isso se aplica ao desenvolvimento de callouts. Para obter mais informações, consulte [Considerações sobre programação](/windows-hardware/drivers/network/callout-driver-programming-considerations) de driver de chamada no WDK (Kit Windows Driver).

-   Considere as implicações de desempenho ao usar filtros complexos.

    A partir do Windows 7 e Windows Server 2008 R2, os filtros podem ser criados com várias condições que usam a mesma chave de campo. Isso permite que políticas complexas sejam criadas com menos filtros. No entanto, esses filtros complexos podem incorrer em um desempenho mais lento para o mecanismo de filtro WFP classificar. Uma avaliação deve ser feita para determinar se o uso desses filtros causa um efeito adverso no desempenho geral da solução.

 

 
