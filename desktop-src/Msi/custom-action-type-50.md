---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 50 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Tipo de ação personalizada 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747341"
---
# <a name="custom-action-type-50"></a>Tipo de ação personalizada 50

Essa ação personalizada chama um executável iniciado com uma linha de comando.

Consulte também [arquivos executáveis](executable-files.md).

## <a name="source"></a>Fonte

O executável é gerado a partir de um arquivo existente. O campo Source da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de propriedades](property-table.md) de uma propriedade que contém o caminho completo para o arquivo executável.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.



| Constantes                                                        | Hexadecimal | Decimal |
|------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty** | 0x032       | 50      |



 

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

Uma ação personalizada que inicia um executável usa uma linha de comando, que normalmente contém propriedades que são designadas dinamicamente. Se essa for também uma [ação personalizada de execução adiada](deferred-execution-custom-actions.md), o instalador usará CreateProcessAsUser ou CreateProcess para criar o processo quando a ação personalizada for invocada a partir do script de instalação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> </dl>

 

 



