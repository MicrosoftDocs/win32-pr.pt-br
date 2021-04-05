---
description: O Windows Installer instala e remove blocos de recursos referidos como Windows Installer componentes. Para obter mais informações, consulte principais grupos de tabelas e componentes e recursos.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Especificando componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98cb254498236b85ab5c2bc0df3bd32892227b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827285"
---
# <a name="specifying-components"></a>Especificando componentes

O Windows Installer instala e remove blocos de recursos referidos como [Windows Installer componentes](windows-installer-components.md). Para obter mais informações, consulte [principais grupos de tabelas](core-tables-group.md) e [componentes e recursos](components-and-features.md).

Nesta seção, você adiciona informações sobre os componentes usados pelo exemplo do bloco de notas à [tabela de componentes](component-table.md) criada na [importação de um banco de dados em branco](importing-a-blank-database.md). Para obter mais informações, consulte [organizando aplicativos em componentes](organizing-applications-into-components.md) e [definindo componentes do instalador](defining-installer-components.md).

O exemplo do bloco de notas usa oito componentes para controlar os recursos.



| Componente | Recursos                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Beisebol  | Baseball.txt, sBaseball                                                                                               |
| Concerto   | Concert.txt, sConcert                                                                                                 |
| Dance     | Dance.txt, sDance                                                                                                     |
| Comemorar  | Football.txt, sFootball                                                                                               |
| Ajuda      | Help.txt, sHelp                                                                                                       |
| Janeiro   | January.txt, sJanuary                                                                                                 |
| NewYears  | NewYears.txt, sNewYears                                                                                               |
| Bloco de notas   | Redpark.exe, Readme.txt, sReadme, sNotepad, **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **notepad exemplo** |



 

Cada componente deve ser identificado com um [GUID](guid.md)de ID de componente exclusivo. Se você estiver reproduzindo o exemplo, não reutilize os mesmos GUIDs de ID de componente na tabela a seguir. Em vez disso, use um utilitário como Guidgen.exe para gerar novos GUIDs para seus componentes.

Certifique-se de usar uma cadeia de caracteres GUID consistente com o tipo de dados Windows Installer GUID. Para obter mais informações, consulte [alterando o código do componente](changing-the-component-code.md) e [o que acontece se as regras de componente forem interrompidas?](what-happens-if-the-component-rules-are-broken.md)

Use Orca ou outro editor de banco de dados para inserir os dados a seguir na [tabela de componentes](component-table.md) em branco de MNP2000.msi. Não reutilize os GUIDs mostrados abaixo na coluna ComponentID no seu exemplo.



| Componente | ComponentId                            | Diretório\_ | Atributos | Condição | KeyPath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Beisebol  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concerto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| Dance     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| Comemorar  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Ajuda      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| Janeiro   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloco de notas   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

Os diretórios de origem e de destino para cada componente são especificados pelo valor inserido na \_ coluna diretório. O instalador resolve o local desse diretório usando as informações na tabela de diretórios. O instalador usa os arquivos de caminho de chave especificados na coluna KeyPath para detectar cada componente. Os atributos de execução remota são definidos no exemplo para que os componentes possam ser executados da origem ou executados localmente.

[Continuar](specifying-files-and-file-attributes.md)

 

 



