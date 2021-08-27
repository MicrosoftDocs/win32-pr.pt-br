---
description: Os desenvolvedores Windows pacotes do Instalador podem optar por usar um tipo de ação personalizada 19 quando as ações padrão não são suficientes para executar a instalação.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo de ação personalizada 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cbbef4ec07d805e41c0de25c371f995782ce3d8df66a89ee93363afa05f55b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075056"
---
# <a name="custom-action-type-19"></a>Tipo de ação personalizada 19

Essa ação personalizada exibe uma mensagem de erro especificada, retorna a falha e, em seguida, encerra a instalação. A mensagem de erro exibida pode ser fornecida como uma cadeia de caracteres ou como um índice na [tabela Erro](error-table.md).

## <a name="source"></a>Fonte

Deixe a coluna Origem da tabela [CustomAction em](customaction-table.md) branco.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna Tipo da tabela CustomAction para especificar o tipo numérico básico.



| Constantes                                                               | Hexadecimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>Destino

A coluna Destino da tabela [CustomAction](customaction-table.md) contém uma cadeia de caracteres de texto formatada usando a funcionalidade especificada em [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sem os especificadores de campo numérico). Os parâmetros a serem substituídos são incluídos entre colchetes, ... e podem ser propriedades, variáveis de ambiente (prefixo%), caminhos de arquivo ( prefixo) ou caminhos de diretório de componente \[ \] \# (prefixo$ ). Se depois de formatar a cadeia de caracteres for avaliada como um inteiro, esse inteiro será usado como um índice na tabela [Erro](error-table.md) para recuperar a mensagem a ser exibida. Se depois de formatar a cadeia de caracteres contiver caracteres não numéricos, a própria cadeia de caracteres será exibida como a mensagem.

## <a name="return-processing-options"></a>Opções de processamento de retorno

A ação personalizada não usa nenhuma opção.

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

A ação personalizada não usa nenhuma opção.

## <a name="in-script-execution-options"></a>In-Script de execução

A ação personalizada não usa nenhuma opção.

## <a name="return-values"></a>Valores de retorno

Consulte [Valores de retorno de ação personalizada.](custom-action-return-values.md)

## <a name="remarks"></a>Comentários

Por exemplo, as ações personalizadas CAError1, CAError2, CAError3 e CAError4 retornam essas mensagens.

[Tabela CustomAction](customaction-table.md)



| Ação   | Tipo | Fonte | Destino                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Prop1\]                           |
| CAError2 | 19   |        | Falha na instalação devido ao Erro2. |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[Prop2\]                           |



 

[Tabela de propriedades](property-table.md)



| Propriedade | Valor                                 |
|----------|---------------------------------------|
| Prop1    | "Falha na instalação devido ao Erro1." |
| Prop2    | "25100"                               |



 

[Tabela de erros](error-table.md)



| Código  | Mensagem                             |
|-------|-------------------------------------|
| 25000 | Falha na instalação devido ao Erro3. |
| 25100 | Falha na instalação devido ao Erro4. |



 

Essas ações personalizadas retornam as seguintes mensagens de erro:



| Ação personalizada | Cadeia de caracteres de mensagem retornada             |
|---------------|-------------------------------------|
| CAError1      | Falha na instalação devido a Error1. |
| CAError2      | Falha na instalação devido ao Erro2. |
| CAError3      | Falha na instalação devido ao Erro3. |
| CAError4      | Falha na instalação devido ao Erro4. |



 

Observe que, como a ordem de avaliação das condições de lançamento não pode ser garantida com a publicação da tabela [LaunchCondition](launchcondition-table.md), você deve usar ações personalizadas do Tipo de Ação Personalizada 19 em sua instalação para avaliar condições em uma ordem específica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ações \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



