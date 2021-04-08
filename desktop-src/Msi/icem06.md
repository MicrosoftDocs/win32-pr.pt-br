---
description: ICEM06 verifica referências diretas inválidas para recursos pelo módulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828711"
---
# <a name="icem06"></a>ICEM06

ICEM06 verifica referências diretas inválidas para recursos pelo módulo.

O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.

## <a name="result"></a>Resultado

ICEM06 posta um erro quando o banco de dados do módulo contém referências diretas a um recurso. As informações de recurso devem ser fornecidas pelo usuário do módulo.

## <a name="example"></a>Exemplo

ICEM06 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho          | Destino                                 |
|-------------------|----------------------------------------|
| Shortcut1. *GUID1* | cmd.exe                                |
| Shortcut2. *GUID1* | \[MyProp\]                             |
| Shortcut3. *GUID1* | {00000000-0000-0000-0000-000000000000} |



 

[Tabela de classes](class-table.md) (parcial)



| CLSID   | Contexto       | Componente\_ | Recurso\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Component1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Component2  | MyFeature                              |



 

O ICEM06 relata o primeiro erro porque o primeiro registro na tabela de atalho tem uma entrada no campo de destino que não é uma propriedade ou um GUID nulo. Um módulo não pode fazer referência diretamente a um recurso. As informações de recurso devem ser fornecidas pelo usuário do módulo. Para corrigir esse erro, as referências a um recurso devem ser substituídas por um GUID nulo.

ICEM06 relata o segundo erro porque o segundo registro na tabela de classes tem uma entrada no campo de recurso que não é um GUID nulo. Um módulo não pode fazer referência diretamente a um recurso. As informações de recurso devem ser fornecidas pelo usuário do módulo. Para corrigir esse erro, as referências a um recurso devem ser substituídas por um GUID nulo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



