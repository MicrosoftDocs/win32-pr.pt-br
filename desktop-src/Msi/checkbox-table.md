---
description: A tabela de caixa de seleção lista os valores para as caixas de seleção.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Tabela de caixas de seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756740"
---
# <a name="checkbox-table"></a>Tabela de caixas de seleção

A tabela de caixa de seleção lista os valores para as caixas de seleção.

A tabela de caixas de seleção tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Propriedade | [Identificador](identifier.md) | S   | N        |
| Valor    | [Binário](formatted.md)   | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

Uma propriedade nomeada a ser vinculada a este item.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

A cadeia de caracteres de valor associada a este item.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a caixa de seleção estiver marcada, a propriedade correspondente será definida como o valor especificado. Se não houver nenhum valor especificado ou essa tabela não existir, a propriedade será definida como seu valor original quando a caixa de seleção estiver marcada. Se o valor original for NULL, a propriedade será definida como "1".

O conteúdo da coluna valor é formatado pela função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado. Portanto, ele pode conter qualquer expressão que a função **MsiFormatRecord** possa interpretar. A coluna valor é formatada somente quando o controle é criado e não é atualizada se uma propriedade envolvida em uma expressão é modificada durante a vida útil do controle.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



