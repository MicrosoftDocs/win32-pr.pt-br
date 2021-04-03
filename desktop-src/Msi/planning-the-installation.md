---
description: Quando a instalação de um aplicativo existente é movida para Windows Installer de outra tecnologia de instalação, o desenvolvedor da instalação pode começar a criar um pacote de Windows Installer usando as imagens de arquivo de origem e de destino da instalação existente.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Planejando a instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb98368c5c5c8e13a8f9b03a44805a8cff6e517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828872"
---
# <a name="planning-the-installation"></a>Planejando a instalação

Quando a instalação de um aplicativo existente é movida para Windows Installer de outra tecnologia de instalação, o desenvolvedor da instalação pode começar a criar um pacote de Windows Installer usando as imagens de arquivo de origem e de destino da instalação existente. Um plano detalhado de como os arquivos e outros recursos são organizados na origem e no destino também é um bom ponto de partida para o desenvolvimento de um pacote para um novo aplicativo.

O pacote de instalação de exemplo usa os seguintes arquivos que são armazenados no local de origem do aplicativo e os instala no destino no computador do usuário.



| Arquivo         | Descrição                               | Caminho para a origem                                    | Caminho para o destino                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | Arquivo executável do editor de texto.              | C: \\Redpark.exe do bloco de notas de exemplo \\ \\                  | \[\] \\Redpark.exe de \_ estacionamento \\ vermelho ProgramFilesFolder          |
| Readme.txt   | Um arquivo informativo.                    | C: \\Readme.txt do bloco de notas de exemplo \\ \\                   | \[\] \\Readme.txt de \_ estacionamento \\ vermelho ProgramFilesFolder           |
| Help.txt     | Manual de ajuda                               | C: \\Help.txt do bloco de notas de exemplo \\ \\                     | Não instalado. Sempre executar de origem.                  |
| Baseball.txt | Agenda de jogo de beisebol para o ano 2000.     | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Baseball.txt         | \[\] \\Baseball.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| Football.txt | Agenda de jogo de futebol para o ano 2000.     | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Football.txt         | \[\] \\Football.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| Dance.txt    | Desempenho de dança para o ano 2000.         | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Dance.txt            | \[\] \\Dance.txt ProgramFilesFolder Red \_ Park \\ Arts \\      |
| Concert.txt  | Desempenho de música para o ano 2000.         | C: \\ eventos de exemplo do \\ bloco de notas \\ \\Concert.txt          | \[\] \\Concert.txt ProgramFilesFolder Red \_ Park \\ Arts \\    |
| January.txt  | Admissões em Janeiro do ano de 2000.       | C: \\ porta do bloco de notas de exemplo \\ \\ \\January.txt            | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\January.txt    |
| NewYears.txt | As admissões no ano novo dia 2000. | C: \\ exemplo de \\ feriados do bloco de notas \\ \\ \\NewYears.txt | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\NewYears.txt   |



 

O exemplo grava os seguintes valores no registro do usuário em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ notepad Sample**.



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



 

O exemplo instala os atalhos a seguir. Um desses atalhos pode ser selecionado durante a instalação como um atalho anunciado para que o usuário possa instalar o recurso de beisebol sob demanda.



| Nome      | Local do atalho                         | Destino do atalho                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| sNotepad  | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Redpark.exe de \_ estacionamento \\ vermelho ProgramFilesFolder          |
| sReadme   | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Readme.txt de \_ estacionamento \\ vermelho ProgramFilesFolder           |
| sHelp     | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Help.txt do \\ bloco de notas \\ ProgramFilesFolder       |
| sBaseball | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Baseball.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| sFootball | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Football.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| sDance    | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Dance.txt ProgramFilesFolder Red \_ Park \\ Arts \\      |
| sConcert  | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Concert.txt ProgramFilesFolder Red \_ Park \\ Arts \\    |
| sJanuary  | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\January.txt    |
| sNewYears | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\NewYears.txt   |



 

Para reproduzir o exemplo, comece criando a estrutura do diretório de origem fornecida na primeira tabela. Você pode fazer uma cópia do arquivo de Notepad.exe do seu sistema e, em seguida, renomear essa cópia Redpark.exe. Use o editor do bloco de notas para criar os arquivos de texto restantes. A estrutura de diretório do destino, os valores do registro e os atalhos são adicionados por meio da criação do banco de dados de instalação.

[Continuar](importing-a-blank-database.md)

 

 



