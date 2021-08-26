---
description: quando a instalação de um aplicativo existente é movida para Windows Installer de outra tecnologia de instalação, o desenvolvedor da instalação pode começar a criar um pacote de Windows Installer usando as imagens de arquivo de origem e de destino da instalação existente.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Planejando a instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d406ec97fd5edb34468586eb9f707eff32b289df3dc88b803b8c55d4aad10cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042356"
---
# <a name="planning-the-installation"></a>Planejando a instalação

quando a instalação de um aplicativo existente é movida para Windows Installer de outra tecnologia de instalação, o desenvolvedor da instalação pode começar a criar um pacote de Windows Installer usando as imagens de arquivo de origem e de destino da instalação existente. Um plano detalhado de como os arquivos e outros recursos são organizados na origem e no destino também é um bom ponto de partida para o desenvolvimento de um pacote para um novo aplicativo.

O pacote de instalação de exemplo usa os seguintes arquivos que são armazenados no local de origem do aplicativo e os instala no destino no computador do usuário.



| Arquivo         | Descrição                               | Caminho para a origem                                    | Caminho para o destino                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | Arquivo executável do editor de texto.              | C: \\ Bloco de notas de exemplo \\ \\Redpark.exe                  | \[\] \\Redpark.exe de \_ estacionamento \\ vermelho ProgramFilesFolder          |
| Readme.txt   | Um arquivo informativo.                    | C: \\ Bloco de notas de exemplo \\ \\Readme.txt                   | \[\] \\Readme.txt de \_ estacionamento \\ vermelho ProgramFilesFolder           |
| Help.txt     | Manual de ajuda                               | C: \\ Bloco de notas de exemplo \\ \\Help.txt                     | Não instalado. Sempre executar de origem.                  |
| Baseball.txt | Agenda de jogo de beisebol para o ano 2000.     | C: \\ Bloco de notas de eventos de exemplo \\ \\ \\Baseball.txt         | \[\] \\Baseball.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| Football.txt | Agenda de jogo de futebol para o ano 2000.     | C: \\ Bloco de notas de eventos de exemplo \\ \\ \\Football.txt         | \[\] \\Football.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| Dance.txt    | Desempenho de dança para o ano 2000.         | C: \\ Bloco de notas de eventos de exemplo \\ \\ \\Dance.txt            | \[\] \\Dance.txt ProgramFilesFolder Red \_ Park \\ Arts \\      |
| Concert.txt  | Desempenho de música para o ano 2000.         | C: \\ Bloco de notas de eventos de exemplo \\ \\ \\Concert.txt          | \[\] \\Concert.txt ProgramFilesFolder Red \_ Park \\ Arts \\    |
| January.txt  | Admissões em Janeiro do ano de 2000.       | C: \\ portão de Bloco de notas de exemplo \\ \\ \\January.txt            | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\January.txt    |
| NewYears.txt | As admissões no ano novo dia 2000. | C: \\ exemplos \\ de \\ feriados do Gate Bloco de notas \\ \\NewYears.txt | \[ProgramFilesFolder \] \\ \_ portão de estacionamento vermelho \\ \\NewYears.txt   |



 

o exemplo grava os seguintes valores no registro do usuário em **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Bloco de notas sample**.



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
| sHelp     | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\ Bloco de notas de exemplo ProgramFilesFolder \\ \\Help.txt       |
| sBaseball | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Baseball.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| sFootball | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Football.txt de \_ esportes de estacionamento vermelho \\ \\ ProgramFilesFolder |
| sDance    | \[\] \\ Menu de \_ estacionamento \\ vermelho ProgramFilesFolder\\ | \[\] \\Dance.txt ProgramFilesFolder Red \_ Park \\ Arts \\      |
| sConcert  | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Concert.txt \\    |
| sJanuary  | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| sNewYears | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |



 

Para reproduzir o exemplo, comece criando a estrutura de diretório de origem determinada na primeira tabela. Você pode fazer uma cópia do arquivo de Notepad.exe do sistema e renomear essa cópia Redpark.exe. Use o editor Bloco de notas para criar os arquivos de texto restantes. A estrutura de diretório do destino, os valores do Registro e os atalhos são adicionados com a criação do banco de dados de instalação.

[Continuar](importing-a-blank-database.md)

 

 



