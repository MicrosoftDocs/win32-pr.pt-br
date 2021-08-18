---
description: O Windows instalador do Windows instala e remove blocos de recursos chamados Windows Instalador. Para obter mais informações, consulte Grupo de tabelas principais e componentes e recursos.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Especificando componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2264784d3edaad5b46017e3d337f8abfec66e1b60d18ba54388b03beddb13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627996"
---
# <a name="specifying-components"></a>Especificando componentes

O Windows instalador do Windows instala e remove blocos de recursos chamados [de componentes Windows Instalador.](windows-installer-components.md) Para obter mais informações, consulte [Grupo de tabelas principais e](core-tables-group.md) [componentes e recursos](components-and-features.md).

Nesta seção, você adiciona informações sobre os componentes usados [](component-table.md) pelo Bloco de notas à Tabela de Componentes criada em Importando um banco de [dados em branco.](importing-a-blank-database.md) Para obter mais informações, consulte [Organizando aplicativos em componentes](organizing-applications-into-components.md) e [Definindo componentes do instalador](defining-installer-components.md).

O Bloco de notas exemplo usa oito componentes para controlar recursos.



| Componente | Recursos                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Beisebol  | Baseball.txt, sBaseball                                                                                               |
| Concerto   | Concert.txt, sConcert                                                                                                 |
| Dança     | Dance.txt, sDance                                                                                                     |
| Futebol  | Football.txt, sFootball                                                                                               |
| Ajuda      | Help.txt, sHelp                                                                                                       |
| Janeiro   | January.txt, sJanuary                                                                                                 |
| NewYears  | NewYears.txt, sNewYears                                                                                               |
| Bloco de notas   | Redpark.exe, Readme.txt, sReadme, sNotepad, **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Bloco de notas Sample** |



 

Cada componente deve ser identificado com um GUID de ID de [componente exclusivo.](guid.md) Se você estiver reproduzindo o exemplo, não reutilizar os mesmos GUIDs de ID de componente na tabela a seguir. Em vez disso, use um utilitário como Guidgen.exe para gerar novos GUIDs para seus componentes.

Certifique-se de usar uma cadeia de caracteres GUID consistente com o Windows de dados guid do instalador. Para obter mais informações, consulte [Alterando o código do componente e](changing-the-component-code.md) O que acontece se as regras do componente são [interrompidas?](what-happens-if-the-component-rules-are-broken.md)

Use Orca ou outro editor de banco de dados para inserir os dados a seguir na Tabela de [Componentes](component-table.md) em branco MNP2000.msi. Não reutilizar os GUIDs mostrados abaixo na coluna ComponentId em seu exemplo.



| Componente | Componentid                            | Diretório\_ | Atributos | Condição | Keypath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Beisebol  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concerto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | KANDIR     | 2          |           | Concert.txt  |
| Dança     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | KANDIR     | 2          |           | Dance.txt    |
| Futebol  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Ajuda      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| Janeiro   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloco de notas   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

Os diretórios de origem e destino para cada componente são especificados pelo valor inserido na coluna \_ Diretório. O instalador resolve o local desse diretório usando as informações na tabela Diretório. O instalador usa os arquivos de caminho de chave especificados na coluna KeyPath para detectar cada componente. Os atributos de execução remota são definidos no exemplo para que os componentes possam ser executados de origem ou executados localmente.

[Continuar](specifying-files-and-file-attributes.md)

 

 



