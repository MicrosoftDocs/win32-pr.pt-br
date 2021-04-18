---
description: O exemplo de código OpenSearch demonstra como criar um serviço de pesquisa federado usando o protocolo OpenSearch e um arquivo de descritor de OpenSearch (. osdx) (um conector de pesquisa).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370620"
---
# <a name="opensearch"></a>OpenSearch

O exemplo de código OpenSearch demonstra como criar um serviço de pesquisa federado usando o protocolo [OpenSearch](https://github.com/dewitt/opensearch) e um arquivo de descritor de OpenSearch (. osdx) (um conector de pesquisa).

Este tópico inclui as seções a seguir.

-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Produto     | Versão mínima do produto |
|-------------|-------------------------|
| Windows     | Windows 7               |
| SDK do Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local      | URL do caminho                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Exemplo de OpenSearch](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.

 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **AdventureSearch** . 
2.  Digite `msbuild AdventureSearch.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **AdventureSearch** .
2.  Clique duas vezes no ícone do arquivo AdventureSearch. sln para abrir o projeto no Visual Studio.
    > [!Note]  
    > A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão. Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".

     

3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.
2.  No prompt de comando, digite `AdventureSearch.exe` ou, no Windows Explorer, clique duas vezes no ícone para AdventureSearch.exe.
3.  No prompt de comando, digite `GetOSDX.exe` ou, no Windows Explorer, clique duas vezes no ícone para GetOSDX.exe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Visão geral do esquema de descrição do conector de pesquisa](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Exemplos de código de pesquisa](-search-samples-ovw.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Esquema de descrição da biblioteca](../shell/library-schema-entry.md)
</dt> </dl>

 

 
