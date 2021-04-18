---
description: O exemplo de código StructuredQuerySample demonstra como ler linhas do console, analisá-las usando o esquema do sistema e exibir as árvores de condição resultantes.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760495"
---
# <a name="structuredquerysample"></a>StructuredQuerySample

O exemplo de código StructuredQuerySample demonstra como ler linhas do console, analisá-las usando o esquema do sistema e exibir as árvores de condição resultantes.

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
| GitHub        | [StructuredQuerySample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.

## <a name="building-the-sample"></a>Compilando o exemplo

1. Abra o Windows Explorer e navegue até o diretório do projeto **StructuredQuerySample** .
2. Clique duas vezes no ícone do arquivo StructuredQuerySample. sln para abrir o projeto no Visual Studio.

    > [!NOTE]  
    > O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente. Isso não afetará o comportamento do exemplo.

3. No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1. Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.
2. No prompt de comando, digite `StructuredQuerySample.exe` ou, no Windows Explorer, clique duas vezes no ícone para StructuredQuerySample.exe.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[**IQueryParserManager**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a>Outros exemplos

[Exemplos de código de pesquisa](-search-samples-ovw.md)
