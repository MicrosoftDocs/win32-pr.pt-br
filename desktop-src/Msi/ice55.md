---
description: ICE55 valida que todos os objetos LockPermission existem e têm valores de permissão válidos.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170840"
---
# <a name="ice55"></a>ICE55

ICE55 valida que todos os objetos LockPermission existem e têm valores de permissão válidos.

## <a name="result"></a>Resultado

ICE55 poste um erro se um lockobject listado na [Tabela LockPermissions](lockpermissions-table.md) não existir ou se nenhum nível de privilégio for especificado na coluna permissão.

## <a name="example"></a>Exemplo

ICE55 relataria os erros a seguir para o exemplo.

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[Tabela LockPermissions](lockpermissions-table.md) (parcial)



| LockObject | Tabela | Domínio | Usuário  | Permissão |
|------------|-------|--------|-------|------------|
| Arquivo1      | Arquivo  |        | guest |            |
| Arquivo3      | Arquivo  |        | guest | 1          |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Versão | Idioma |
|-------|---------|----------|
| Arquivo1 | Arquivo2   |          |
| Arquivo2 | 1.0.0.0 | 1046     |



 

O objeto arquivo1 tem um nulo na coluna de permissão. Cada linha deve ter um valor na coluna permissões. Para corrigir esse erro, especifique um valor numérico nesta coluna. Se nenhum privilégio for necessário para esse objeto, você deverá remover a linha.

O objeto arquivo3 descrito na Tabela LockPermissions não está listado na tabela de arquivos. Para corrigir esse erro, consulte um objeto válido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



