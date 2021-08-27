---
description: O arquivo VBScript WiExport.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exportar arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7cab882778bce6d84412f53987c65211f70f4a8a10b52836ad993d8e813304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044435"
---
# <a name="export-files"></a>Exportar arquivos

O arquivo VBScript WiExport.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) Este exemplo mostra como escrever script para exportar tabelas para um banco de dados Windows Instalador. O exemplo de script se conecta a [**um objeto Instalador,**](installer-object.md) abre um banco de dados e exporta tabelas para arquivos arquivados.

O exemplo demonstra o uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto Installer**](installer-object.md)
-   [**Método de exportação**](database-export.md)
-   [**Método OpenView**](database-openview.md) do objeto [ **Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md) do [ **objeto View**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)

Você exigirá a versão CScript.exe ou WScript.exe do host Windows Script para usar este exemplo. Para usar CScript.exe executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiExport.vbs caminho do banco de dados para lista de nomes de tabela \[ \] \[ de opções \] \[ \] \[ de pasta\]**

Especifique o caminho para o banco de dados do instalador do qual as tabelas estão sendo exportadas. Especifique o caminho para a pasta na qual os arquivos de arquivo exportados devem ser copiados. Liste os nomes que confidenciais de caso das tabelas de [banco de](database-tables.md) dados que estão sendo exportadas. \*Especifique ' ' para exportar todas as tabelas, incluindo \_ SummaryInformation.

As opções a seguir podem ser especificadas em qualquer lugar na linha de comando antes da lista de nomes de tabela.



| Opção              | Descrição                                            |
|---------------------|--------------------------------------------------------|
| nenhuma opção especificada | Arquivos de arquivos exportados podem ter um nome de arquivo longo.      |
| /s                  | Forçar arquivos de arquivo exportados a ter nomes de arquivo curtos. |



 

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows Host de Script, consulte Windows Ferramentas de Desenvolvimento [do Instalador](windows-installer-development-tools.md)do .

 

 



