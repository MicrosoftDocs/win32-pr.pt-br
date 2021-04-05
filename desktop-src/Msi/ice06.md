---
description: O ICE06 verifica todas as tabelas para validar se todas as colunas listadas na \_ tabela de validação estão presentes na tabela. Se uma tabela não existir, todas \_ as entradas de validação para essa tabela serão ignoradas.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922025"
---
# <a name="ice06"></a>ICE06

O ICE06 verifica todas as tabelas para validar se todas as colunas listadas na [ \_ tabela de validação](-validation-table.md) estão presentes na tabela. Se uma tabela não existir, todas \_ as entradas de validação para essa tabela serão ignoradas.

A finalidade do ICE06 é detectar instâncias nas quais um autor tenta usar uma nova tabela de \_ validação que reflete uma alteração de esquema com um banco de dados antigo que não foi atualizado. ICE06 também detecta o caso inverso de uma \_ tabela de validação antiga que está sendo usada com um banco de dados alterado.

Observe que a validação interna executada pelo [ICE03](ice03.md) captura a instância de uma coluna de tabela não definida na \_ tabela de validação que está sendo listada no catálogo de colunas. O uso de ICE03 e ICE06, portanto, garante que todas as colunas no banco de dados sejam testadas.

## <a name="result"></a>Resultado

ICE06 posta um erro quando há uma coluna de tabela definida na \_ tabela de validação que não está listada na \_ tabela colunas.

## <a name="example"></a>Exemplo

Para o exemplo a seguir, o ICE06 posta a mensagem

A coluna: versão da tabela: ModuleSignature não está definida no banco de dados.

[ \_ Tabela de validação](-validation-table.md) (parcial)



| Tabela           | Coluna   |
|-----------------|----------|
| ModuleSignature | ModuleID |
| ModuleSignature | Versão  |



 

[ \_ Tabela de colunas](-columns-table.md) (parcial)



| Tabela           | Número | Nome     |
|-----------------|--------|----------|
| ModuleSignature | 1      | ModuleID |



 

A coluna versão da tabela ModuleSignature não está no banco de dados ou está listada na \_ tabela colunas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



