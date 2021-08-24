---
description: ICEM06 verifica se há referências diretas inválidas aos recursos pelo módulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5150e511e6f8018e51ab537b52ccc6c32645d09c80110129f040d6a329335ec5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828876"
---
# <a name="icem06"></a>ICEM06

ICEM06 verifica se há referências diretas inválidas aos recursos pelo módulo.

Os ICEs do módulo de mesclagem são armazenados em um arquivo .cú do módulo de mesclagem chamado Mergemod.plus e não no arquivo .file que contém os ICEs usados para validação do pacote.

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
| Atalho1. *GUID1* | cmd.exe                                |
| Shortcut2. *GUID1* | \[MyProp\]                             |
| Atalho 3. *GUID1* | {00000000-0000-0000-0000-000000000000} |



 

[Tabela de Classe](class-table.md) (parcial)



| CLSID   | Contexto       | Componente\_ | Recurso\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Component1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Component2  | MyFeature                              |



 

ICEM06 relata o primeiro erro porque o primeiro registro na tabela Atalho tem uma entrada no campo Destino que não é uma propriedade ou um GUID nulo. Um módulo não pode referenciar um recurso diretamente. As informações de recurso devem ser fornecidas pelo usuário do módulo. Para corrigir esse erro, as referências a um recurso devem ser substituídas por um GUID nulo.

ICEM06 relata o segundo erro porque o segundo registro na tabela Classe tem uma entrada no campo Recurso que não é um GUID nulo. Um módulo não pode referenciar um recurso diretamente. As informações de recurso devem ser fornecidas pelo usuário do módulo. Para corrigir esse erro, as referências a um recurso devem ser substituídas por um GUID nulo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência ice do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



