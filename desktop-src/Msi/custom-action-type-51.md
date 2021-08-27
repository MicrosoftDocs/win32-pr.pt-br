---
description: Os desenvolvedores Windows pacotes do Instalador podem optar por usar um tipo de ação personalizada 51 quando as ações padrão não são suficientes para executar a instalação.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Tipo de ação personalizada 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e780c1a38b60c855f4bfe665f5f68a3f6a037a078f4a2875d1a2ea57c5e7e8dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075046"
---
# <a name="custom-action-type-51"></a>Tipo de ação personalizada 51

Essa ação personalizada define uma propriedade de uma cadeia de caracteres de texto formatada.

Para afetar uma propriedade usada em uma condição em um componente ou recurso, a ação personalizada deve vir antes da [ação CostFinalize](costfinalize-action.md) na sequência de ação.

## <a name="source"></a>Fonte

O campo Origem da [tabela CustomAction](customaction-table.md) pode conter o nome de uma propriedade ou uma chave para a [tabela Property](property-table.md). Essa propriedade é definida pela cadeia de caracteres formatada no campo Destino usando [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna Tipo da tabela [CustomAction](customaction-table.md) para especificar o tipo numérico básico.



| Constantes                                                             | Hexadecimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty** | 0x033       | 51      |



 

## <a name="target"></a>Destino

A coluna Destino da tabela [CustomAction](customaction-table.md) contém uma cadeia de caracteres de texto formatada usando a funcionalidade especificada em [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sem os especificadores de campo numérico). Os parâmetros a serem substituídos são incluídos entre colchetes, ... e podem ser propriedades, variáveis de ambiente (prefixo%), caminhos de arquivo ( prefixo) ou caminhos de diretório de componente \[ \] \# (prefixo$ ).

## <a name="return-processing-options"></a>Opções de processamento de retorno

A ação personalizada não usa essas opções.

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Tipo da tabela [CustomAction para](customaction-table.md) especificar opções de agendamento de execução. Essas opções controlam a execução múltipla de ações personalizadas. Para ver uma descrição das opções, consulte [Opções de agendamento de execução de](custom-action-execution-scheduling-options.md)ação personalizada.

## <a name="in-script-execution-options"></a>In-Script de execução

A ação personalizada não usa essas opções.

## <a name="return-values"></a>Valores de retorno

Consulte [Valores de retorno de ação personalizada.](custom-action-return-values.md)

## <a name="remarks"></a>Comentários

Se você definir [uma](private-properties.md) propriedade privada na sequência de interface do usuário ao criar uma ação personalizada em uma das tabelas de sequência de interface do usuário, essa propriedade não será definida na sequência de execução. Para definir a propriedade na sequência de execução, você também deve colocar uma ação personalizada em uma tabela de sequência de execução. Como alternativa, você pode tornar a propriedade uma [propriedade pública](public-properties.md) e incluí-la na [**propriedade SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ações \_ personalizadas](custom-actions.md)
</dt> <dt>

[Ações personalizadas de texto formatado](formatted-text-custom-actions.md)
</dt> </dl>

 

 



