---
description: Avaliadores de consistência internos, também chamados de ICEs, são ações personalizadas escritas em VBScript, JScript ou como DLL ou EXE.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: Avaliadores de consistência internos-ICEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77be6e2bf33bbe348acab45191782a211ea4663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785434"
---
# <a name="internal-consistency-evaluators---ices"></a>Avaliadores de consistência internos-ICEs

Avaliadores de consistência internos, também chamados de ICEs, são ações personalizadas escritas em VBScript, JScript ou como DLL ou EXE. Quando essas ações personalizadas são executadas, elas verificam o banco de dados em busca de entradas em registros de banco de dados válidos quando examinados individualmente, mas isso pode causar um comportamento incorreto no contexto do banco de dados inteiro. Observe que isso é diferente da validação feita em registros individuais usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify).

Por exemplo, a [tabela de componentes](component-table.md) pode listar vários componentes válidos quando testados individualmente com [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify). No entanto, o **MsiViewModify** não detectaria o erro quando dois componentes usam o mesmo [GUID](guid.md) que o código do componente. A ação personalizada [ICE08](ice08.md) foi projetada para validar que a tabela de componentes não contém GUIDs de código de componente duplicados.

As ações personalizadas do ICE retornam quatro tipos de mensagens:

-   [**Erros**](merge-errors.md) do Mensagens de erro relatam criação de banco de dados que causam comportamento incorreto. Por exemplo, GUIDs de componente duplicados fazem com que o instalador Registre componentes incorretamente.
-   **Avisos** Mensagens de aviso relatam criação de banco de dados que causa comportamento incorreto em determinados casos. Os avisos também podem relatar efeitos colaterais inesperados de criação de banco de dados. Por exemplo, inserir o mesmo nome de propriedade em duas condições que diferem somente pelo caso de letras no nome. Como o instalador diferencia maiúsculas de minúsculas, o instalador o trata como propriedades diferentes.
-   **Falhas** Mensagens de falha relatam a falha da ação personalizada do ICE. Normalmente, a falha é causada por um banco de dados com problemas graves que o ICE não pode até mesmo executar.
-   **Informações** As mensagens informativas fornecem informações do ICE e não indicam um problema com o banco de dados. Geralmente, eles são informações sobre o próprio ICE, como uma breve descrição. Eles também podem fornecer informações de progresso à medida que a ICE é executada.

Para obter mais informações, consulte [usando avaliadores de consistência internos](using-internal-consistency-evaluators.md).

 

 



