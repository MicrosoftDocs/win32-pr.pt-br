---
description: Este material destina-se a desenvolvedores que estão escrevendo seus próprios programas de instalação e desenvolvedores que desejam saber mais sobre as tabelas de banco de dados do instalador. Para obter informações gerais sobre o instalador, consulte sobre o Windows Installer.
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: Funções de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a4233437d24944c8bb7fe5c7de6412e700022b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647474"
---
# <a name="database-functions"></a>Funções de banco de dados

Este material destina-se a desenvolvedores que estão escrevendo seus próprios programas de instalação e desenvolvedores que desejam saber mais sobre as tabelas de banco de dados do instalador. Para obter informações gerais sobre o instalador, consulte [sobre o Windows Installer](about-windows-installer.md).

Você pode usar as funções de acesso do instalador para acessar o banco de dados e o processo de instalação. Essas funções só devem ser usadas por ações de instalação personalizadas e por ferramentas de criação. Algumas das funções de acesso do instalador exigem cadeias de caracteres de consulta SQL para consultar o banco de dados. As consultas devem aderir à sintaxe do instalador [SQL](sql-syntax.md).

Este tópico lista as funções de acesso ao banco de dados do instalador por categoria.

## <a name="general-database-access-functions"></a>Funções gerais de acesso ao banco de dados



| Função                                                             | Descrição                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | Confirma as alterações em um banco de dados.                                                          |
| [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | Retorna os nomes de todas as colunas de chave primária.                                       |
| [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | Retorna uma enumeração que descreve o estado de uma tabela.                                 |
| [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | Prepara uma consulta de banco de dados e cria um objeto de exibição.                                    |
| [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | Retorna o banco de dados ativo para a instalação.                                       |
| [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | Retorna nomes ou definições de coluna.                                                    |
| [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | Abre um arquivo de banco de dados para o acesso ao dado.                                                  |
| [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | Libera o conjunto de resultados para uma exibição executada.                                           |
| [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | Executa a consulta de exibição e fornece os parâmetros necessários.                               |
| [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | Busca o próximo registro sequencial da exibição.                                       |
| [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | Retorna o erro que ocorreu na função [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) . |
| [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | Atualiza um registro buscado.                                                               |



 

## <a name="database-management-functions"></a>Funções de gerenciamento de banco de dados



| Função                                                               | Descrição                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | Cria informações de resumo para uma transformação existente.           |
| [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | Aplica uma transformação a um banco de dados.                               |
| [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | Exporta uma tabela de um banco de dados aberto para um arquivo morto de texto.    |
| [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | Gera um arquivo de transformação de diferenças entre dois bancos de dados. |
| [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | Importa uma tabela de arquivamento de texto do instalador para um banco de dados aberto.   |
| [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | Mescla dois bancos de dados juntos.                                   |
| [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | Retorna o estado do banco de dados.                               |



 

## <a name="record-processing-functions"></a>Funções de processamento de registros



| Função                                                 | Descrição                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | Cria um novo objeto de registro com o número especificado de campos.      |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | Formata dados e propriedades do campo de registro usando uma cadeia de caracteres de formato. |
| [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | Define todos os campos em um registro como nulo.                            |
| [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | Retorna o comprimento de um campo de registro.                           |
| [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | Retorna o número de campos em um registro.                       |
| [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | Retorna o valor inteiro de um campo de registro.                  |
| [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | Retorna o valor da cadeia de caracteres de um campo de registro.                     |
| [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | Relata se um campo de registro é nulo.                         |
| [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | Lê bytes de um campo de fluxo de registro em um buffer.           |
| [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | Define um campo de registro como um campo de número inteiro.                        |
| [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | Define um campo de fluxo de registros de um arquivo.                         |
| [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | Copia uma cadeia de caracteres no campo designado.                      |



 

## <a name="summary-information-property-functions"></a>Funções de propriedade de informações de resumo



| Função                                                                 | Descrição                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | Obtém o identificador para o fluxo de informações de resumo do banco de dados do instalador.    |
| [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | Obtém uma única propriedade das informações de resumo.                   |
| [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | Retorna o número de propriedades no fluxo de informações de resumo.        |
| [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | Grava informações de resumo alteradas de volta no fluxo de informações de resumo. |
| [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | Define uma única propriedade de informações de resumo.                            |



 

## <a name="installer-state-access-functions"></a>Funções de acesso de estado do instalador



| Função                                               | Descrição                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | Retorna o idioma numérico da instalação atual.   |
| [**MsiGetLastErrorRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | Retorna o registro de erro retornado pela última vez para o processo de chamada. |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | Retorna um dos Estados de instalação interna booliana.    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | Obtém o valor de uma propriedade do instalador.                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | Define o valor de uma propriedade de instalação.                 |
| [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | Define um estado booliano do mecanismo interno.                      |



 

## <a name="installer-action-functions"></a>Funções de ação do instalador



| Função                                             | Descrição                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | Executa a ação interna, a ação personalizada ou o assistente de interface do usuário. |
| [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | Avalia uma expressão condicional que contém nomes e valores de propriedade.  |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | Envia um registro de erro para o instalador para processamento.                    |
| [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | Executa uma sequência de ação.                                              |



 

## <a name="installer-location-functions"></a>Funções de localização do instalador



| Função                                     | Descrição                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | Retorna o caminho de origem completo de uma pasta na tabela de diretórios. |
| [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | Retorna o caminho de destino completo de uma pasta na tabela de diretórios. |
| [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | Define o caminho de destino completo para uma pasta na tabela de diretórios.    |



 

## <a name="installer-selection-functions"></a>Funções de seleção do instalador



| Função                                                     | Descrição                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**MsiEnumComponentCosts**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | Enumera o espaço em disco por unidade necessária para instalar um componente. |
| [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | Obtém o estado de um componente.                                    |
| [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | Retorna o espaço em disco exigido por um recurso.                        |
| [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | Obtém o estado de um recurso.                                         |
| [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | Retorna um estado de instalação válido.                                  |
| [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | Define um componente para o estado especificado.                             |
| [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | Modifica os atributos padrão de um recurso em tempo de execução.            |
| [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | Define um recurso para um estado especificado.                                 |
| [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | Define o nível de instalação de uma instalação completa do produto.          |
| [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | Verifica se há espaço em disco suficiente.                                    |



 

## <a name="user-interface-functions"></a>Funções da interface do usuário



| Função                                           | Descrição                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | Habilita o modo de visualização da interface do usuário.                             |
| [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | Exibe um mural com o controle de host na caixa de diálogo exibida. |
| [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | Exibe uma caixa de diálogo como sem janela restrita e inativa.                         |



 

Todas as funções oferecem suporte a chamadas ANSI e Unicode. Para usar essas funções, inclua MsiQuery. h e vincule a MSI. lib.

## <a name="installation-functions"></a>Funções de instalação

Além das funções de acesso ao banco de dados listadas acima, você cria um pacote de instalação para um aplicativo usando as funções do instalador listadas na seção de [referência da função do instalador](installer-function-reference.md) .

 

 



