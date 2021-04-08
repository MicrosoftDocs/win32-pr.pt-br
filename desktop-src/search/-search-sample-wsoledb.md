---
description: O exemplo de código WSOleDB demonstra Active Template Library (ATL) OLE DB acesso aos aplicativos do Windows Search e demonstra dois métodos adicionais para recuperar os resultados do Windows Search.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826911"
---
# <a name="wsoledb"></a>WSOleDB

O exemplo de código WSOleDB demonstra Active Template Library (ATL) OLE DB acesso aos aplicativos do Windows Search e demonstra dois métodos adicionais para recuperar os resultados do Windows Search.

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
| GitHub        | [Exemplo de WSOleDB](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.

## <a name="building-the-sample"></a>Compilando o exemplo

1. Abra o Windows Explorer e navegue até o diretório do projeto **WSOleDB** .
2. Clique duas vezes no ícone do arquivo WSOleDB. sln para abrir o projeto no Visual Studio.
  
    > [!NOTE]  
    > O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente. Isso não afetará o comportamento do exemplo.

3. No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1. Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.
2. No prompt de comando, digite `WSOleDB.exe` ou, no Windows Explorer, clique duas vezes no ícone para WSOleDB.exe.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a>Conceitual

[Visão geral da programação de OLE DB](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Outros exemplos

[Exemplos de código de pesquisa](-search-samples-ovw.md)
