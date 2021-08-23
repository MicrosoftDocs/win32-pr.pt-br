---
description: A tabela CheckBox lista os valores das caixas de seleção.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Tabela CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848769f9430681a8c37de0afd8d9d1fa8abfee2f833798ecbdc5271535f79da4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649866"
---
# <a name="checkbox-table"></a>Tabela CheckBox

A tabela CheckBox lista os valores das caixas de seleção.

A tabela CheckBox tem as seguintes colunas.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Propriedade | [Identificador](identifier.md) | Y   | N        |
| Valor    | [Formatado](formatted.md)   | N   | Y        |



 

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

Se a caixa de seleção estiver marcada, a propriedade correspondente será definida como o valor especificado. Se não houver nenhum valor especificado ou essa tabela não existir, a propriedade será definida como seu valor original quando a caixa de seleção for marcada. Se o valor original for nulo, a propriedade será definida como "1".

O conteúdo da coluna Valor é formatado pela [**função MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado. Portanto, ele pode conter qualquer expressão que a **função MsiFormatRecord** possa interpretar. A coluna Valor é formatada somente quando o controle é criado e não é atualizada se uma propriedade envolvida em uma expressão é modificada durante a vida útil do controle.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



