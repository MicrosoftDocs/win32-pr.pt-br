---
description: A tabela LaunchCondition é usada pela ação LaunchConditions. Ele contém uma lista de condições que devem ser satisfeitas para que a instalação seja iniciada.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Tabela LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782788"
---
# <a name="launchcondition-table"></a>Tabela LaunchCondition

A tabela LaunchCondition é usada pela [ação LaunchConditions](launchconditions-action.md). Ele contém uma lista de condições que devem ser satisfeitas para que a instalação seja iniciada.

A tabela LaunchCondition tem as colunas a seguir.



| Coluna      | Tipo                       | Chave | Nullable |
|-------------|----------------------------|-----|----------|
| Condição   | [Condição](condition.md) | S   | N        |
| Descrição | [Binário](formatted.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Expressão que deve ser avaliada como true para que a instalação seja iniciada.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Texto localizável para exibir quando a condição falha e a instalação deve ser encerrada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você não pode garantir a ordem na qual as condições de inicialização são avaliadas por meio da criação desta tabela. Se for necessário controlar a ordem em que as condições são avaliadas, você deve fazer isso usando ações personalizadas do tipo de ação personalizada 19 em sua instalação.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



