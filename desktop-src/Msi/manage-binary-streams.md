---
description: O arquivo VBScript WiStream.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Gerenciar fluxos binários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785430"
---
# <a name="manage-binary-streams"></a>Gerenciar fluxos binários

O arquivo VBScript WiStream.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script pode ser usado para gerenciar fluxos binários em um banco de dados Windows Installer. O exemplo pode ser usado para inserir gabinetes de arquivo compactados em um banco de dados. Este exemplo demonstra a operação da [ \_ tabela de fluxos](-streams-table.md) no banco de dados Windows Installer.

O exemplo também demonstra o uso de:

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

**cscript WiStream.vbs \[ caminho para o caminho do banco \] \[ de dados para opções de arquivo \] \[ \] \[ nome do fluxo\]**

Especifique o caminho para o banco de dados de Windows Installer que deve receber o fluxo. Especifique um caminho para o arquivo binário que contém os dados do fluxo. Para listar os fluxos no banco de dados do instalador, omita este caminho. Você pode especificar um nome de fluxo opcional, se isso for omitido, o padrão será o nome do arquivo.

A opção a seguir pode ser especificada.



| Opção              | Descrição                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| nenhuma opção especificada | Adicione um fluxo ao banco de dados de Windows Installer.                                                 |
| /d                  | Remover um fluxo. Esse sinalizador de opção deve ser seguido pelo nome do subarmazenamento que está sendo removido. |



 

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



