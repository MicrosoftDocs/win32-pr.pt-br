---
description: O arquivo VBScript WiSubStg.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Gerenciar Substorages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f6d3a0716854755e595133771ede65b11212cdd0fd19b4502bab0c631a9d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945591"
---
# <a name="manage-substorages"></a>Gerenciar Substorages

O arquivo VBScript WiSubStg.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) Este exemplo mostra como o script pode ser usado para gerenciar substorages em um banco de Windows do Instalador. Uma transformação pode ser adicionada a um banco de dados Windows instalador existente como um substorage.

O exemplo demonstra o uso de:

-   [\_Tabela de armazenamentos](-storages-table.md)
-   [**Método OpenDatabase (Objeto do Instalador)**](installer-opendatabase.md)
-   [**Método CreateRecord**](installer-createrecord.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método commit do**](database-commit.md) objeto [ **Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md)
-   [**Modificar método**](view-modify.md)
-   [**Método Execute**](view-execute.md) do [ **objeto View**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md)
-   [**Método SetStream**](record-setstream.md) do [ **objeto Record**](record-object.md)

Você exigirá a versão CScript.exe ou WScript.exe do host Windows Script para usar este exemplo. Para usar CScript.exe executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiSubStg.vbs \[ caminho do banco de \] \[ dados para o nome \] \[ \] \[ do substorage de opções de arquivo\]**

Especifique o caminho para o banco Windows do Instalador para adicionar ou remover o substorage. Especifique um caminho para a transformação ou o arquivo de banco de dados que está sendo adicionado como substorage. Para listar os substorages no banco de dados Windows Instalador, omita o caminho para esse arquivo. Você pode especificar um nome de substorage opcional, se isso for omitido, o nome do substorage assume como padrão o nome do arquivo.

A opção a seguir pode ser especificada.



| Opção              | Descrição                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| nenhuma opção especificada | Adicione um substorage ao banco de dados Windows instalador.                                                 |
| /d                  | Remova um substorage. Esse sinalizador de opção deve ser seguido pelo nome do substorage a ser removido. |



 

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows Host de Script, consulte Windows Ferramentas de Desenvolvimento [do Instalador](windows-installer-development-tools.md)do .

Observe que [um exemplo de localização](a-localization-example.md) demonstra [a incorporação de transformaçãos de personalização como substorage](embedding-customization-transforms-as-substorage.md).

 

 



