---
description: O exemplo de código IFilterSample demonstra como criar uma classe base IFilter para implementar a interface IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f015166d0366152d07a5fb8d182edcb5422112c66f016219970fef9b889df3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863729"
---
# <a name="ifiltersample"></a>IFilterSample

O exemplo de código IFilterSample demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

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

| Localização      | URL do caminho                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [IFilterSample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para a versão mais atualizada.

## <a name="building-the-sample"></a>Compilando o exemplo

1. abra Windows Explorer e navegue até o diretório do projeto **FilterBase** .
2. Clique duas vezes no ícone do arquivo FilterBase. sln para abrir o projeto no Visual Studio.

    > [!NOTE]  
    > o arquivo sln foi criado em uma versão mais antiga do Visual Studio, assim, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente. Isso não afetará o comportamento do exemplo.

3. No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1. navegue até o diretório que contém o novo executável, usando a janela de Prompt de comando ou Windows Explorer.
2. no prompt de comando, digite `FilterBase.exe` ou, no Windows Explorer, clique duas vezes no ícone para FilterBase.exe.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[**Visio**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Conceitual

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Outros exemplos

[Exemplos de código de pesquisa](-search-samples-ovw.md)
