---
description: os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 18 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Tipo de ação personalizada 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3befbb614e9ee78961cf5b8ef969bdb3d6e7b6c0cb713a267cab3d09b4588d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379272"
---
# <a name="custom-action-type-18"></a>Tipo de ação personalizada 18

Essa ação personalizada chama um executável iniciado com uma linha de comando.

## <a name="source"></a>Fonte

O executável é gerado a partir de um arquivo instalado com o aplicativo. O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de arquivos](file-table.md). O local do código de ação personalizado é determinado pela resolução do caminho de destino para esse arquivo; Portanto, essa ação personalizada deve ser chamada depois que o arquivo tiver sido instalado e antes de ser removido.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |



 

## <a name="target"></a>Destino

A coluna de destino da [tabela CustomAction](customaction-table.md) contém a cadeia de caracteres de linha de comando para o executável identificado na coluna de origem.

## <a name="return-processing-options"></a>Opções de processamento de retorno

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno. Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução. Essas opções controlam a execução de várias ações personalizadas. Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opções de execução de In-Script

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script. Essas opções copiam o código de ação para o script de execução, reversão ou confirmação. Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores de retorno

As ações personalizadas que são [arquivos executáveis](executable-files.md) devem retornar um valor de 0 para êxito. O instalador interpreta qualquer outro valor de retorno como falha. Para ignorar valores de retorno, defina o sinalizador de bit **msidbCustomActionTypeContinue** no campo Type da tabela CustomAction.

## <a name="remarks"></a>Comentários

Uma ação personalizada que inicia um executável usa uma linha de comando, que normalmente contém propriedades que são designadas dinamicamente. Se essa for também uma [ação personalizada de execução adiada](deferred-execution-custom-actions.md), o instalador usará [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para criar o processo quando a ação personalizada for invocada a partir do script de instalação.

As ações personalizadas que fazem referência a um arquivo instalado como sua fonte, como o tipo de ação personalizada 18 (EXE), devem aderir às seguintes restrições de sequenciamento:

-   A ação personalizada deve ser sequenciada após a [ação CostFinalize](costfinalize-action.md). Isso é para que a ação personalizada possa resolver o caminho necessário para localizar o EXE.
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (em script) desse tipo deverão ser sequenciadas após a [ação InstallFiles](installfiles-action.md).
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas não adiadas desse tipo deverão ser sequenciadas após a [ação InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> <dt>

[Arquivos executáveis](executable-files.md)
</dt> </dl>

 

 
