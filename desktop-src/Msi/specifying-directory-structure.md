---
description: O instalador mantém informações sobre a estrutura do diretório de instalação na Tabela de Diretórios.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Especificando a estrutura de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc71e448c03a7fdbdf9de249122246aaf0038769a1dd409551330a503be7e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627886"
---
# <a name="specifying-directory-structure"></a>Especificando a estrutura de diretório

O instalador mantém informações sobre a estrutura do diretório de instalação na [Tabela de Diretórios](directory-table.md). Consulte o [Grupo de Tabelas Principais](core-tables-group.md). Nesta seção, você adiciona informações de estrutura de diretório para o exemplo Bloco de notas ao banco de dados vazio criado em [Importando um banco de dados em branco.](importing-a-blank-database.md) Use o Orca do editor de banco de dados fornecido com o SDK ou outro editor para abrir a Tabela de Diretórios no MNP2000.msi. Use o editor para inserir os dados a seguir na tabela Diretório em branco.

[Tabela de diretórios](directory-table.md)



| Diretório                                        | Pai do \_ Diretório                                | Defaultdir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**Targetdir**](targetdir.md)                   |                                                  | SourceDir         |
| [**Programfilesfolder**](programfilesfolder.md) | [**Targetdir**](targetdir.md)                   | .                 |
| KANDIR                                          | NOTEPADDIR                                       | Feiras:Eventos       |
| HOLDIR                                           | MONDIR                                           | .:Holidays        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIR                                           | NOTEPADDIR                                       | Porta              |
| NOTEPADDIR                                       | [**Programfilesfolder**](programfilesfolder.md) | Red \_ Park:Bloco de notas |
| SPORTDIR                                         | NOTEPADDIR                                       | Sports:Events     |



 

Inserir esses dados na tabela Diretório especifica as estruturas de diretório de origem e de destino. Consulte os [tópicos Tabela de](directory-table.md) Diretório [e Usando a Tabela de](using-the-directory-table.md) Diretórios. Observe que a [**propriedade TARGETDIR**](targetdir.md) deve ser o nome de uma raiz na tabela Diretório de cada instalação.

[Continuar](specifying-components.md)

 

 



