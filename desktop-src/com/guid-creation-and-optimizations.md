---
title: Criação e otimizações de GUID
description: Criação e otimizações de GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364397"
---
# <a name="guid-creation-and-optimizations"></a>Criação e otimizações de GUID

Como um CLSID, como um IID (identificador de interface), é um GUID, nenhuma outra classe, independentemente de quem o escreve, tem um CLSID duplicado. Os implementadores de servidor geralmente obtêm CLSIDs por meio da função [**falha em CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) . Essa função tem a garantia de produzir CLSIDs exclusivos, portanto, os implementadores de servidor em todo o mundo podem desenvolver e implantar o software de forma independente sem medo de colisão acidental com software escrito por outras pessoas.

O uso de CLSIDs exclusivos evita a possibilidade de colisões de nome entre classes porque os CLSIDs não estão de maneira alguma conectada aos nomes usados na implementação subjacente. Por exemplo, dois fornecedores diferentes podem escrever classes chamadas "StackClass", mas cada uma teria um CLSID exclusivo e, portanto, não poderia ser confundida.

COM frequência deve mapear GUIDs (IIDs e CLSIDs) para um conjunto arbitrariamente grande de outros valores. Como desenvolvedor de aplicativos, você pode ajudar a acelerar essas pesquisas e, assim, melhorar o desempenho do sistema, gerando os GUIDs para seu aplicativo como um bloco de valores consecutivos.

A maneira mais eficiente de gerar um bloco de GUIDs consecutivos é executar o utilitário Uuidgen usando as opções-n e-x, que gera um bloco de UUIDs, cada um deles cujo primeiro valor DWORD é incrementado em um.

Por exemplo, se você digitar

**Uuidgen-N5-x**

o utilitário Uuidgen geraria um bloco de UUIDs semelhante ao seguinte:

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

Um método para gerar e controlar GUIDs para um projeto inteiro começa com a geração de um bloco de um número arbitrariamente grande de UUIDs, digamos 500. Por exemplo, se você digitar

**Uuidgen-N500-x > guids.txt**

o utilitário gerará UUIDs consecutivos de 500 e os gravaria no arquivo de texto especificado. Você pode então verificar esse arquivo em sua árvore de origem, fornecendo um único repositório para todos os GUIDs a serem usados em um projeto. À medida que as pessoas exigem GUIDs para suas partes do projeto, eles podem fazer check-out do arquivo, ter vários GUIDs de que precisam, marcá-los como sendo tirados e deixar uma observação sobre onde no código ou "espec" eles estão usando-os.

Além de melhorar o desempenho do sistema, a geração de blocos de GUIDs consecutivos dessa maneira tem os seguintes benefícios:

-   Um arquivo central que contém todos os GUIDs de um aplicativo facilita o controle de quais GUIDs são para o que as pessoas estão usando.
-   Um bloco de GUIDs consecutivos associados a um aplicativo específico ajuda os desenvolvedores e testadores a reconhecer GUIDs internos durante a depuração e torna mais fácil encontrá-los no registro do sistema, pois eles são armazenados em sequência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Responsabilidades do servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 




