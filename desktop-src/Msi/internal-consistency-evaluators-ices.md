---
description: Os avaliadores de consistência interna, também chamados de ICEs, são ações personalizadas escritas em VBScript, JScript ou como uma DLL ou EXE.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: Avaliadores de consistência interna – ICEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744915d7f484128095e308f390caae75323775b684b38a0184592dc99a2700f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043376"
---
# <a name="internal-consistency-evaluators---ices"></a>Avaliadores de consistência interna – ICEs

Os avaliadores de consistência interna, também chamados de ICEs, são ações personalizadas escritas em VBScript, JScript ou como uma DLL ou EXE. Quando essas ações personalizadas são executadas, eles examinam o banco de dados em busca de entradas nos registros de banco de dados válidos quando examinados individualmente, mas que podem causar comportamento incorreto no contexto de todo o banco de dados. Observe que isso é diferente da validação feita em registros individuais usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify).

Por exemplo, a [tabela Componente pode](component-table.md) listar vários componentes que são todos válidos quando testados individualmente com [**MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) No entanto, **MsiViewModify** não capturaria o erro quando dois componentes usam o mesmo [GUID](guid.md) que o código do componente. A ação personalizada [ICE08](ice08.md) foi projetada para validar se a tabela Component não contém GUIDs de código de componente duplicados.

As ações personalizadas ice retornam quatro tipos de mensagens:

-   [**Erros**](merge-errors.md) Mensagens de erro relatam a autorização do banco de dados que causam comportamento incorreto. Por exemplo, GUIDs de componente duplicados fazer com que o instalador registre componentes incorretamente.
-   **Avisos** Mensagens de aviso relatam a produção de banco de dados que causa comportamento incorreto em determinados casos. Os avisos também podem relatar efeitos colaterais inesperados da autorização do banco de dados. Por exemplo, inserindo o mesmo nome de propriedade em duas condições que diferem apenas pelo caso de letras no nome. Como o instalador diferencia minúsculas, o instalador os trata como propriedades diferentes.
-   **Falhas** Mensagens de falha relatam a falha da ação personalizada ice. A falha geralmente é causada por um banco de dados com problemas tão graves que o ICE não pode executar.
-   **Informacional** As mensagens informativas fornecem informações do ICE e não indicam um problema com o banco de dados. Geralmente, elas são informações sobre o PRÓPRIO ICE, como uma breve descrição. Eles também podem fornecer informações de progresso à medida que o ICE é executado.

Para obter mais informações, consulte [Usando avaliadores de consistência interna.](using-internal-consistency-evaluators.md)

 

 



