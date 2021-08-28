---
description: O arquivo VBScript WiDialog.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores. Este exemplo mostra como o script é usado para visualizar diálogos em um banco de Windows do Instalador.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Visualização Interface do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572ab444cc2f6acb6ec426f842318201187336121aa9c2a0557fca8cab94a3ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074706"
---
# <a name="preview-user-interface"></a>Visualização Interface do Usuário

O arquivo VBScript WiDialog.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) Este exemplo mostra como o script é usado para visualizar diálogos em um banco de Windows do Instalador.

Este exemplo demonstra:

-   [**Método OpenDatabase (Objeto do Instalador),**](installer-opendatabase.md)o [**método CreateRecord**](installer-createrecord.md)e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**Objeto do Instalador**](installer-object.md)
-   [**Método OpenView e**](database-openview.md) o [**método EnableUIpreview**](database-enableuipreview.md) do Objeto [**de Banco de Dados**](database-object.md)
-   [**Método Execute**](view-execute.md) e o [**método Fetch**](view-fetch.md) do Objeto [**de Exibição**](view-object.md)
-   [**Propriedade StringDatado**](record-stringdata.md) Objeto [ **de Registro**](record-object.md)

Este exemplo requer a versão CScript.exe ou WScript.exe do host Windows Script. Para usar CScript.exe exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiDialog.vbs** *\[ caminho para nomes de caixa de diálogo do banco \] \[ de dados \]*

Especifique o caminho para um banco de Windows do Instalador. Especifique o nome de uma caixa de diálogo. Esse nome deve ser listado na coluna Caixa de diálogo da [tabela Dialog](dialog-table.md). Para exibir um mista, adefina o nome da [](control-table.md) caixa de diálogo com o nome do controle da tabela Controle e aenda-o ao nome dophone na tabela [Domá.](billboard-table.md) Se nenhuma caixa de diálogo for especificada, todas as caixas de diálogo na tabela Diálogo serão exibidas sequencialmente.

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows Host de Script, consulte Windows Ferramentas de Desenvolvimento [do Instalador](windows-installer-development-tools.md)do .

 

 



