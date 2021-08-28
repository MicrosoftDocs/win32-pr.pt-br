---
description: o arquivo de exemplo de código VBScript WiTextIn.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copiar arquivo ANSI em um campo de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65f38425fac327abd8eddaf9183464355ae025bb209947c750d4e3414d9b917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631326"
---
# <a name="copy-ansi-file-into-a-database-field"></a>Copiar arquivo ANSI em um campo de banco de dados

o arquivo de exemplo de código VBScript WiTextIn.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). o exemplo mostra como um script pode ser usado para copiar um arquivo em um campo de texto de um banco de dados de Windows Installer e demonstra o processamento de seus principais.

O exemplo de código também mostra o seguinte:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md)
-   [**Método OpenView**](database-openview.md), o [**método Commit**](database-commit.md)e a [**Propriedade primarykeys**](database-primarykeys.md) do [**objeto Database**](database-object.md)
-   [**Método FETCH**](view-fetch.md) e o [**método Modify**](view-modify.md) do [**objeto View**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md) e [**método ReadStream**](record-readstream.md) do [**objeto Record**](record-object.md)

para usar o exemplo de código, você precisa da versão CScript.exe ou WScript.exe do Host de Script Windows.

**Para usar CScript.exe para executar este exemplo**

-   No prompt de comando, digite a seguinte sintaxe:

    **cscript WiTextIn.vbs \[ caminho para a tabela do banco de dados \] \[ nome da \] \[ coluna valores de chave primária \] \[ nome do \] \[ caminho para arquivo\]**

> [!Note]  
> A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados.

 

**Para redirecionar a saída para um arquivo**

-   Termine a linha de comando com o seguinte: **VBS > \[ caminho para o arquivo \] . T**

> [!Note]  
> O exemplo retorna um valor de 0 (zero) para êxito, 1 (um) se a ajuda for invocada e 2 (dois) se o script falhar.

 

A lista a seguir identifica os itens que você deve especificar:

-   especifique o caminho para o banco de dados de Windows Installer.
-   Especifique o nome da tabela de banco de dados.
-   Especifique todos os valores de chave primária para a linha, em ordem, e concatenados com dois-pontos.
-   Especifique um nome de coluna que não seja uma coluna de chave. Essa é a coluna na qual você deseja receber os dados.
-   Especifique o caminho para o arquivo de texto que está sendo copiado.

> [!Note]  
> Se o último argumento for omitido, o valor atual no campo será exibido.

 

para obter mais exemplos de script, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). para utilitários de exemplo que não exigem o Host de Script Windows, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



