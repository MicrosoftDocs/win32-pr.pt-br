---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 19 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo de ação personalizada 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787504"
---
# <a name="custom-action-type-19"></a>Tipo de ação personalizada 19

Essa ação personalizada exibe uma mensagem de erro especificada, retorna falha e, em seguida, encerra a instalação. A mensagem de erro exibida pode ser fornecida como uma cadeia de caracteres ou como um índice na [tabela de erros](error-table.md).

## <a name="source"></a>Fonte

Deixe a coluna de origem da [tabela CustomAction](customaction-table.md) em branco.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna tipo da tabela CustomAction para especificar o tipo numérico básico.



| Constantes                                                               | Hexadecimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>Destino

A coluna Target da [tabela CustomAction](customaction-table.md) contém uma cadeia de texto formatada usando a funcionalidade especificada em [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sem os especificadores de campo numérico). Os parâmetros a serem substituídos são colocados entre colchetes, \[ ... \] e podem ser Propriedades, variáveis de ambiente (% Prefix), caminhos de arquivo ( \# prefixo) ou caminhos de diretório de componente ($ Prefix). Se depois de Formatar a cadeia de caracteres for avaliada como um inteiro, esse inteiro será usado como um índice na [tabela de erros](error-table.md) para recuperar a mensagem a ser exibida. Se, depois de Formatar, a cadeia de caracteres contiver caracteres não numéricos, a cadeia de caracteres será exibida como a mensagem.

## <a name="return-processing-options"></a>Opções de processamento de retorno

A ação personalizada não usa nenhuma opção.

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

A ação personalizada não usa nenhuma opção.

## <a name="in-script-execution-options"></a>Opções de execução de In-Script

A ação personalizada não usa nenhuma opção.

## <a name="return-values"></a>Valores de retorno

Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).

## <a name="remarks"></a>Comentários

Por exemplo, as ações personalizadas CAError1, CAError2, CAError3 e CAError4 retornam essas mensagens.

[Tabela CustomAction](customaction-table.md)



| Ação   | Tipo | Fonte | Destino                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Prop1\]                           |
| CAError2 | 19   |        | Falha na instalação devido a Error2. |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[Prop2\]                           |



 

[Tabela de propriedades](property-table.md)



| Propriedade | Valor                                 |
|----------|---------------------------------------|
| Prop1    | "Falha na instalação devido a Error1." |
| Prop2    | "25100"                               |



 

[Tabela de erros](error-table.md)



| Código  | Mensagem                             |
|-------|-------------------------------------|
| 25000 | Falha na instalação devido a Error3. |
| 25100 | Falha na instalação devido a Error4. |



 

Essas ações personalizadas retornam as seguintes mensagens de erro:



| Ação personalizada | Cadeia de caracteres de mensagem retornada             |
|---------------|-------------------------------------|
| CAError1      | Falha na instalação devido a Error1. |
| CAError2      | Falha na instalação devido a Error2. |
| CAError3      | Falha na instalação devido a Error3. |
| CAError4      | Falha na instalação devido a Error4. |



 

Observe que, como a ordem de avaliação das condições de inicialização não pode ser garantida ao criar a [tabela LaunchCondition](launchcondition-table.md), você deve usar as ações personalizadas do tipo de ação personalizada 19 em sua instalação para avaliar as condições em uma ordem específica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> </dl>

 

 



