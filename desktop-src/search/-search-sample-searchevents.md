---
description: O exemplo de código SearchEvents demonstra como priorizar eventos de indexação.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788936"
---
# <a name="searchevents"></a>SearchEvents

O exemplo de código SearchEvents demonstra como priorizar eventos de indexação.

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
| GitHub        | [Exemplo de SearchEvents](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.

## <a name="building-the-sample"></a>Compilando o exemplo

1. Abra o Windows Explorer e navegue até o diretório do projeto **SearchEvents** .
2. Clique duas vezes no ícone do arquivo Eventing. sln para abrir o projeto no Visual Studio.
  
    > [!NOTE]  
    > O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente. Isso não afetará o comportamento do exemplo.

3. No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1. Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.
2. No prompt de comando, digite `Eventing.exe` ou, no Windows Explorer, clique duas vezes no ícone para Eventing.exe.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[**nível de prioridade \_**](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[**tipo de ROWSETEVENT \_**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a>Outros exemplos

[Exemplos de código de pesquisa](-search-samples-ovw.md)
