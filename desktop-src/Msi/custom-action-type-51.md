---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 51 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Tipo de ação personalizada 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922332"
---
# <a name="custom-action-type-51"></a>Tipo de ação personalizada 51

Essa ação personalizada define uma propriedade de uma cadeia de caracteres de texto formatado.

Para afetar uma propriedade usada em uma condição em um componente ou recurso, a ação personalizada deve vir antes da [ação CostFinalize](costfinalize-action.md) na sequência de ação.

## <a name="source"></a>Fonte

O campo de origem da [tabela CustomAction](customaction-table.md) pode conter o nome de uma propriedade ou uma chave para a [tabela de propriedades](property-table.md). Essa propriedade é definida pela cadeia de caracteres formatada no campo de destino usando [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.



| Constantes                                                             | Hexadecimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty** | 0x033       | 51      |



 

## <a name="target"></a>Destino

A coluna Target da [tabela CustomAction](customaction-table.md) contém uma cadeia de texto formatada usando a funcionalidade especificada em [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sem os especificadores de campo numérico). Os parâmetros a serem substituídos são colocados entre colchetes, \[ ... \] e podem ser Propriedades, variáveis de ambiente (% Prefix), caminhos de arquivo ( \# prefixo) ou caminhos de diretório de componente ($ Prefix).

## <a name="return-processing-options"></a>Opções de processamento de retorno

A ação personalizada não usa essas opções.

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução. Essas opções controlam a execução de várias ações personalizadas. Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opções de execução de In-Script

A ação personalizada não usa essas opções.

## <a name="return-values"></a>Valores de retorno

Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).

## <a name="remarks"></a>Comentários

Se você definir uma [propriedade privada](private-properties.md) na sequência da interface do usuário criando uma ação personalizada em uma das tabelas de sequência da interface do usuário, essa propriedade não será definida na sequência de execução. Para definir a propriedade na sequência de execução, você também deve colocar uma ação personalizada em uma tabela de sequência de execução. Como alternativa, você pode tornar a propriedade uma [propriedade pública](public-properties.md) e incluí-la na [**Propriedade SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> <dt>

[Ações personalizadas de texto formatado](formatted-text-custom-actions.md)
</dt> </dl>

 

 



