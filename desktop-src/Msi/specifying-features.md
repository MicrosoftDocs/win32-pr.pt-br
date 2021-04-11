---
description: O Microsoft Installer permite que os usuários instalem e removam blocos de funcionalidade de aplicativo que são chamados de recursos de Windows Installer.
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: Especificando recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf7463b30247e921fb440ada1cd6f00f8e96a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169839"
---
# <a name="specifying-features"></a>Especificando recursos

O Microsoft Installer permite que os usuários instalem e removam blocos de funcionalidade de aplicativo que são chamados de [recursos de Windows Installer](windows-installer-features.md). Nesta seção, você adiciona informações ao banco de dados de instalação sobre os recursos que estão disponíveis para o exemplo do bloco de notas. Para obter mais informações, consulte [principais grupos de tabelas](core-tables-group.md) e [componentes e recursos](components-and-features.md).

O exemplo do bloco de notas instala recursos em uma hierarquia de recursos pai e filho. Na lista a seguir, os recursos filho são recuados em relação ao seu recurso pai. Os recursos devem ser exibidos nessa ordem no [controle SelectionTree](selectiontree-control.md) da interface do usuário.

Bloco de notas

-   Leiame
-   Ajuda

Check

-   Janeiro
    -   NewYears

Esporte

-   Beisebol
-   Comemorar

Artes

-   Concerto
-   Dance

Use um editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na [tabela de recursos](feature-table.md)vazia.



| Recurso  | Pai do recurso \_ | Título         | Descrição                | Monitor | Nível | Diretório\_ | Atributos |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Artes     |                 | Artes          | Eventos de artes no parque vermelho.   | 20      | 3     | NOTEPADDIR  | 0          |
| Beisebol | Esporte           | Beisebol      | Jogos de beisebol             | 17      | 3     | SPORTDIR    | 32         |
| Concerto  | Artes            | Concerto       | Eventos de concerto em Parque vermelho | 21      | 3     | ARTSDIR     | 2          |
| Dance    | Artes            | Dance         | Eventos da dança no parque vermelho   | 23      | 3     | ARTSDIR     | 2          |
| Comemorar | Esporte           | Comemorar      | Jogos de futebol             | 19      | 3     | SPORTDIR    | 2          |
| Check     |                 | Check          | Admissões do Parque vermelho      | 6       | 3     | NOTEPADDIR  | 0          |
| Ajuda     | Bloco de notas         | Ajuda          | Arquivo de ajuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| Janeiro  | Check            | Janeiro       | Inmissões de janeiro         | 10      | 3     | MONDIR      | 2          |
| NewYears | Janeiro         | Ano novo | Novos dias de admissão no ano   | 11      | 3     | HOLDIR      | 2          |
| Bloco de notas  |                 | Bloco de notas       | Editor do bloco de notas             | 1       | 3     | NOTEPADDIR  | 0          |
| Leiame   | Bloco de notas         | Leiame        | Arquivo Leiame                | 3       | 3     | NOTEPADDIR  | 0          |
| Esporte    |                 | Eventos de esporte  | Eventos de esporte no parque vermelho   | 14      | 3     | NOTEPADDIR  | 0          |



 

[Continuar](specifying-feature-component-relationships.md)

 

 



