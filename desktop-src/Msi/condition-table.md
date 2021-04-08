---
description: A tabela de condição pode ser usada para modificar o estado de seleção de qualquer entrada na tabela de recursos com base em uma expressão condicional.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabela de condição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920720"
---
# <a name="condition-table"></a>Tabela de condição

A tabela de condição pode ser usada para modificar o estado de seleção de qualquer entrada na [tabela de recursos](feature-table.md) com base em uma expressão condicional.

A tabela de condições tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Recurso\_ | [Identificador](identifier.md) | S   | N        |
| Nível     | [Inteiro](integer.md)       | S   | N        |
| Condição | [Condição](condition.md)   | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Chave externa na coluna um da tabela de recursos.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Geral
</dt> <dd>

Um nível de instalação condicional para o recurso na \_ coluna recurso desta tabela. O instalador definirá o nível de instalação desse recurso para o nível especificado nesta coluna se a expressão na coluna condição for avaliada como TRUE.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Se essa expressão condicional for avaliada como TRUE, a coluna nível na tabela de recursos será definida como o nível de instalação condicional.

A expressão na coluna condição não deve conter referência ao estado instalado de qualquer recurso ou componente. Isso ocorre porque as expressões na coluna condição são avaliadas antes que o instalador avalie os Estados instalados de recursos e componentes. Qualquer expressão na tabela de condição que tenta verificar o estado instalado de um recurso ou componente sempre é avaliada como false.

Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Um recurso pode ser desabilitado permanentemente definindo a coluna nível como 0.

O nível pode ser definido com base em qualquer instrução condicional, como um teste para plataforma, sistema operacional ou uma configuração de propriedade específica.

As condições devem ser cuidadosamente escolhidas para que um recurso não seja habilitado na instalação e, em seguida, desabilitado na desinstalação. Isso deixará o recurso órfão e o produto não será capaz de ser desinstalado.

Essa tabela é referida quando a [ação CostFinalize](costfinalize-action.md) é executada.

Se a propriedade [**preselecionada**](preselected.md) tiver sido definida como 1, o instalador não avaliará a tabela de condições. A tabela de condição afeta apenas a instalação de recursos quando nenhuma das propriedades a seguir foi definida:

<dl>

[**ADDLOCAL**](addlocal.md)  
[**EXCLU**](remove.md)  
[**Addsource**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**Install**](reinstall.md)  
[**ANUNCI**](advertise.md)  
[**COMPADDLOCAL**](compaddlocal.md)  
[**COMPADDSOURCE**](compaddsource.md)  
[**COMPADDDEFAULT**](compadddefault.md)  
[**FILEADDLOCAL**](fileaddlocal.md)  
[**FILEADDSOURCE**](fileaddsource.md)  
[**FILEADDDEFAULT**](fileadddefault.md)  
</dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



