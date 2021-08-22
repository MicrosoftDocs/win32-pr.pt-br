---
description: A tabela Condição pode ser usada para modificar o estado de seleção de qualquer entrada na tabela Recurso com base em uma expressão condicional.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabela de condição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d9ccb265d69f99a58e155657a0e9d058ba61a920088184ec2b67c3e4506a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926956"
---
# <a name="condition-table"></a>Tabela de condição

A tabela Condição pode ser usada para modificar o estado de seleção de qualquer entrada na tabela [Recurso](feature-table.md) com base em uma expressão condicional.

A tabela Condição tem as seguintes colunas.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Recurso\_ | [Identificador](identifier.md) | Y   | N        |
| Nível     | [Inteiro](integer.md)       | Y   | N        |
| Condição | [Condição](condition.md)   | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Chave externa na coluna um da tabela Recurso.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Nível
</dt> <dd>

Um nível de instalação condicional para o recurso na coluna \_ Recurso desta tabela. O instalador define o nível de instalação desse recurso para o nível especificado nesta coluna se a expressão na coluna Condição for avaliada como TRUE.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condição
</dt> <dd>

Se essa expressão condicional for avaliada como TRUE, a coluna Nível na tabela Recurso será definida como o nível de instalação condicional.

A expressão na coluna Condição não deve conter referência ao estado instalado de nenhum recurso ou componente. Isso porque as expressões na coluna Condição são avaliadas antes que o instalador avalie os estados instalados de recursos e componentes. Qualquer expressão na tabela Condição que tenta verificar o estado instalado de um recurso ou componente sempre é avaliada como false.

Para obter informações sobre a sintaxe de instruções condicionais, consulte [Sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Um recurso pode ser desabilitado permanentemente definindo a coluna Nível como 0.

O Nível pode ser definido com base em qualquer instrução condicional, como um teste para plataforma, sistema operacional ou uma configuração de propriedade específica.

As condições devem ser cuidadosamente escolhidas para que um recurso não seja habilitado na instalação e desabilitado na desinstalação. Isso fará com que o recurso seja órfão e o produto não poderá ser desinstalado.

Essa tabela é referenciada quando a [ação CostFinalize](costfinalize-action.md) é executada.

Se a [**propriedade Pré-selecionada**](preselected.md) tiver sido definida como 1, o instalador não avaliará a tabela Condição. A tabela Condição afeta apenas a instalação de recursos quando nenhuma das seguintes propriedades foi definida:

<dl>

[**ADDLOCAL**](addlocal.md)  
[**Remover**](remove.md)  
[**ADDSOURCE**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**Reinstalar**](reinstall.md)  
[**Anunciar**](advertise.md)  
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

 

 



