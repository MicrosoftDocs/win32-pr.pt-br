---
description: o arquivo VBScript WiMakCab.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. este exemplo mostra como o script é usado para gerar gabinetes de arquivo de um banco de dados Windows Installer.
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: Gerar gabinete de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca9e30822d0683aa09dc015ec2fd98d1f598c70e0fd63fd00f66a6bcdf3edf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581486"
---
# <a name="generate-file-cabinet"></a>Gerar gabinete de arquivo

o arquivo VBScript WiMakCab.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). este exemplo mostra como o script é usado para gerar gabinetes de arquivo de um banco de dados Windows Installer.

Este exemplo demonstra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md)
-   [**Método Commit**](database-commit.md), o [**método OpenView**](database-openview.md) e a [**Propriedade SummaryInformation (objeto Database)**](database-summaryinformation.md) do [**objeto Database**](database-object.md)
-   [**Método FETCH**](view-fetch.md), [**método execute**](view-execute.md) e [**método Modify**](view-modify.md) do [**objeto View**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md) e [**Propriedade IntegerData**](record-integerdata.md) do [**objeto Record**](record-object.md)
-   [**Método DoAction**](session-doaction.md), a [**Propriedade Property (objeto Session)**](session-session.md)e a [**propriedade Mode**](session-mode.md) do [**objeto Session**](session-object.md)

você precisará da versão CScript.exe ou WScript.exe do Host de Script Windows para usar este exemplo. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiMakCab.vbs \[ caminho para o nome base do banco de dados \] \[ \] \[ locais de origem opcionais\]**

Para gerar um gabinete, Makecab.exe deve estar no caminho. o utilitário Makecab.exe está incluído nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Observe que o exemplo não atualiza a [tabela de mídia](media-table.md) para lidar com vários gabinetes. Para substituir um gabinete incorporado, inclua as opções:/R/C/U/E.

Especifique o caminho para o banco de dados do instalador. Isso deve estar localizado na raiz da árvore de origem. Especifique o nome base que diferencia maiúsculas de minúsculas para os arquivos de gabinete gerados. Se o tipo de origem for compactado, todos os arquivos serão abertos na raiz. As opções a seguir podem ser especificadas em qualquer ponto na linha de comando.



| Opção              | Descrição                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| nenhuma opção especificada |                                                                                                                                           |
| /C                  | Execute a compactação. Se/C não for especificado, WiMakCab.vbs gerará apenas o arquivo DDF.                                                        |
| /L                  | Usar compactação LZX em vez de MSZIP                                                                                                      |
| /F                  | Limite o tamanho do gabinete para 1,44 MB de tamanho de disquete em vez de CD-ROM                                                                              |
| /U                  | Atualizar o banco de dados para fazer referência ao gabinete gerado                                                                                    |
| /E                  | Inserir o arquivo de gabinete no pacote do instalador como um fluxo                                                                               |
| /S                  | Usar números de sequência na tabela de arquivos ordenados por diretórios                                                                             |
| /R                  | Reverta para instalação sem gabinete, remova o gabinete se/E for especificado (a opção/R remove a propriedade SummaryInfo de bit compactada 15 & 2) |



 

para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). para utilitários de exemplo que não exigem Windows Host de Script, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



