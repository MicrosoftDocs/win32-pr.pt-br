---
description: ICE06 verifica todas as tabelas para validar se todas as colunas listadas na tabela \_ Validação estão presentes na tabela. Se uma tabela não existir, todas as \_ entradas de Validação dessa tabela serão ignoradas.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febccd205b78e90d3dac49f88d0750f803c8cd575b6b76b46cab79a684deea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142564"
---
# <a name="ice06"></a>ICE06

ICE06 verifica todas as tabelas para validar se todas as colunas listadas na tabela [ \_ Validação](-validation-table.md) estão presentes na tabela. Se uma tabela não existir, todas as \_ entradas de Validação dessa tabela serão ignoradas.

A finalidade do ICE06 é detectar instâncias em que um autor tenta usar uma nova tabela validação que reflete uma alteração de esquema com um banco de dados antigo que não \_ foi atualizado. O ICE06 também detecta o caso inverso de uma tabela de validação antiga que \_ está sendo usada com um banco de dados alterado.

Observe que a validação interna executada pelo [ICE03](ice03.md) captura a instância de uma coluna de tabela não definida na tabela Validação que está sendo listada \_ no catálogo de colunas. Portanto, o uso de ICE03 e ICE06 garante que cada coluna no banco de dados seja testada.

## <a name="result"></a>Resultado

ICE06 posta um erro quando há uma coluna de tabela definida na tabela Validação que não \_ está listada na \_ tabela Colunas.

## <a name="example"></a>Exemplo

Para o exemplo a seguir, ICE06 posta a mensagem

Coluna: Versão da Tabela: ModuleSignature não está definida no banco de dados.

[ \_ Tabela de validação](-validation-table.md) (parcial)



| Tabela           | Coluna   |
|-----------------|----------|
| Modulesignature | ModuleID |
| Modulesignature | Versão  |



 

[ \_ Tabela de colunas](-columns-table.md) (parcial)



| Tabela           | Número | Nome     |
|-----------------|--------|----------|
| Modulesignature | 1      | ModuleID |



 

A coluna Versão da tabela ModuleSignature não está no banco de dados ou está listada na \_ tabela Colunas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



