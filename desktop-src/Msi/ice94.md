---
description: ICE94 verifica a tabela Atalho, a Tabela de recursos e a tabela MsiAssembly e posta um aviso se há atalhos não revertidos apontando para um arquivo de assembly no cache de assembly global.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd203fe35b6bedc7d36f3e5a5c18fc6a235d3e65924b41909803e67ab79337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894886"
---
# <a name="ice94"></a>ICE94

ICE94 verifica a [](feature-table.md)tabela atalho [,](shortcut-table.md)a tabela De recursos e a tabela [MsiAssembly](msiassembly-table.md) e posta um aviso se há atalhos não revertidos apontando para um arquivo de assembly no cache de assembly global. Se a entrada no campo Destino da tabela Atalho não for um recurso na tabela Recurso, o atalho não será revertido. Se a entrada no campo Componente da tabela Atalho também estiver listada na tabela \_ MsiAssembly, o atalho aponta para um arquivo de assembly. Se a entrada no campo Aplicativo de Arquivo na \_ tabela MsiAssembly estiver vazia, o arquivo de assembly está no cache de assembly global.

## <a name="result"></a>Resultado

ICE94 posta o aviso a seguir.



| Aviso ICE94                                                                                | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| O atalho não anunciado ' \[ 2 \] ' aponta para um arquivo de assembly no cache de assembly global. | Um atalho não revertido está apontando para um arquivo de assembly no cache de assembly global. |



 

## <a name="example"></a>Exemplo

ICE94 relata o seguinte erro para o exemplo:

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Componente\_ | Destino    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[file1\] |
| shortcut2 | c2          | feature1  |
| shortcut3 | c3          | \[file2\] |



 

[Tabela de recursos](feature-table.md) (parcial)



| Recurso  |
|----------|
| feature1 |



 

[Tabela MsiAssembly](msiassembly-table.md) (parcial)



| Componente\_ | Aplicativo de \_ arquivo |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



