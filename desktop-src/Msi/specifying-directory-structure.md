---
description: O instalador mantém informações sobre a estrutura do diretório de instalação na tabela de diretórios.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Especificando a estrutura do diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827284"
---
# <a name="specifying-directory-structure"></a>Especificando a estrutura do diretório

O instalador mantém informações sobre a estrutura do diretório de instalação na [tabela de diretórios](directory-table.md). Consulte o [grupo tabelas principais](core-tables-group.md). Nesta seção, você adiciona informações de estrutura de diretório para o exemplo do bloco de notas ao banco de dados vazio que você criou na [importação de um banco de dados em branco](importing-a-blank-database.md). Use o editor de banco de dados Orca fornecido com o SDK ou outro editor para abrir a tabela de diretórios no MNP2000.msi. Use o editor para inserir os dados a seguir na tabela de diretório em branco.

[Tabela de diretórios](directory-table.md)



| Diretório                                        | Pai do diretório \_                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | Artes: eventos       |
| HOLDIR                                           | MONDIR                                           | .: Feriados        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIR                                           | NOTEPADDIR                                       | Check              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | \_Parque vermelho: bloco de notas |
| SPORTDIR                                         | NOTEPADDIR                                       | Esportes: eventos     |



 

A inserção desses dados na tabela de diretórios especifica as estruturas de diretório de origem e de destino. Consulte a [tabela de diretórios](directory-table.md) e [usando os tópicos da tabela de diretórios](using-the-directory-table.md) . Observe que a propriedade [**TARGETDIR**](targetdir.md) deve ser o nome de uma raiz na tabela de diretórios de cada instalação.

[Continuar](specifying-components.md)

 

 



