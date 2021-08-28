---
title: Pesquisando o Active Directory
description: Uma função importante do Active Directory é resolver consultas de dados para pessoas, bem como dados de configuração para computadores e serviços.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Pesquisando ADSI do Active Directory
- ADSI ADSI, pesquisando Active Directory
- consultas ADSI , pesquisando Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d3ec83268556ebcacd89efeca425db87e2c0cc06e69a1e6eea810bcd6a21de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005466"
---
# <a name="searching-active-directory"></a>Pesquisando o Active Directory

Uma função importante do Active Directory é resolver consultas de dados para pessoas, bem como dados de configuração para computadores e serviços. Para escrever consultas eficientes para o Active Directory, é útil estar familiarizado com o seguinte:

-   Determinando o escopo da consulta: o cliente deve encontrar propriedades para objetos que podem estar localizados em qualquer lugar dentro de uma floresta ou apenas dentro de um domínio ou dentro de uma unidade organizacional (UO)?
-   Determinando a profundidade da consulta: a consulta deve pesquisar apenas um nível ou pode ser cruzada para outros diretórios LDAP?
-   Desempenho e manipulação de grandes conjuntos de resultados: como o cliente deve lidar efetivamente com o potencial de um conjunto de resultados grande?
-   Determinando as melhores consultas: Que tipo de consultas fornecem os resultados mais eficientes? Que tipo de consultas o desenvolvedor deve evitar?
-   Noções básicas sobre a sintaxe de consulta: a ADSI dá suporte à sintaxe LDAP, conforme documentado no RFC 2254, bem como a um subconjunto de SQL.
-   Escolha de interfaces: a ADSI fornece suporte OLE DB, bem como uma interface C/C++ chamada [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). Como a ADSI funciona para vários namespaces, você pode usar essas interfaces para consultar outros namespaces, como Exchange, bem como o Active Directory. Como o ADO (objeto de dados ActiveX) do ActiveX é um modelo de objeto de acesso a dados simples que pode ser roteado por script sobre o OLE DB, as interfaces do OLE DB funcionam bem para programadores de Visual Basic e criadores de script de página da Web. Os novos recursos de acesso a dados em aplicativos Visual Studio e Office que aproveitam o ADO e o OLE DB agora podem acessar dados do Active Directory da mesma maneira que acessam dados de outros provedores do OLE DB, como SQL Server. No entanto, se um desenvolvedor C/C++ precisar executar uma pesquisa de diretório simples, a interface **IDirectorySearch** poderá ser mais apropriada do que as interfaces OLE DB web.

Os tópicos a seguir descrevem como pesquisar no Active Directory para garantir que seu aplicativo emite a consulta mais eficiente, considerando os requisitos do cliente:

-   [Escopo da consulta](scope-of-query.md)
-   [Desempenho e manipulação de grandes conjuntos de resultados](performance-and-handling-large-result-sets.md)
-   [Sintaxe de filtro de pesquisa](search-filter-syntax.md)
-   [Interfaces de consulta](query-interfaces.md)
-   [Pesquisando dados binários](searching-binary-data.md)
-   [Consulta Distribuída](distributed-query.md)

 

 




