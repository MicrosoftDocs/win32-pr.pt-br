---
description: 'O exemplo de código ReindexMatchingUrls demonstra como fornecer três maneiras de especificar os arquivos a serem reindexados: URLs que correspondem a um tipo de arquivo, tipo MIME ou uma cláusula WHERE especificada.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: ReindexMatchingUrls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460984"
---
# <a name="reindexmatchingurls"></a>ReindexMatchingUrls

O exemplo de código ReindexMatchingUrls demonstra como fornecer três maneiras de especificar os arquivos a serem reindexados: URLs que correspondem a um tipo de arquivo, tipo MIME ou uma cláusula WHERE especificada.

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

| Local      | URL do caminho                                                                      |
|---------------|-------------------------------------------------------------------------------|
| GitHub  | [Exemplo de ReindexMatchingUrls](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.

## <a name="building-the-sample"></a>Compilando o exemplo

1. Abra o Windows Explorer e navegue até o diretório do projeto **ReindexMatchingUrls** . Por exemplo, o caminho de instalação padrão completo é `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .
2. Clique duas vezes no ícone do arquivo REINDEX. sln para abrir o projeto no Visual Studio.
  
    > [!NOTE]  
    > O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente. Isso não afetará o comportamento do exemplo.

3. No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1. Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.
2. No prompt de comando, digite `Reindex.exe` ou, no Windows Explorer, clique duas vezes no ícone para Reindex.exe.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[**ISearchViewChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[**PRIORIZAr \_ sinalizadores**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a>Outros exemplos

[Exemplos de código de pesquisa](-search-samples-ovw.md)
