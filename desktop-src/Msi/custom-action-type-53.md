---
description: Os desenvolvedores Windows pacotes do Instalador podem optar por usar um tipo de ação personalizada 53 quando as ações padrão não são suficientes para executar a instalação.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Tipo de ação personalizada 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b78c2dbc8aa233175eeacfa8d16521968dfceeb6b97504e639946c6284b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947887"
---
# <a name="custom-action-type-53"></a>Tipo de ação personalizada 53

Essa ação personalizada é escrita em JScript, como ECMA 262. Windows O instalador não dá suporte JScript 1.0. Para obter mais informações, consulte [Scripts](scripts.md).

## <a name="source"></a>Fonte

O campo Origem da [tabela CustomAction](customaction-table.md) contém um nome de propriedade ou uma chave para a tabela [Property](property-table.md) para uma propriedade que contém o texto do script.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna Tipo da tabela [CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.



| Constantes                                                            | Hexadecimal | Decimal |
|----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty** | 0x035       | 53      |



 

Windows O instalador pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits. Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico. Para obter informações, [consulte Ações personalizadas de 64 bits.](64-bit-custom-actions.md) Inclua o seguinte valor na coluna Tipo da tabela [CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.



| Constantes                                                                                                   | Hexadecimal | Decimal |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001035   | 4149    |



 

## <a name="target"></a>Destino

O campo Destino da tabela [CustomAction contém](customaction-table.md) uma função de script opcional. O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.

## <a name="return-processing-options"></a>Opções de processamento de retorno

Inclua bits de sinalizador opcionais na coluna Tipo da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno. Para ver uma descrição das opções e dos valores, consulte Opções de processamento de [retorno de ação personalizada.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Tipo da tabela [CustomAction para](customaction-table.md) especificar opções de agendamento de execução. Essas opções controlam a execução múltipla de ações personalizadas. Para ver uma descrição das opções, consulte [Opções de agendamento de execução de](custom-action-execution-scheduling-options.md)ação personalizada.

## <a name="in-script-execution-options"></a>In-Script de execução

Inclua bits de sinalizador opcionais na coluna Tipo da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução no script. Essas opções copiam o código de ação para o script de execução, reação ou confirmação. Para ver uma descrição das opções, consulte [Ações personalizadas In-Script opções de execução.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Valores de retorno

As funções opcionais escritas no script devem retornar um dos valores descritos em Valores de [Retorno de JScript e Ações Personalizadas do VBScript.](return-values-of-jscript-and-vbscript-custom-actions.md)

## <a name="remarks"></a>Comentários

Uma ação personalizada que é escrita em JScript requer o objeto [**sessão de**](session-object.md) instalação. Como o objeto **Session** pode não existir durante uma reação de [instalação,](obtaining-context-information-for-deferred-execution-custom-actions.md)uma ação personalizada adiada escrita no script usa um dos métodos descritos em Obtendo informações de contexto para ações personalizadas de execução adiada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ações \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



