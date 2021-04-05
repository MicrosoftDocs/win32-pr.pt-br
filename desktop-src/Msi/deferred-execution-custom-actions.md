---
description: A finalidade de uma ação personalizada de execução adiada é atrasar a execução de uma alteração do sistema no momento em que o script de instalação é executado.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Ações personalizadas de execução adiada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09b91793f5d5bbc7be7099c92f8d8f212012d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922044"
---
# <a name="deferred-execution-custom-actions"></a>Ações personalizadas de execução adiada

A finalidade de uma ação personalizada de execução adiada é atrasar a execução de uma alteração do sistema no momento em que o script de instalação é executado. Isso é diferente de uma ação personalizada regular ou de uma ação padrão, na qual o instalador executa a ação imediatamente ao encontrar em uma tabela de sequência ou em uma chamada para [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). Uma ação personalizada de execução adiada permite que um autor de pacote especifique operações do sistema em um ponto específico dentro da execução do script de instalação.

O instalador não executa uma ação personalizada de execução adiada no momento em que a sequência de instalação é processada. Em vez disso, o instalador grava a ação personalizada no script de instalação. O único parâmetro de modo que o instalador define nesse caso é MSIRUNMODE \_ agendado. Consulte [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para obter uma descrição dos parâmetros do modo de execução.

Uma ação personalizada de execução adiada deve ser agendada na tabela de sequências de execução na seção que executa a geração de script. As ações personalizadas de execução adiada devem vir após [InstallInitialize](installinitialize-action.md) e vir antes de [InstallFinalize](installfinalize-action.md) na sequência de ação.

Ações personalizadas que definem propriedades, Estados de recursos, Estados de componentes ou diretórios de destino, ou que agendam operações do sistema inserindo linhas em tabelas de sequência, podem, em muitos casos, usar a execução imediata com segurança. No entanto, as ações personalizadas que alteram o sistema diretamente ou chamam outro serviço do sistema devem ser adiadas para a hora em que o script de instalação é executado. Consulte [ações personalizadas síncronas e assíncronas](synchronous-and-asynchronous-custom-actions.md) para obter mais informações sobre possíveis conflitos entre suas ações personalizadas e o thread de instalação principal.

Como o script de instalação pode ser executado fora da sessão de instalação na qual ele foi gravado, a sessão pode não existir mais durante a execução do script de instalação. Isso significa que o identificador de sessão original e o conjunto de dados de propriedade durante a sequência de instalação não estão disponíveis para uma ação personalizada de execução adiada. As ações personalizadas adiadas que chamam DLLs (bibliotecas de vínculo dinâmico) passam um identificador que só pode ser usado para obter uma quantidade muito limitada de informações, conforme descrito em [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).

Observe que as ações personalizadas adiadas, incluindo [reversão de ações personalizadas](rollback-custom-actions.md) e [ações personalizadas de confirmação](commit-custom-actions.md), são os únicos tipos de ações que podem ser executadas fora do contexto de segurança dos usuários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referência de ação personalizada](custom-action-reference.md)
</dt> </dl>

 

 



