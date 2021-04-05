---
description: A tabela ControlCondition permite que um autor especifique ações especiais a serem aplicadas a controles com base no resultado de uma instrução condicional. Por exemplo, usando essa tabela, o autor pode optar por ocultar um controle com base na propriedade VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Tabela ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922138"
---
# <a name="controlcondition-table"></a>Tabela ControlCondition

A tabela ControlCondition permite que um autor especifique ações especiais a serem aplicadas a controles com base no resultado de uma instrução condicional. Por exemplo, usando essa tabela, o autor pode optar por ocultar um controle com base na propriedade [**VersionNT**](versionnt.md) .

A tabela ControlCondition tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| caixa de diálogo\_  | [Identificador](identifier.md) | S   | N        |
| controle\_ | [Identificador](identifier.md) | S   | N        |
| Ação    | [Text](text.md)             | S   | N        |
| Condição | [Condição](condition.md)   | S   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>'\_
</dt> <dd>

Uma chave externa para a primeira coluna da [tabela de diálogo](dialog-table.md). A combinação desse campo com o \_ campo de controle identifica um controle exclusivo.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controlo\_
</dt> <dd>

Uma chave externa para a segunda coluna da [tabela de controle](control-table.md). Combinando este campo, o campo de caixa de diálogo \_ identifica um controle exclusivo.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

A ação a ser executada no controle. As ações possíveis são mostradas na tabela a seguir.



| Valor   | Significado                     |
|---------|-----------------------------|
| Padrão | Defina o controle como o padrão. |
| Desabilitar | Desabilite o controle.        |
| Habilitar  | Habilite o controle.         |
| Ocultar    | Ocultar o controle.           |
| Mostrar    | Exibir o controle.        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Uma instrução condicional que especifica sob quais condições a ação deve ser disparada. Esta coluna não pode ser deixada em branco. Se essa instrução não for avaliada como TRUE, a ação não ocorrerá. Se estiver definido como 1, a ação sempre será aplicada. Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você quiser ocultar e desabilitar um controle de [pressão](pushbutton-control.md) ou [controle de caixa de seleção](checkbox-control.md) com base em uma instrução condicional no campo condição da tabela ControlCondition, deverá usar quatro registros para cada controle para desabilitar e ocultar o controle. Os controles de pressão ou caixa de seleção que só foram ocultos ainda podem ser acessados por teclas de atalho.

Por exemplo, os seguintes registros ocultam e desabilitam o ControlA na caixa de diálogo quando o produto é instalado. O controle ficará visível e habilitado quando o produto não estiver instalado.



| caixa de diálogo  | Control  | Ação  | Condição                      |
|---------|----------|---------|--------------------------------|
| Caixa de diálogo | ControlA | Ocultar    | [**Instalado**](installed.md) |
| Caixa de diálogo | ControlA | Desabilitar | Instalado                      |
| Caixa de diálogo | ControlA | Mostrar    | NÃO instalado                  |
| Caixa de diálogo | ControlA | Habilitar  | NÃO instalado                  |



 

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



