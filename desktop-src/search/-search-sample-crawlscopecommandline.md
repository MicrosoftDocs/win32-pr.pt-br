---
description: O exemplo de código CrawlScopeCommandLine demonstra como definir opções de linha de comando para operações de indexação Gerenciador do Escopo de Rastreamento (CSM).
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: CrawlScopeCommandLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4ed7100400593491b5ab75653bfe316267bc9cf82bd37a089118deb0f5a348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051936"
---
# <a name="crawlscopecommandline"></a>CrawlScopeCommandLine

O exemplo de código CrawlScopeCommandLine demonstra como definir opções de linha de comando para operações de indexação Gerenciador do Escopo de Rastreamento (CSM).

Este tópico inclui as seções a seguir.

- [Requirements](#requirements)
- [Baixando o exemplo](#downloading-the-sample)
- [Compilando o exemplo](#building-the-sample)
- [Executando o exemplo](#running-the-sample)
- [Tópicos relacionados](#related-topics)

## <a name="requirements"></a>Requisitos

| Produto     | Versão do produto          |
|-------------|--------------------------|
| Windows     | no Windows 7, 8.1 ou 10    |
| SDK do Windows | 7.0 ou superior           |

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no local a seguir.

| Localização | Caminho ou URL                                                                |
|----------|----------------------------------------------------------------------------|
| GitHub   |    [Exemplo de CrawlScopeCommandLine](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> Para todas as versões do Windows, incluindo Windows 7, é recomendável baixar os exemplos diretamente do GitHub para a versão mais atualizada.

## <a name="building-the-sample"></a>Compilando o exemplo

1. Abra Windows Explorer e navegue até o diretório do projeto **CrawlScopeCommandLine.**
2. Clique duas vezes no ícone do arquivo csmcmd.sln para abrir o projeto Visual Studio.
  
    > [!NOTE]  
    > O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, atualizando-o será necessário se você estiver executando o Visual Studio 2012 ou mais recente. Isso não afetará o comportamento do exemplo.

3. No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1. Navegue até o diretório que contém o novo executável, usando a janela prompt de comando ou Windows Explorer.
2. No prompt de comando, insira ou, Windows Explorer, clique duas vezes `csmcmd.exe` no ícone para csmcmd.exe.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a>Outros exemplos

[Exemplos de código de pesquisa](-search-samples-ovw.md)
