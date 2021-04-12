---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 21 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Tipo de ação personalizada 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5bb7482c2f7c7b6cbd85af7a6f01cc83edbb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297448"
---
# <a name="custom-action-type-21"></a>Tipo de ação personalizada 21

Essa ação personalizada é escrita em JScript, como ECMA 262. Windows Installer não dá suporte a JScript 1,0. Para obter mais informações, consulte [scripts](scripts.md).

## <a name="source"></a>Fonte

O script é instalado com o aplicativo durante a sessão atual. O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de arquivos](file-table.md). O local do código de ação personalizado é determinado pela resolução do caminho de destino para esse arquivo; Portanto, essa ação personalizada deve ser chamada depois que o arquivo tiver sido instalado e antes de ser removido.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.



| Constantes                                                              | Hexadecimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile** | 0x015       | 21      |



 

Windows Installer pode usar [ações personalizadas de 64 bits](64-bit-custom-actions.md) em sistemas operacionais de 64 bits. Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico. Para obter informações, consulte ações personalizadas de 64 bits. Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.



| Constantes                                                                                                     | Hexadecimal | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript** | 0x0001015   | 4117    |



 

## <a name="target"></a>Destino

O campo de destino da [tabela CustomAction](customaction-table.md) contém uma função de script opcional. O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.

## <a name="return-processing-options"></a>Opções de processamento de retorno

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno. Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução. Essas opções controlam a execução de várias ações personalizadas. Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opções de execução de In-Script

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script. Essas opções copiam o código de ação para o script de execução, reversão ou confirmação. Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores de retorno

Funções opcionais escritas em script devem retornar um dos valores descritos em [valores de retorno de ações personalizadas JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).

## <a name="remarks"></a>Comentários

Uma ação personalizada escrita em JScript ou VBScript requer o objeto de [**sessão**](session-object.md) de instalação. O instalador anexa o **objeto de sessão** ao script com o nome "Session". Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.

As ações personalizadas que fazem referência a um arquivo instalado como sua fonte, como o tipo de ação personalizada 21 (JScript), devem aderir às seguintes restrições de sequenciamento:

-   A ação personalizada deve ser sequenciada após a [ação CostFinalize](costfinalize-action.md). Isso é para que a ação personalizada possa resolver o caminho necessário para localizar o arquivo de origem que contém o JScript.
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (em script) desse tipo deverão ser sequenciadas após a [ação InstallFiles](installfiles-action.md).
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas não adiadas desse tipo deverão ser sequenciadas após a [ação InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> </dl>

 

 



