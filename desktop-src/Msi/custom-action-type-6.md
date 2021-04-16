---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 6 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Tipo de ação personalizada 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747556"
---
# <a name="custom-action-type-6"></a>Tipo de ação personalizada 6

Essa ação personalizada é escrita em VBScript. Para obter mais informações, consulte [scripts](scripts.md).

## <a name="source"></a>Fonte

O script é gerado a partir de um fluxo binário temporário. O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela binária](binary-table.md). A coluna de dados na tabela binária contém os dados de fluxo. Um fluxo separado é alocado para cada linha.

Novos dados binários podem ser inseridos de um arquivo usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido por [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na tabela. Quando a ação personalizada é invocada, os dados de fluxo são copiados em um arquivo temporário, que é processado dependendo do tipo de ação personalizada.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.



| Constantes                                                               | Hexadecimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData** | 0x006       | 6       |



 

Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits. Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico. Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md). Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.



| Constantes                                                                                                      | Hexadecimal | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript** | 0x0001006   | 4102    |



 

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

Uma ação personalizada escrita em JScript ou VBScript requer a instalação do [**objeto de sessão**](session-object.md). O instalador anexa o objeto de **sessão** ao script com a *sessão* de nome. Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.

Quando uma tabela de banco de dados é exportada, cada fluxo é gravado como um arquivo separado na subpasta nomeada após a tabela, usando a chave primária como o nome do arquivo (coluna de nome para a tabela binária), com uma extensão padrão de ". IBD". O nome deve usar o formato de nome de arquivo 8,3 se o sistema de arquivos ou o sistema de controle de versão não oferecer suporte a nomes de arquivo longos. O arquivo morto persistente substitui os dados de fluxo pelo nome de arquivo usado, para que os dados possam ser localizados quando a tabela for importada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> </dl>

 

 



