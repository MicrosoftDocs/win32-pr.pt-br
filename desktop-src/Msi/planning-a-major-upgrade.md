---
description: Se Windows Installer for usado para a instalação e a configuração de um aplicativo, as atualizações posteriores desse aplicativo poderão ser tratadas pela instalação de um pacote de atualização.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Planejando uma atualização principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ca6b82e53a38dde8131525eb885a5f17603ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749787"
---
# <a name="planning-a-major-upgrade"></a>Planejando uma atualização principal

Se Windows Installer for usado para a instalação e a configuração de um aplicativo, as atualizações posteriores desse aplicativo poderão ser tratadas pela instalação de um pacote de atualização. Os desenvolvedores de instalação podem optar por criar um pacote de atualização modificando o pacote de instalação original. Essa abordagem é ilustrada pelo exemplo de atualização a seguir.

A instalação do produto original, MNP2000, seguida pela instalação do pacote de atualização fornece ao usuário os seguintes arquivos exigidos pelo produto MNP2001.



| Arquivo          | Descrição                                                    | Caminho para a origem                                    | Caminho para o destino                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | Arquivo executável do editor de texto. Inalterado de produtos anteriores. | C: \\Redpark.exe do bloco de notas de exemplo \\ \\                  | \[\] \\Redpark.exe de \_ estacionamento \\ vermelho ProgramFilesFolder          |
| Readme.txt    | Um arquivo de informações. Inalterado de produtos anteriores.         | C: \\Readme.txt do bloco de notas de exemplo \\ \\                   | \[\] \\Readme.txt de \_ estacionamento \\ vermelho ProgramFilesFolder           |
| Help.txt      | Manual de ajuda. Inalterado de produtos anteriores.                 | C: \\Help.txt do bloco de notas de exemplo \\ \\                     | Não instalado. Sempre executar de origem.                  |
| Baseba01.txt  | Agenda de jogo de beisebol para o ano 2001.                          | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Baseba01.txt         | \[\] \\Baseball.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| Footba01.txt  | Agenda de jogo de futebol para o ano 2001.                          | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Footba01.txt         | \[\] \\Football.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| Basket01.txt  | Agenda de jogo de basquete para o ano 2001.                        | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Basket01.txt         | \[\] \\Basket01.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| Dance01.txt   | Desempenho de dança para o ano 2001.                              | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Dance01.txt          | \[\] \\Dance.txt ProgramFilesFolder Red \_ Park \\ Arts \\      |
| Concert01.txt | Desempenho de música para o ano 2001.                              | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Concer01.txt         | \[\] \\Concert.txt ProgramFilesFolder Red \_ Park \\ Arts \\    |
| Opera01.txt   | Desempenho do Opera para o ano 2001.                              | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Opera01.txt          | \[\] \\Opera01.txt ProgramFilesFolder Red \_ Park \\ Arts \\    |
| Januar01.txt  | Admissões em Janeiro do ano de 2001.                            | C: \\ porta do bloco de notas de exemplo \\ \\ \\Januar01.txt           | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\January.txt    |
| NewYea01.txt  | As admissões no ano novo dia 2001.                      | C: \\ exemplo de \\ feriados do bloco de notas \\ \\ \\NewYea01.txt | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\NewYears.txt   |
| Memori01.txt  | Admissões no dia de Memorial do ano 2001.                       | C: \\ exemplo de \\ feriados do bloco de notas \\ \\ \\Memori01.txt | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\Memori01.txt   |



 

A instalação do pacote de atualização remove todos os recursos instalados com o produto original que não estão sendo usados pelo produto atualizado.

Por exemplo, ao atualizar do MNP2000, a instalação da atualização remove os seguintes arquivos do computador do usuário:

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

A instalação do pacote de atualização grava os seguintes valores no registro do usuário em:

**HKEY \_ Exemplo \_** de software da máquina local \\  \\ **Microsoft** \\ **notepad**



| Nome             | Valor    |
|------------------|----------|
| lfCharSet        | 0        |
| lfClipPrecision  | 2        |
| lfFaceName       | FixedSys |
| lfItalic         | 0        |
| lfOrientation    | 0        |
| lfOutPrecision   | 1        |
| fSavePageSetting | 0        |
| lfPitchAndFamily | 49       |
| iPointSize       | 120      |
| lfQuality        | 2        |
| lfStrikeOut      | 0        |
| lfWeight         | 400      |
| fWrap            | 0        |



 

A atualização atualiza atalhos antigos para os atalhos a seguir. Um desses atalhos pode ser selecionado durante a instalação como um atalho anunciado para que o usuário possa instalar o recurso de beisebol sob demanda.



| Nome        | Local do atalho                         | Destino do atalho                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Redpark.exe de \_ estacionamento \\ vermelho ProgramFilesFolder            |
| sReadme     | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Readme.txt de \_ estacionamento \\ vermelho ProgramFilesFolder             |
| sHelp       | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Help.txt do \\ bloco de notas \\ ProgramFilesFolder         |
| sBaseball   | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Baseba01.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder   |
| sFootball   | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Footba01.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder   |
| sBasketball | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Basketba01.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| sDance      | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Dance01.txt ProgramFilesFolder Red \_ Park \\ Arts \\      |
| sConcert    | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Concer01.txt ProgramFilesFolder Red \_ Park \\ Arts \\     |
| sOpera      | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Opera01.txt ProgramFilesFolder Red \_ Park \\ Arts \\      |
| sJanuary    | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\Januar01.txt     |
| sNewYears   | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\NewYea01.txt     |
| sMemorial   | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\Memori01.txt     |



 

Quando um usuário desinstala o pacote de atualização, Windows Installer remove completamente todas as versões do produto do computador do usuário. O usuário não é deixado com nenhuma parte de MNP2000 ou MNP2001.

[Continuar](importing-original-installation-database.md)

 

 



