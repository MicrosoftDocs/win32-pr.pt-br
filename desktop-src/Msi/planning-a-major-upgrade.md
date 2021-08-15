---
description: Se Windows instalador for usado para a instalação e a instalação de um aplicativo, atualizações posteriores desse aplicativo poderão ser manipuladas instalando um pacote de atualização.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Planejando uma atualização principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07ece8acf0dbc37ecdfddaa3505e5e54a283a8e8efd7b4eb0dc1a0a365a461e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377367"
---
# <a name="planning-a-major-upgrade"></a>Planejando uma atualização principal

Se Windows instalador for usado para a instalação e a instalação de um aplicativo, atualizações posteriores desse aplicativo poderão ser manipuladas instalando um pacote de atualização. Os desenvolvedores de instalação podem optar por um pacote de atualização modificando o pacote de instalação original. Essa abordagem é ilustrada pelo exemplo de atualização a seguir.

A instalação do produto original, MNP2000, seguida da instalação do pacote de atualização fornece ao usuário os seguintes arquivos exigidos pelo produto MNP2001.



| Arquivo          | Descrição                                                    | Caminho para a origem                                    | Caminho para o destino                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | Arquivo executável do editor de texto. Inalterado em relação aos produtos anteriores. | C: \\ Exemplo \\ Bloco de notas \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| Readme.txt    | Um arquivo de informações. Inalterado em relação aos produtos anteriores.         | C: \\ Exemplo \\ Bloco de notas \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| Help.txt      | Manual de ajuda. Inalterado em relação aos produtos anteriores.                 | C: \\ Exemplo \\ Bloco de notas \\Help.txt                     | Não instalado. Sempre executar de origem.                  |
| Baseba01.txt  | Agenda do jogo de basebol do ano 2001.                          | C: \\ Exemplo de Bloco de notas eventos \\ \\ \\Baseba01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| Footba01.txt  | Agenda de jogos de futebol para o ano de 2001.                          | C: \\ Exemplo de Bloco de notas eventos \\ \\ \\Footba01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| Basket01.txt  | Agenda do jogo de basquete do ano 2001.                        | C: \\ Exemplo de Bloco de notas eventos \\ \\ \\Basket01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Basket01.txt |
| Dance01.txt   | Desempenhos de música para o ano de 2001.                              | C: \\ Exemplo de Bloco de notas eventos \\ \\ \\Dance01.txt          | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Dance.txt \\      |
| Concert01.txt | Desempenhos de música do ano 2001.                              | C: \\ Exemplo de Bloco de notas eventos \\ \\ \\Concer01.txt         | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Concert.txt \\    |
| Opera01.txt   | Desempenhos de opera do ano 2001.                              | C: \\ Exemplo de Bloco de notas eventos \\ \\ \\Opera01.txt          | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Opera01.txt \\    |
| Januar01.txt  | Admissões em janeiro do ano de 2001.                            | C: \\ Exemplo de Bloco de notas gate \\ \\ \\Januar01.txt           | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| NewYea01.txt  | Admissões no dia do ano novo de 2001.                      | C: \\ Exemplo de Bloco de notas \\ \\ \\ feriados de \\NewYea01.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |
| Memori01.txt  | Admissões no Dia do Ano de 2001.                       | C: \\ Exemplo de Bloco de notas \\ \\ \\ feriados de \\Memori01.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Memori01.txt   |



 

A instalação do pacote de atualização remove todos os recursos instalados com o produto original que não está sendo usado pelo produto atualizado.

Por exemplo, ao atualizar do MNP2000, a instalação da atualização remove os seguintes arquivos do computador do usuário:

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

A instalação do pacote de atualização grava os seguintes valores no registro do usuário em:

**HKEY \_ Exemplo \_ de software** de máquina local da \\  \\ **Microsoft** \\ **Bloco de notas**



| Nome             | Valor    |
|------------------|----------|
| Lfcharset        | 0        |
| LfClipPrecision  | 2        |
| Lffacename       | FixedSys |
| LfItalic         | 0        |
| LfOrientation    | 0        |
| LfOutPrecision   | 1        |
| fSavePageSetting | 0        |
| LfPitchAndFamily | 49       |
| iPointSize       | 120      |
| Lfquality        | 2        |
| LfStrikeOut      | 0        |
| Lfweight         | 400      |
| fWrap            | 0        |



 

A atualização atualiza atalhos antigos para os atalhos a seguir. Um desses atalhos pode ser selecionado durante a instalação como um atalho anunciado para que o usuário possa instalar sob demanda o recurso De basebol.



| Nome        | Local de atalho                         | Destino de atalho                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe            |
| sReadme     | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt             |
| sHelp       | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[Exemplo de ProgramFilesFolder \] \\ \\ Bloco de notas \\Help.txt         |
| sBaseball   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseba01.txt   |
| sFootball   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Footba01.txt   |
| sBasketball | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Basketba01.txt |
| sDance      | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Dance01.txt \\      |
| sConcert    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Concer01.txt \\     |
| sOpera      | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Opera01.txt \\      |
| sJanuary    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Januar01.txt     |
| sNewYears   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYea01.txt     |
| sMeiaal   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Memori01.txt     |



 

Quando um usuário desinstala o pacote de atualização, Windows Instalador remove completamente todas as versões do produto do computador do usuário. O usuário não é deixado com nenhuma parte de MNP2000 ou MNP2001.

[Continuar](importing-original-installation-database.md)

 

 



