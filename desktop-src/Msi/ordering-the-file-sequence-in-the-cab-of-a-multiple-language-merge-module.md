---
description: Módulos de mesclagem de vários idiomas, transformações de linguagem e arquivos de gabinete devem ser criados de forma que a ordem dos arquivos corresponda à ordem especificada na tabela de arquivos.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Ordenando a sequência de arquivos no CAB de um módulo de mesclagem de vários idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e0d7d5efc3c4599f7a3f0eecce2101d1a7db034be6e0f80eda30245a95204d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942803"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Ordenando a sequência de arquivos no CAB de um módulo de mesclagem de vários idiomas

Os módulos de mesclagem de vários idiomas, as transformações de linguagem e os arquivos de gabinete devem ser criados de forma que a ordem dos arquivos na .cab corresponda à ordem de instalação dos arquivos especificados na [tabela de arquivos](file-table.md), mesmo após a aplicação da transformação de idioma. Se a ordem no módulo e no .cab não corresponder, o módulo de mesclagem não poderá ser usado.

Atribua a cada arquivo no módulo, um número de sequência exclusivo que seja independente de seu idioma e sempre use esse número de sequência para o arquivo. Use a mesma sequência ao criar o arquivo de gabinete e criar uma transformação de idioma.

Como o instalador instala apenas os arquivos listados na [tabela de arquivos](file-table.md), o uso de uma sequência de arquivos global no gabinete, na [tabela de arquivos](file-table.md)e na transformação de linguagem permite que a ferramenta de mesclagem ignore todos os arquivos extras armazenados no gabinete que não estejam listados na tabela de [arquivos](file-table.md). Outros arquivos podem existir no gabinete, mas eles não devem estar listados na tabela de [arquivos](file-table.md). Por exemplo, um módulo que instala Code.dll, inglês. dat, alemão. dat e francês. dat pode usar a seguinte ordem de sequência de arquivos global.



| Arquivo        | Sequência |
|-------------|----------|
| Code.Dll    | 1        |
| Inglês. dat | 2        |
| Alemão. dat  | 3        |
| Francês. dat  | 4        |



 

As transformações de linguagem podem ser criadas para modificar a [tabela de arquivos](file-table.md) do módulo para inglês, alemão ou francês.

[Tabela de arquivos](file-table.md) (parcial para inglês)



| Arquivo        | Sequência |
|-------------|----------|
| Code.Dll    | 1        |
| Inglês. dat | 2        |



 

[Tabela de arquivos](file-table.md) (parcial para alemão)



| Arquivo       | Sequência |
|------------|----------|
| Code.Dll   | 1        |
| Alemão. dat | 3        |



 

[Tabela de arquivos](file-table.md) (parcial para francês)



| Arquivo       | Sequência |
|------------|----------|
| Code.Dll   | 1        |
| Francês. dat | 4        |



 

Para obter mais informações, consulte [criando uma transformação de idioma para um módulo de mesclagem de vários idiomas](authoring-a-language-transform-for-a-multiple-language-merge-module.md) e [criando tabelas de arquivos de módulo de mesclagem](authoring-merge-module-file-tables.md).

 

 



