---
title: Pesquisando Active Directory
description: Uma função importante do Active Directory é resolver consultas de dados para pessoas, bem como dados de configuração para computadores e serviços.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Pesquisando Active Directory ADSI
- ADSI ADSI, pesquisando Active Directory
- consulta ADSI, pesquisando Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291778"
---
# <a name="searching-active-directory"></a>Pesquisando Active Directory

Uma função importante do Active Directory é resolver consultas de dados para pessoas, bem como dados de configuração para computadores e serviços. Para escrever consultas eficientes para Active Directory, é útil estar familiarizado com o seguinte:

-   Determinando o escopo da consulta: o cliente deve localizar as propriedades de objetos que podem estar localizados em qualquer lugar dentro de uma floresta ou somente dentro de um domínio ou em uma UO (unidade organizacional) específica?
-   Determinando a profundidade da consulta: a consulta deve pesquisar apenas um nível ou ela pode atravessar outros diretórios LDAP?
-   Desempenho e manipulação de grandes conjuntos de resultados: como o cliente deve lidar efetivamente com o potencial de um grande conjunto de resultados?
-   Determinando as melhores consultas: quais tipos de consultas fornecem os resultados mais eficientes? Que tipo de consultas o desenvolvedor deve evitar?
-   Compreendendo a sintaxe de consulta: a ADSI dá suporte à sintaxe LDAP, conforme documentado em RFC 2254, bem como um subconjunto de SQL.
-   Opções de interfaces: a ADSI fornece suporte a OLE DB, bem como uma interface C/C++ chamada [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). Como o ADSI funciona para vários namespaces, você pode usar essas interfaces para consultar outros namespaces, como o Exchange, bem como Active Directory. Como o ADO (ActiveX Data Object) é um modelo de objeto de acesso a dados simples programável por scripts sobre OLE DB, as interfaces de OLE DB funcionam bem para programadores de Visual Basic e gravadores de script de página da Web. Os novos recursos de acesso a dados dentro de aplicativos do Visual Studio e do Office que aproveitam o ADO e o OLE DB agora podem acessar Active Directory dados da mesma forma que acessam dados de outros provedores de OLE DB, como o SQL Server. No entanto, se um desenvolvedor de C/C++ precisar executar uma pesquisa de diretório simples, a interface **IDirectorySearch** poderá ser mais apropriada do que as interfaces de OLE DB.

Os tópicos a seguir descrevem como Pesquisar Active Directory para garantir que seu aplicativo emita a consulta mais eficiente, considerando os requisitos do cliente:

-   [Escopo da consulta](scope-of-query.md)
-   [Desempenho e manipulação de grandes conjuntos de resultados](performance-and-handling-large-result-sets.md)
-   [Sintaxe do filtro de pesquisa](search-filter-syntax.md)
-   [Interfaces de consulta](query-interfaces.md)
-   [Pesquisando dados binários](searching-binary-data.md)
-   [Consulta Distribuída](distributed-query.md)

 

 




