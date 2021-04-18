---
description: O exemplo de código DSearch demonstra como criar uma classe para um aplicativo de console estático para consultar o Windows Search usando o assembly Microsoft. Search. Interop para ISearchQueryHelper.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813524"
---
# <a name="dsearch"></a>DSearch

O exemplo de código DSearch demonstra como criar uma classe para um aplicativo de console estático para consultar o Windows Search usando o assembly Microsoft. Search. Interop para [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).

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
| SDK do Windows | 7,0 ou superior           |

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no local a seguir.

| Local      | URL do caminho                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Exemplo de DSearch](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.

## <a name="building-the-sample"></a>Compilando o exemplo

1. Abra o Windows Explorer e navegue até o diretório do projeto **DSearch** .
2. Clique duas vezes no ícone do arquivo DSearch. sln para abrir o projeto no Visual Studio.
  
    > [!NOTE]  
    > O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente. Isso não afetará o comportamento do exemplo.

3. No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1. Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.
2. No prompt de comando, digite `DSearch.exe` ou, no Windows Explorer, clique duas vezes no ícone para DSearch.exe.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a>Outros exemplos

[Exemplos de código de pesquisa](-search-samples-ovw.md)
