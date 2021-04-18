---
description: A tabela ActionText contém o texto a ser exibido em uma caixa de diálogo de progresso e gravada no log para ações que levam muito tempo para serem executadas. O texto exibido consiste na descrição da ação e, opcionalmente, nos dados formatados da ação.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabela ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756746"
---
# <a name="actiontext-table"></a>Tabela ActionText

A tabela ActionText contém o texto a ser exibido em uma caixa de diálogo de progresso e gravada no log para ações que levam muito tempo para serem executadas. O texto exibido consiste na descrição da ação e, opcionalmente, nos dados formatados da ação.

A tabela ActionText tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Ação      | [Identificador](identifier.md) | S   | N        |
| Descrição | [Text](text.md)             | N   | S        |
| Modelo    | [Modelo](template.md)     | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

Nome da ação.

Chave de tabela primária.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Descrição localizada que é exibida na caixa de diálogo de progresso ou gravada no log quando a ação está em execução.

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Modelos
</dt> <dd>

Um modelo de formato localizado que é usado para formatar registros de dados de ação a serem exibidos durante a execução da ação. Se um modelo não for fornecido, os dados de ação não serão exibidos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Normalmente, as entradas na tabela ActionText referem-se a ações em tabelas de sequência. Há outras ações que o instalador executa que não estão listadas na tabela de sequência, mas que ainda precisam ser especificadas na tabela. A tabela a seguir identifica as entradas de tabela necessárias nas quais o nome e o modelo da ação devem ser criados exatamente como mostrado, mas a descrição pode ser personalizada.



| Ação          | Descrição                             | Modelo |
|-----------------|-----------------------------------------|----------|
| Reversão        | Desfaz ações.                         | \[1\]    |
| RollbackCleanup | Remove arquivos antigos.                      | \[1\]    |
| GenerateScript  | Gera operações do sistema para ação. | \[1\]    |



 

> [!Note]  
> O texto da ação só é exibido para ações executadas dentro do script de instalação. Portanto, o texto da ação só é exibido para ações sequenciadas entre as ações [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) .

 

Você pode importar uma tabela ActionText localizada para seu banco de dados usando Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). O SDK inclui uma tabela ActionText localizada para cada um dos idiomas listados na seção [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) . Se a tabela ActionText não for populada, o instalador carregará cadeias de caracteres localizadas para o idioma especificado pela propriedade [**ProductLanguage**](productlanguage.md) .

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



