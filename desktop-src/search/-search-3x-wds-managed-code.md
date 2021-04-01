---
description: O SDK do Windows Search fornece um assembly de interoperabilidade para que você trabalhe com objetos Component Object Model (COM) expostos pelo Windows Search e outros programas em relação às interfaces e classes usando código gerenciado.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Usar código gerenciado com os dados do Shell e do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090100"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>Usar código gerenciado com os dados do Shell e do Windows Search

O SDK do Windows Search fornece um assembly de interoperabilidade para que você trabalhe com objetos Component Object Model (COM) expostos pelo Windows Search e outros programas em relação às interfaces e classes usando código gerenciado. O assembly de interoperabilidade é assinado digitalmente pela Microsoft e pode ser encontrado com os [exemplos do Windows Search](-search-samples-ovw.md).

Este tópico é organizado da seguinte maneira:

-   [Usando a API do Windows CodePack](#using-the-windows-api-codepack)
    -   [Acessando resultados de índice](#accessing-index-results)
    -   [Aplicativo de exemplo usando a API do Windows Codepack](#sample-application-using-the-windows-api-codepack)
-   [Tópicos relacionados](#related-topics)

## <a name="using-the-windows-api-codepack"></a>Usando a API do Windows CodePack

Se você estiver trabalhando no ambiente de Microsoft .NET, use o [pacote de código da API do Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) para obter resultados da pesquisa ou apenas procure o namespace. O [pacote de códigos da API do Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) fornece uma coleção de itens de shell que são essencialmente invólucros em relação à [interface IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)nativa. Você pode iterar sobre essa coleção e obter os vários valores de propriedade de maneira semelhante a como você enumeraria os resultados em uma tabela de uma consulta de vinculação de objeto e de banco de dados de incorporação (OLE DB).

O trecho de código a seguir ilustra como iterar em itens de pesquisa e obter os valores de propriedade para cada um.


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>Acessando resultados de índice

Você pode acessar os resultados do índice por meio de OLE DB ou do modelo de dados do Shell. Há vantagens e desvantagens com qualquer abordagem. Uma vantagem é que OLE DB e linguagem SQL (SQL) são familiares aos programadores de banco de dados. Outras vantagens são um melhor controle sobre o desempenho ao consultar apenas o indexador e o acesso a funcionalidades adicionais, como a capacidade de localizar resultados anteriores em um novo conjunto de linhas rapidamente.

As vantagens do modelo de dados do shell são que elas são abstratas em diferentes fontes de informações, como OpenSearch, e fornecem acesso a funcionalidades adicionais, como miniaturas e manipuladores de propriedades. Nem o modelo de objeto do Shell requer suporte de caso especial para resultados que não sejam de nome de arquivo, como itens de email e resultados do OneNote, nem para qualquer item que resida no índice do usuário. Observe que no Shell [KNOWNFOLDERID](../shell/knownfolderid.md) é o escopo de pasta conhecido para conteúdo indexado local. Para obter mais informações sobre como criar uma fonte de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

As fontes de dados OpenSearch não são expostas por meio de OLE DB para pesquisa federada no Windows 7 e posterior. Por esse motivo, recomendamos que você considere escrever um provedor LINQ para o namespace do Shell em vez de usar OLE DB para acessar os resultados do indexador. Para obter mais informações, consulte [Walkthrough: Criando um provedor de LINQ do IQueryable](/previous-versions/bb546158(v=vs.140)).

### <a name="sample-application-using-the-windows-api-codepack"></a>Aplicativo de exemplo usando a API do Windows Codepack

A captura de tela a seguir representa uma simulação de um aplicativo de exemplo criado com o [pacote de códigos de API do Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).

![captura de tela do aplicativo player de mídia mostrando mensagens de email](images/folderid-searchhome.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Interoperabilidade em qualquer idioma](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))
</dt> </dl>

 

 
