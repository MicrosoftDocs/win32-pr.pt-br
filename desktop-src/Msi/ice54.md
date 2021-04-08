---
description: O ICE54 verifica os componentes que usam um arquivo complementar como seu caminho de chave.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828568"
---
# <a name="ice54"></a>ICE54

O ICE54 verifica os componentes que usam um arquivo complementar como seu caminho de chave.

O arquivo de caminho de chave de um componente não deve derivar sua versão de um arquivo diferente. Isso pode fazer com que alguns arquivos falhem na instalação. Consulte a [tabela de arquivos](file-table.md) para obter mais informações sobre arquivos complementares.

## <a name="result"></a>Resultado

ICE54 posta um aviso se algum componente tiver um arquivo de caminho de chave que derive sua versão de outro arquivo.

## <a name="example"></a>Exemplo

ICE54 retorna o seguinte aviso para o exemplo mostrado.

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Atributo | KeyPath |
|------------|-----------|---------|
| Component1 | 0         | Arquivo1   |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Versão | Idioma |
|-------|---------|----------|
| Arquivo1 | Arquivo2   |          |
| Arquivo2 | 1.0.0.0 | 1046     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



