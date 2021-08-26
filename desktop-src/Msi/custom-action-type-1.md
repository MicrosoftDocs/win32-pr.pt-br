---
description: Os desenvolvedores Windows pacotes do Instalador podem optar por usar um tipo de ação personalizada 1 quando as ações padrão não são suficientes para executar a instalação.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Tipo de ação personalizada 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3437fcd8a9a0da84ecb03f2527d30b6644210b2feb2ccc6c5f6558c3667a0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044896"
---
# <a name="custom-action-type-1"></a>Tipo de ação personalizada 1

Essa ação personalizada chama uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++.

## <a name="source"></a>Fonte

A DLL é gerada de um fluxo binário temporário. O campo Origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela Binária](binary-table.md).

A coluna Dados na tabela Binary contém os dados de fluxo. Um fluxo separado é alocado para cada linha. Novos dados binários podem ser inseridos de um arquivo usando [**MsiRecordSetStream seguido**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) por [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na tabela. Quando a ação personalizada é invocada, os dados de fluxo são copiados para um arquivo temporário, que é processado dependendo do tipo de ação personalizada.

## <a name="type-value"></a>Valor do tipo

Inclua os seguintes bits de sinalizador na coluna Tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData** | 0x001       | 1       |



 

## <a name="target"></a>Destino

A DLL é chamada por meio do ponto de entrada chamado no campo Destino da tabela [CustomAction](customaction-table.md), passando um único argumento que é o identificador para a sessão de instalação atual. O nome do ponto de entrada especificado na tabela deve corresponder ao exportado da DLL. Observe que se a função de entrada não for especificada por um . Arquivo DEF ou por uma especificação do linker /EXPORT: , o nome pode ter um sublinhado à frente e um @4 sufixo " ". A função chamada deve especificar a \_ \_ convenção de chamada stdcall.

## <a name="return-processing-options"></a>Opções de processamento de retorno

Inclua bits de sinalizador opcionais na coluna Tipo da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno. Para ver uma descrição das opções e dos valores, consulte Opções de processamento de [retorno de ação personalizada.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Tipo da tabela [CustomAction para](customaction-table.md) especificar opções de agendamento de execução. Essas opções controlam a execução múltipla de ações personalizadas. Para ver uma descrição das opções, consulte [Opções de agendamento de execução de](custom-action-execution-scheduling-options.md)ação personalizada.

## <a name="in-script-execution-options"></a>In-Script de execução

Inclua bits de sinalizador opcionais na coluna Tipo da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução no script. Essas opções copiam o código de ação para o script de execução, reação ou confirmação. Para ver uma descrição das opções, consulte [Ações personalizadas In-Script opções de execução.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Valores de retorno

Consulte [Valores de retorno de ação personalizada.](custom-action-return-values.md)

## <a name="remarks"></a>Comentários

Uma ação personalizada que chama uma DLL (biblioteca de vínculo dinâmico) requer um handle para a sessão de instalação. Se essa também for uma ação personalizada de execução adiada, a sessão poderá não existir mais durante a execução do script de instalação. Para obter informações sobre como uma ação personalizada desse tipo pode obter informações de contexto, consulte Obtendo informações de contexto para ações [personalizadas de execução adiada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Quando uma tabela de banco de dados é exportada, cada fluxo é gravado como um arquivo separado na subpasta chamada após a tabela, usando a chave primária como o nome do arquivo (coluna Nome da tabela Binária), com uma extensão padrão de ".ibd". O nome deverá usar o formato 8.3 se o sistema de arquivos ou o sistema de controle de versão não for suportado por nomes de arquivo longos. O arquivo de arquivo persistente substitui os dados de fluxo pelo nome de arquivo usado, para que os dados possam ser localizados quando a tabela for importada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ações \_ personalizadas](custom-actions.md)
</dt> <dt>

[Bibliotecas de vínculo dinâmico](dynamic-link-libraries.md)
</dt> <dt>

[Obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



