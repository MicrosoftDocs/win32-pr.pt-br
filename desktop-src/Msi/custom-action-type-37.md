---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 37 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Tipo de ação personalizada 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a42d4837af6fe2878f33624251d9c06550855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011466"
---
# <a name="custom-action-type-37"></a>Tipo de ação personalizada 37

Essa ação personalizada é escrita em JScript, como ECMA 262. Windows Installer não dá suporte a JScript 1,0. Para obter mais informações, consulte [scripts](scripts.md).

## <a name="source"></a>Fonte

O campo de origem da [tabela CustomAction](customaction-table.md) contém o valor nulo. O código de script para a ação personalizada é armazenado como uma cadeia de caracteres de texto de script literal no campo de destino.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.



| Constantes                                                             | Hexadecimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory** | 0x025       | 37      |



 

Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits. Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico. Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md). Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.



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

Uma ação personalizada escrita em JScript ou VBScript requer o objeto de [**sessão**](session-object.md) de instalação. O instalador anexa o **objeto de sessão** ao script com o nome "Session". Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> </dl>

 

 



