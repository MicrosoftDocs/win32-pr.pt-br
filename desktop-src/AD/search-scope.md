---
title: Especificando o escopo da pesquisa
description: Você pode especificar o escopo de uma pesquisa como uma pesquisa de base, de um nível ou de subárvore.
ms.assetid: b02354c2-7b95-4911-8ae3-4a261d3ca2d3
ms.tgt_platform: multiple
keywords:
- Especificando o AD do escopo de pesquisa
- Active Directory, pesquisando, especificando o escopo da pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ff076e0410088c69eace25f204241c1c51c6fb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640383"
---
# <a name="specifying-the-search-scope"></a>Especificando o escopo da pesquisa

Você pode especificar o escopo de uma pesquisa como uma pesquisa de base, de um nível ou de subárvore. Use o sinalizador de **\_ escopo de \_ pesquisa \_ do ADS SEARCHPREF** com os valores da enumeração [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) para especificar o escopo da pesquisa. A lista a seguir inclui descrições dos tipos de pesquisa:

-   **Base**. Uma pesquisa de base limita a pesquisa ao objeto base. O número máximo de objetos retornados é sempre um. Essa pesquisa é útil para verificar a existência de um objeto para recuperar a associação de grupo. Por exemplo, se você tiver um nome diferenciado de objeto e precisar verificar a existência do objeto com base no caminho, você poderá usar uma pesquisa de nível único. Se a pesquisa falhar, você poderá pressupor que o objeto pode ter sido renomeado ou movido para um local diferente, ou que você tenha recebido as informações erradas sobre o objeto. Lembre-se de que você deve armazenar o GUID (identificador global exclusivo) do objeto em vez do nome distinto, se desejar revisitar um objeto. O GUID sempre fará referência ao mesmo objeto, independentemente de onde o objeto está localizado dentro da hierarquia de diretório.
-   **Um nível**. Uma pesquisa de nível único é restrita aos filhos imediatos de um objeto base, mas exclui o objeto base em si. Essa configuração pode executar uma pesquisa direcionada para objetos filho imediatos de um objeto pai. Por exemplo, considere um objeto pai P1 e seus filhos imediatos: C1, C2 e C3. Uma pesquisa de nível único avalia C1, C2 e C3 em relação aos critérios de pesquisa, mas não avalia P1. Use uma pesquisa de nível único para enumerar todos os filhos de um objeto. Uma enumeração [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) se traduz em uma pesquisa de um nível.
-   **Subárvore**. Uma pesquisa de subárvore (ou uma pesquisa profunda) inclui todos os objetos filho, bem como o objeto base. Você pode solicitar ao provedor LDAP para perseguir referências a outros serviços de diretório LDAP, incluindo outros domínios de diretório ou florestas.

 

 