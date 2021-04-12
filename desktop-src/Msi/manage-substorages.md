---
description: O arquivo VBScript WiSubStg.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Gerenciar subarmazenamentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297444"
---
# <a name="manage-substorages"></a>Gerenciar subarmazenamentos

O arquivo VBScript WiSubStg.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script pode ser usado para gerenciar subarmazenamentos em um banco de dados Windows Installer. Uma transformação pode ser adicionada a um banco de dados Windows Installer existente como um subarmazenamento.

O exemplo demonstra o uso de:

-   [\_Tabela de armazenamentos](-storages-table.md)
-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Método CreateRecord**](installer-createrecord.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md)
-   [**Modificar método**](view-modify.md)
-   [**Método execute**](view-execute.md) do [ **objeto View**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md)
-   [**Método SetStream**](record-setstream.md) do [ **objeto Record**](record-object.md)

Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo. Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiSubStg.vbs \[ caminho para o caminho do banco \] \[ de dados para opções de arquivo \] \[ \] \[ nome do subarmazenamento\]**

Especifique o caminho para o banco de dados de Windows Installer para adicionar ou remover o subarmazenamento. Especifique um caminho para a transformação ou o arquivo de banco de dados que está sendo adicionado como subarmazenamento. Para listar os subarmazenamentos no banco de dados Windows Installer, omita o caminho para esse arquivo. Você pode especificar um nome de subarmazenamento opcional, se for omitido, o nome do subarmazenamento padrão será o nome do arquivo.

A opção a seguir pode ser especificada.



| Opção              | Descrição                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| nenhuma opção especificada | Adicione um subarmazenamento ao banco de dados de Windows Installer.                                                 |
| /d                  | Remova um subarmazenamento. Esse sinalizador de opção deve ser seguido pelo nome do subarmazenamento a ser removido. |



 

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

Observe que [um exemplo de localização demonstra a](a-localization-example.md) [inserção de transformações de personalização como um subarmazenamento](embedding-customization-transforms-as-substorage.md).

 

 



