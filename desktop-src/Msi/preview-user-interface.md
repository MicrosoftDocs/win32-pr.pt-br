---
description: O arquivo VBScript WiDialog.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como o script é usado para visualizar caixas de diálogo em um banco de dados Windows Installer.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Visualizar interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749786"
---
# <a name="preview-user-interface"></a>Visualizar interface do usuário

O arquivo VBScript WiDialog.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script é usado para visualizar caixas de diálogo em um banco de dados Windows Installer.

Este exemplo demonstra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md), o [**método CreateRecord**](installer-createrecord.md)e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md)
-   [**Método OpenView**](database-openview.md) e o [**método EnableUIpreview**](database-enableuipreview.md) do [**objeto Database**](database-object.md)
-   [**Método execute**](view-execute.md) e o [**método FETCH**](view-fetch.md) do [**objeto View**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md) Propertyof o [ **objeto Record**](record-object.md)

Este exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host. Para usar CScript.exe para este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiDialog.vbs** *\[ caminho para \] \[ nomes \] de caixa de diálogo do banco de dados*

Especifique o caminho para um banco de dados Windows Installer. Especifique o nome de uma caixa de diálogo. Esse nome deve ser listado na coluna caixa de diálogo da [tabela de diálogo](dialog-table.md). Para exibir um mural, acrescente o nome da caixa de diálogo com o nome do controle da [tabela de controle](control-table.md) e acrescente isso ao nome do mural na tabela do [mural](billboard-table.md). Se nenhuma caixa de diálogo for especificada, todas as caixas de diálogo na tabela de diálogo serão exibidas em sequência.

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



