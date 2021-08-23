---
title: Criação e otimizações de GUID
description: Criação e otimizações de GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dc1b0cc52312768759daca35824f8e7e515629131ac2c301a17d7ae99d6455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731426"
---
# <a name="guid-creation-and-optimizations"></a>Criação e otimizações de GUID

Como um CLSID, como um IID (identificador de interface), é um GUID, nenhuma outra classe, independentemente de quem o grava, tem um CLSID duplicado. Os implementadores de servidor geralmente obtém CLSIDs por meio da [**função CoCreateGuid.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) Essa função tem a garantia de produzir CLSIDs exclusivas, de modo que os implementadores de servidor em todo o mundo possam desenvolver e implantar seu software de forma independente sem medo de colisão acidental com software escrito por outras pessoas.

O uso de CLSIDs exclusivos evita a possibilidade de colisões de nomes entre classes, pois as CLSIDs não estão conectadas aos nomes usados na implementação subjacente. Por exemplo, dois fornecedores diferentes podem escrever classes chamadas "StackClass", mas cada um teria um CLSID exclusivo e, portanto, não poderia ser confundido.

COM frequentemente deve mapear GUIDs (IIDs e CLSIDs) para algum conjunto arbitrariamente grande de outros valores. Como desenvolvedor de aplicativos, você pode ajudar a acelerar essas pesquisas e, assim, aprimorar o desempenho do sistema, gerando os GUIDs para seu aplicativo como um bloco de valores consecutivos.

A maneira mais eficiente de gerar um bloco de GUIDs consecutivos é executar o utilitário uuidgen usando as opções -n e -x, que gera um bloco de UUIDs, cada um cujo primeiro valor DWORD é incrementado em um.

Por exemplo, se você digitar

**uuidgen -n5 -x**

o utilitário uuidgen geraria um bloco de UUIDs semelhante ao seguinte:

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

Um método para gerar e acompanhar GUIDs para um projeto inteiro começa com a geração de um bloco de um número arbitrariamente grande de UUIDs, digamos, 500. Por exemplo, se você digitar

**uuidgen -n500 -x > guids.txt**

O utilitário geraria 500 UUIDs consecutivos e os gravaria no arquivo de texto especificado. Em seguida, você pode verificar esse arquivo em sua árvore de origem, fornecendo um único repositório para que todos os GUIDs sejam usados em um projeto. Como as pessoas exigem GUIDs para suas partes do projeto, elas podem fazer check-out do arquivo, usar quantos GUIDs elas precisam, marcando-as como tomadas e deixando uma observação sobre onde no código ou "especificação" eles estão usando.

Além de melhorar o desempenho do sistema, a geração de blocos de GUIDs consecutivos dessa maneira tem os seguintes benefícios:

-   Um arquivo central que contém todos os GUIDs de um aplicativo facilita o controle de quais GUIDs são para o que e quais pessoas os estão usando.
-   Um bloco de GUIDs consecutivos associados a um aplicativo específico ajuda desenvolvedores e testadores a reconhecer GUIDs internos durante a depuração e torna mais fácil encontrá-los no registro do sistema porque eles são armazenados sequencialmente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Responsabilidades do servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 




