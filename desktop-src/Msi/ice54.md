---
description: ICE54 verifica se há componentes que usam um arquivo de adoção como seu caminho de chave.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00658bb62b5c29b25f9fb653e216920fc776ba6df0e3fc2f8b47bbdf715040b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946603"
---
# <a name="ice54"></a>ICE54

ICE54 verifica se há componentes que usam um arquivo de adoção como seu caminho de chave.

O arquivo de caminho de chave de um componente não deve derivar sua versão de um arquivo diferente. Isso pode fazer com que alguns arquivos falhem na instalação. Consulte a [tabela Arquivo para](file-table.md) obter mais informações sobre arquivos adicionais.

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

 

 



