---
description: os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 17 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Tipo de ação personalizada 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c54d19f99c552b731d88ab62926212539381f40e202a044c31a41fd906a7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947984"
---
# <a name="custom-action-type-17"></a>Tipo de ação personalizada 17

Essa ação personalizada chama uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++.

## <a name="source"></a>Fonte

A DLL é instalada com o aplicativo durante a sessão atual. O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de arquivos](file-table.md). O local do código de ação personalizado é determinado pela resolução do caminho de destino para esse arquivo; Portanto, essa ação personalizada deve ser chamada depois que o arquivo tiver sido instalado e antes de ser removido.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile** | 0x011       | 17      |



 

## <a name="target"></a>Destino

A DLL é chamada por meio do ponto de entrada nomeado no campo de destino da [tabela CustomAction](customaction-table.md), passando um único argumento que é o identificador para a sessão de instalação atual. O nome do ponto de entrada especificado na tabela deve corresponder ao exportado da DLL. Observe que, se a função de entrada não for especificada por um. Arquivo DEF ou por uma especificação/EXPORT: linker, o nome pode ter um sublinhado à esquerda e um @4 sufixo "". A função chamada deve especificar a \_ \_ Convenção de chamada stdcall.

## <a name="return-processing-options"></a>Opções de processamento de retorno

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno. Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução. Essas opções controlam a execução de várias ações personalizadas. Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opções de execução de In-Script

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script. Essas opções copiam o código de ação para o script de execução, reversão ou confirmação. Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores de retorno

Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).

## <a name="remarks"></a>Comentários

Uma ação personalizada que chama uma DLL (biblioteca de vínculo dinâmico) requer um identificador para a sessão de instalação. Se essa for também uma ação personalizada de execução adiada, a sessão poderá não existir mais durante a execução do script de instalação. Para obter informações sobre como uma ação personalizada desse tipo pode obter informações de contexto, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).

As ações personalizadas são executadas em um thread separado e podem ter acesso limitado ao sistema. As ações personalizadas que são executadas de modo assíncrono bloqueiam o thread principal no término da sequência atual ou da sessão de instalação até que eles sejam retornados.

As ações personalizadas que fazem referência a um arquivo instalado como sua fonte, como o tipo de ação personalizada 17 (DLL), devem aderir às seguintes restrições de sequenciamento:

-   A ação personalizada deve ser sequenciada após a [ação CostFinalize](costfinalize-action.md). Isso é para que a ação personalizada possa resolver o caminho necessário para localizar a DLL.
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (em script) desse tipo deverão ser sequenciadas após a [ação InstallFiles](installfiles-action.md).
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas não adiadas desse tipo deverão ser sequenciadas após a [ação InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> <dt>

[Ações personalizadas de execução adiada](deferred-execution-custom-actions.md)
</dt> <dt>

[Bibliotecas de vínculo dinâmico](dynamic-link-libraries.md)
</dt> </dl>

 

 



