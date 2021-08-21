---
description: A finalidade de uma ação personalizada de execução adiada é atrasar a execução de uma alteração do sistema para a hora em que o script de instalação é executado.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Ações personalizadas de execução adiada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cec06600fa2cdb447ace579ecf9d19be62e5f4824ecf2d34d77ed879a717d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379173"
---
# <a name="deferred-execution-custom-actions"></a>Ações personalizadas de execução adiada

A finalidade de uma ação personalizada de execução adiada é atrasar a execução de uma alteração do sistema para a hora em que o script de instalação é executado. Isso é diferente de uma ação personalizada regular ou de uma ação padrão, na qual o instalador executa a ação imediatamente após encontrar-a em uma tabela de sequência ou em uma chamada para [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). Uma ação personalizada de execução adiada permite que um autor do pacote especifique operações do sistema em um ponto específico dentro da execução do script de instalação.

O instalador não executa uma ação personalizada de execução adiada no momento em que a sequência de instalação é processada. Em vez disso, o instalador grava a ação personalizada no script de instalação. O único parâmetro de modo que o instalador define nesse caso é MSIRUNMODE \_ SCHEDULED. Consulte [**MsiGetMode para**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) ver uma descrição dos parâmetros de modo de executar.

Uma ação personalizada de execução adiada deve ser agendada na tabela de sequência de execução dentro da seção que executa a geração de script. As ações personalizadas de execução adiada devem vir após [InstallInitialize e vir](installinitialize-action.md) [antes de InstallFinalize](installfinalize-action.md) na sequência de ação.

Ações personalizadas que configuram propriedades, estados de recurso, estados de componente ou diretórios de destino ou que agendam operações do sistema inserindo linhas em tabelas de sequência, podem, em muitos casos, usar a execução imediata com segurança. No entanto, ações personalizadas que alteram o sistema diretamente ou chamam outro serviço do sistema devem ser adiadas para a hora em que o script de instalação é executado. Consulte [Ações personalizadas](synchronous-and-asynchronous-custom-actions.md) síncronas e assíncronas para obter mais informações sobre possíveis conflitos entre suas ações personalizadas e o thread de instalação principal.

Como o script de instalação pode ser executado fora da sessão de instalação na qual foi escrito, a sessão pode não existir mais durante a execução do script de instalação. Isso significa que o handle de sessão original e o conjunto de dados de propriedade durante a sequência de instalação não estão disponíveis para uma ação personalizada de execução adiada. As ações personalizadas adiadas que chamam DLLs (bibliotecas de vínculo dinâmico) passam um handle que só pode ser usado para obter uma quantidade muito limitada de informações, conforme descrito em Obtendo informações de contexto para ações personalizadas de execução [adiada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Observe que as ações [](rollback-custom-actions.md) personalizadas adiadas, incluindo ações personalizadas de reação e ações personalizadas de [confirmação,](commit-custom-actions.md)são os únicos tipos de ações que podem ser executados fora do contexto de segurança dos usuários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Opções de execução In-Script ação personalizada](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referência de ação personalizada](custom-action-reference.md)
</dt> </dl>

 

 



