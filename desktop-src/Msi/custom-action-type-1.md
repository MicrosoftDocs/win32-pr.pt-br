---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 1 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Tipo de ação personalizada 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011725"
---
# <a name="custom-action-type-1"></a>Tipo de ação personalizada 1

Essa ação personalizada chama uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++.

## <a name="source"></a>Fonte

A DLL é gerada a partir de um fluxo binário temporário. O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela binária](binary-table.md).

A coluna de dados na tabela binária contém os dados de fluxo. Um fluxo separado é alocado para cada linha. Novos dados binários podem ser inseridos de um arquivo usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido por [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na tabela. Quando a ação personalizada é invocada, os dados de fluxo são copiados em um arquivo temporário, que é processado dependendo do tipo de ação personalizada.

## <a name="type-value"></a>Valor do tipo

Inclua os seguintes bits de sinalizador na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData** | 0x001       | 1       |



 

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

Quando uma tabela de banco de dados é exportada, cada fluxo é gravado como um arquivo separado na subpasta nomeada após a tabela, usando a chave primária como o nome do arquivo (coluna de nome para a tabela binária), com uma extensão padrão de ". IBD". O nome deve usar o formato 8,3 se o sistema de arquivos ou o sistema de controle de versão não oferecer suporte a nomes de arquivo longos. O arquivo morto persistente substitui os dados de fluxo pelo nome de arquivo usado, para que os dados possam ser localizados quando a tabela for importada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> <dt>

[Bibliotecas de vínculo dinâmico](dynamic-link-libraries.md)
</dt> <dt>

[Obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



