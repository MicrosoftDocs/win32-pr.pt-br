---
description: ICE94 verifica a tabela de atalho, a tabela de recursos e a tabela MsiAssembly e posta um aviso se houver algum atalho não anunciado apontando para um arquivo de assembly no cache de assembly global.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171139"
---
# <a name="ice94"></a>ICE94

ICE94 verifica a [tabela de atalho](shortcut-table.md), a [tabela de recursos](feature-table.md)e a [tabela MsiAssembly](msiassembly-table.md) e posta um aviso se houver algum atalho não anunciado apontando para um arquivo de assembly no cache de assembly global. Se a entrada no campo destino da tabela de atalho não for um recurso na tabela de recursos, o atalho será desanunciado. Se a entrada no campo componente \_ da tabela de atalho também estiver listada na tabela MsiAssembly, o atalho apontará para um arquivo de assembly. Se a entrada no \_ campo aplicativo de arquivo na tabela MsiAssembly estiver vazia, o arquivo de assembly estará no cache de assembly global.

## <a name="result"></a>Resultado

ICE94 posta o aviso a seguir.



| Aviso de ICE94                                                                                | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| O atalho não anunciado ' \[ 2 \] ' aponta para um arquivo de assembly no cache de assembly global. | Um atalho não anunciado está apontando para um arquivo de assembly no cache de assembly global. |



 

## <a name="example"></a>Exemplo

ICE94 relata o seguinte erro para o exemplo:

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Componente\_ | Destino    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[arquivo1\] |
| shortcut2 | c2          | feature1  |
| shortcut3 | c3          | \[file2\] |



 

[Tabela de recursos](feature-table.md) (parcial)



| Recurso  |
|----------|
| feature1 |



 

[Tabela MsiAssembly](msiassembly-table.md) (parcial)



| Componente\_ | Aplicativo de arquivo \_ |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



