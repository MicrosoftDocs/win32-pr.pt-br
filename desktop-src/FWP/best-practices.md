---
title: Práticas recomendadas (plataforma de filtragem do Windows)
description: A lista a seguir contém as práticas recomendadas para o desenvolvimento de aplicativos usando a API da Windows Filtering Platform (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499211"
---
# <a name="best-practices-windows-filtering-platform"></a>Práticas recomendadas (plataforma de filtragem do Windows)

A lista a seguir contém as práticas recomendadas para o desenvolvimento de aplicativos usando a API da Windows Filtering Platform (WFP).

-   Use sessões dinâmicas.

    Muitos aplicativos adicionam objetos de política de filtragem no início e, em seguida, excluem esses objetos em stop. Usando uma sessão dinâmica, você garante que esses objetos sejam excluídos mesmo se o aplicativo falhar. Além disso, simplesmente fechar o identificador do mecanismo em Stop é mais eficiente do que fazer chamadas individuais para excluir cada objeto.

-   Trate os tempos limite da transação normalmente ou defina a sessão **txnWaitTimeoutInMSec** como infinito para evitar tempos limite.

    Mesmo que você não use transações explícitas, a maioria das chamadas ainda será executada em uma transação implícita e, portanto, poderá atingir o tempo limite.

-   Use transações explícitas para combinar operações de adição ou exclusão relacionadas em uma única transação.

    Isso é mais eficiente e torna mais fácil limpar resultados parciais em caminhos de erro.

-   Use cadeias de caracteres compatíveis com o MUI.

    Todas as cadeias de caracteres localizáveis são armazenadas em uma estrutura de dados comum: [**FWPM \_ Exibir \_ data0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). As cadeias de caracteres nessa estrutura podem ser cadeias de caracteres indiretas do tipo com suporte do [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring). Antes que uma estrutura **\_ \_ data0 de exibição de FWPM** seja retornada por qualquer uma das funções, as cadeias de caracteres indiretas são resolvidas para o recurso de cadeia de caracteres especificado usando a localidade do chamador.

-   Associar todos os objetos a um provedor.

    Quando vários provedores são instalados no sistema, isso torna mais fácil para as ferramentas de diagnóstico determinar quem adicionou o quê.

-   Adicione filtros a sua própria subcamada.

    Depois que um filtro de terminação em uma subcamada for atingido, nenhum filtro será avaliado nessa subcamada. Portanto, se você adicionar seus filtros à mesma subcamada como outro provedor, poderá impedir que os filtros uns dos outros sejam invocados, resultando em resultados inesperados.

-   Use a ALE (aplicação de camada de aplicativo) em vez da filtragem orientada por pacotes.

    A filtragem na camada de pacote está lenta.

-   Filtre os erros de ICMP e os eventos RST antes que eles sejam gerados.

    Isso é mais eficiente para filtrar esses eventos depois que eles são gerados.

-   Execute a inspeção de pacotes na camada de dados de fluxo/datagrama em vez de na camada de transporte.

    Isso se aplica ao desenvolvimento de textos explicativos. Para obter mais informações, consulte [considerações de programação de driver de texto explicativo](/windows-hardware/drivers/network/callout-driver-programming-considerations) no WDK (Kit de driver do Windows).

-   Considere as implicações de desempenho ao usar filtros complexos.

    A partir do Windows 7 e do Windows Server 2008 R2, os filtros podem ser criados com várias condições que usam a mesma chave de campo. Isso permite que políticas complexas sejam criadas com menos filtros. No entanto, esses filtros complexos podem incorrer em um desempenho mais lento para o mecanismo de filtro WFP classificar. Deve-se fazer uma avaliação para determinar se o uso desses filtros causa um efeito adverso no desempenho geral da solução.

 

 
