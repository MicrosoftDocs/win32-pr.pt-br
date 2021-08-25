---
description: os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 37 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Tipo de ação personalizada 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1595279d2c8f66e1b899ad88ad6a9d5c164c2727b5c905ce66700479ed32446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996815"
---
# <a name="custom-action-type-37"></a>Tipo de ação personalizada 37

essa ação personalizada é escrita em JScript, como ECMA 262. Windows o instalador não dá suporte ao JScript 1,0. Para obter mais informações, consulte [scripts](scripts.md).

## <a name="source"></a>Fonte

O campo de origem da [tabela CustomAction](customaction-table.md) contém o valor nulo. O código de script para a ação personalizada é armazenado como uma cadeia de caracteres de texto de script literal no campo de destino.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.



| Constantes                                                             | Hexadecimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory** | 0x025       | 37      |



 

Windows O instalador pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits. Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico. Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md). Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.



| Constantes                                                                                                    | Hexadecimal | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript** | 0x0001025   | 4133    |



 

## <a name="target"></a>Destino

O campo de destino da [tabela CustomAction](customaction-table.md) contém o código de script para a ação personalizada como uma cadeia de caracteres de texto de script literal.

## <a name="return-processing-options"></a>Opções de processamento de retorno

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno. Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução. Essas opções controlam a execução de várias ações personalizadas. Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opções de execução de In-Script

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script. Essas opções copiam o código de ação para o script de execução, reversão ou confirmação. Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores de retorno

Esse tipo de ação personalizada sempre retorna êxito.

## <a name="remarks"></a>Comentários

uma ação personalizada escrita em JScript ou VBScript requer o objeto de [**sessão**](session-object.md) de instalação. O instalador anexa o **objeto de sessão** ao script com o nome "Session". Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> </dl>

 

 



