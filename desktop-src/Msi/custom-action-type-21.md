---
description: Os desenvolvedores Windows pacotes do Instalador podem optar por usar um tipo de ação personalizada 21 quando as ações padrão não são suficientes para executar a instalação.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Tipo de ação personalizada 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6184455b15b1bcea1c53532ef53ef526b7af159d81322994220186d6cd187e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105255"
---
# <a name="custom-action-type-21"></a>Tipo de ação personalizada 21

Essa ação personalizada é escrita em JScript, como ECMA 262. Windows O instalador não dá suporte JScript 1.0. Para obter mais informações, consulte [Scripts](scripts.md).

## <a name="source"></a>Fonte

O script é instalado com o aplicativo durante a sessão atual. O campo Origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela Arquivo](file-table.md). O local do código de ação personalizado é determinado pela resolução do caminho de destino para esse arquivo; portanto, essa ação personalizada deve ser chamada depois que o arquivo tiver sido instalado e antes de ser removido.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna Tipo da tabela [CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.



| Constantes                                                              | Hexadecimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile** | 0x015       | 21      |



 

Windows O instalador pode usar Ações Personalizadas de [64 bits](64-bit-custom-actions.md) em sistemas operacionais de 64 bits. Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico. Para obter informações, consulte Ações personalizadas de 64 bits. Inclua o seguinte valor na coluna Tipo da tabela [CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.



| Constantes                                                                                                     | Hexadecimal | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript** | 0x0001015   | 4117    |



 

## <a name="target"></a>Destino

O campo Destino da tabela [CustomAction contém](customaction-table.md) uma função de script opcional. O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.

## <a name="return-processing-options"></a>Opções de processamento de retorno

Inclua bits de sinalizador opcionais na coluna Tipo da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno. Para ver uma descrição das opções e dos valores, consulte Opções de processamento de [retorno de ação personalizada.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Tipo da tabela [CustomAction para](customaction-table.md) especificar opções de agendamento de execução. Essas opções controlam a execução múltipla de ações personalizadas. Para ver uma descrição das opções, consulte [Opções de agendamento de execução de](custom-action-execution-scheduling-options.md)ação personalizada.

## <a name="in-script-execution-options"></a>In-Script de execução

Inclua bits de sinalizador opcionais na coluna Tipo da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução no script. Essas opções copiam o código de ação para o script de execução, reação ou confirmação. Para ver uma descrição das opções, consulte [Ações personalizadas In-Script opções de execução](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores de retorno

As funções opcionais escritas no script devem retornar um dos valores descritos em Valores de [Retorno de JScript e Ações Personalizadas do VBScript.](return-values-of-jscript-and-vbscript-custom-actions.md)

## <a name="remarks"></a>Comentários

Uma ação personalizada que é escrita em JScript ou VBScript requer o objeto [**sessão de**](session-object.md) instalação. O instalador anexa o **Objeto de Sessão** ao script com o nome "Sessão". Como  o objeto Session pode não existir durante uma reação de instalação, uma ação personalizada adiada escrita no [](obtaining-context-information-for-deferred-execution-custom-actions.md) script deve usar um dos métodos ou propriedades do objeto **Session** descritos na seção Obtendo informações de contexto para ações personalizadas de execução adiada para recuperar seu contexto.

Ações personalizadas que referenciam um arquivo instalado como sua origem, como o tipo de ação personalizada 21 (JScript), devem seguir as seguintes restrições de sequenciamento:

-   A ação personalizada deve ser sequenciada após a [ação CostFinalize](costfinalize-action.md). Isso é para que a ação personalizada possa resolver o caminho necessário para localizar o arquivo de origem que contém o JScript.
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (no script) desse tipo deverão ser sequenciadas após a [ação InstallFiles](installfiles-action.md).
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas não adiadas desse tipo deverão ser sequenciadas após a [ação InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ações \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



