---
description: O ICE27 valida as tabelas de sequência de um pacote de instalação para ações válidas, restrições de sequência de ação e organização nas seções pesquisa, custo, seleção e execução.
ms.assetid: c5292a3c-57bb-4203-96a1-6d747f554178
title: ICE27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb4b90b313f5f78874fb93ce9d32c3650b97064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827877"
---
# <a name="ice27"></a>ICE27

O ICE27 valida as [*tabelas de sequência*](s-gly.md) de um pacote de instalação para ações válidas, restrições de sequência de ação e organização nas seções pesquisa, custo, seleção e execução.

A ação personalizada ICE27 valida o seguinte:

-   As ações listadas na coluna ação das tabelas de sequência são [ações padrão](standard-actions.md), uma ação personalizada listada na [tabela CustomAction](customaction-table.md)ou uma caixa de diálogo listada na tabela de [diálogo](dialog-table.md).
-   As ações sujeitas às restrições de sequenciamento estão na ordem relativa correta entre si na sequência de ação. As restrições de sequenciamento resultam quando uma ação depende de outra.
-   As ações restritas a uma seção específica da sequência estão localizadas onde pertencem. ICE27 valida a organização a seguir das tabelas de sequência. Observe que nem todas as tabelas de sequência têm cada seção. Consulte as tabelas de sequência sugeridas em [usando uma tabela de sequência](using-a-sequence-table.md).



| Seção da tabela de sequências | Intervalo na sequência de ação                                                                       | Ações pertencentes à seção                                                                                                                                                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pesquisar                 | {Start} para [CostInitialize](costinitialize-action.md)                                         | Ações que pesquisam aplicativos existentes. [AppSearch](appsearch-action.md)<br/> [CCPSearch](ccpsearch-action.md)<br/>                                                                                                         |
| Custos                | Ação de [CostInitialize](costinitialize-action.md) para [CostFinalize](costfinalize-action.md)  | Ações que fazem o [custo do arquivo](file-costing.md). [CostInitialize](costinitialize-action.md)<br/> [Custo de](filecost-action.md)<br/> [CostFinalize](costfinalize-action.md)<br/>                                           |
| Seleção              | [CostFinalize](costfinalize-action.md) [InstallValidate](installvalidate-action.md)       | Ações que definem pastas ou Estados de recursos. [Ação SetODBCFolders](setodbcfolders-action.md)<br/>                                                                                                                                        |
| Execução              | [InstallValidate](installvalidate-action.md) [InstallFinalize](installfinalize-action.md) | Ações de script, como registro, publicação, instalação (onde você copia arquivos). Observe que a [ação InstallFinalize](installfinalize-action.md) deve estar na tabela se e somente se houver ações na seção execução.<br/> |
| Execução          | [InstallFinalize](installfinalize-action.md) para {End}                                         | [RemoveExistingProducts](removeexistingproducts-action.md)                                                                                                                                                                                      |



 

ICE27 valida as seguintes tabelas:

-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE27 posta uma mensagem de erro se houver tabelas de sequência no pacote com sequenciamento de ação ou organização inválido.

## <a name="example"></a>Exemplo



| Erro de ICE27                                                                                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ação desconhecida: ' Action1 ' da tabela InstallExecuteSequnence. Não é uma ação padrão e não foi encontrada nas tabelas CustomAction ou Dialog    | Há uma ação listada na tabela de sequência indicada que não é [ações padrão](standard-actions.md), uma ação personalizada listada na [tabela CustomAction](customaction-table.md)ou uma caixa de diálogo listada na [tabela de diálogo](dialog-table.md).                                                                                                                                                                                                                                                                       |
| ' Action2 ' na tabela InstallExecute no lugar errado. Atual: pesquisa, correto: custos                                                 | Há uma ação em uma tabela de sequência que é colocada incorretamente em relação ao número de sequência na coluna de sequência. "Current" indica o posicionamento atual da ação nas seções de pesquisa, custo, seleção ou execução da tabela de sequência indicada.<br/> "Corrigir" indica em qual seção a ação pertence.<br/> Para corrigir esse erro, altere o número de sequência da ação para dentro da seção correta. Observe que algumas ações podem estar localizadas em mais de uma seção.<br/> |
| A ação ' InstallFinalize ' na tabela InstallExecuteSequence só pode ser chamada quando há operações de script a serem executadas             | Há uma [ação InstallFinalize](installfinalize-action.md) em uma tabela de sequência que não contém nenhuma operação de script na seção execução da tabela. Adicione ações à seção execução ou remova a ação InstallFinalize da tabela.<br/>                                                                                                                                                                                                                                                        |
| InstallFinalize deve ser chamado na tabela InstallExecuteSequence, já que existem operações de script para serem executadas                            | Há uma tabela de sequência que contém ações na seção execução que não inclui a [ação InstallFinalize](installfinalize-action.md). Adicione a ação InstallFinalize a essa tabela de sequência e dê a ela o maior número de sequência para colocá-la por último na sequência de ação.<br/>                                                                                                                                                                                                                            |
| Ação: ' Action3 ' na tabela InstallExecuteSequence deve vir antes da ação ' Action5 '. Seq \# . atual: 1200. Seq dependente \# : 1100 | Há uma ação na tabela de sequência indicada que é sequenciada após uma ação dependente. Altere o número de sequência na ação dependente para que ele venha antes da ação.<br/>                                                                                                                                                                                                                                                                                                                                    |
| Ação: ' Action4 ' na tabela InstallExecuteSequence deve vir após a ação ' Action6 '.                                             | Há uma ação na tabela de sequência indicada que é sequenciada antes de uma ação na qual ela depende. Altere o número de sequência na ação para que ele venha após sua ação dependente.<br/>                                                                                                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




