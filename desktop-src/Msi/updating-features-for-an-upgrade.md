---
description: O pacote de atualização de Windows Installer de exemplo adiciona novos recursos ao produto original.
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: Atualizando recursos para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af072618bd0a2ba16a7f098d6b1129ba17c27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766381"
---
# <a name="updating-features-for-an-upgrade"></a>Atualizando recursos para uma atualização

O pacote de atualização de exemplo adiciona três novos recursos ao produto original:

-   O basquete, um novo recurso filho do recurso esporte.
-   Opera, um novo recurso filho do recurso de artes.
-   Memorial, um novo recurso filho do recurso Gate.

Use o editor de banco de dados para abrir MNP2001.msi e insira os dados a seguir na [tabela de recursos](feature-table.md).

[Tabela de recursos](feature-table.md)



| Recurso    | Pai do recurso \_ | Título         | Descrição                | Monitor | Nível | Diretório\_ | Atributos |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Artes       |                 | Artes          | Eventos de artes no parque vermelho.   | 18      | 3     | NOTEPADDIR  | 0          |
| Beisebol   | Esporte           | Beisebol      | Jogos de beisebol             | 17      | 3     | SPORTDIR    | 32         |
| Concerto    | Artes            | Concerto       | Eventos de concerto em Parque vermelho | 19      | 3     | ARTSDIR     | 2          |
| Dance      | Artes            | Dance         | Eventos da dança no parque vermelho   | 21      | 3     | ARTSDIR     | 2          |
| Comemorar   | Esporte           | Comemorar      | Jogos de futebol             | 13      | 3     | SPORTDIR    | 2          |
| Check       |                 | Check          | Admissões do Parque vermelho      | 6       | 3     | NOTEPADDIR  | 0          |
| Ajuda       | Bloco de notas         | Ajuda          | Arquivo de ajuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| Janeiro    | Check            | Janeiro       | Inmissões de janeiro         | 7       | 3     | MONDIR      | 2          |
| NewYears   | Janeiro         | Ano novo | Novos dias de admissão no ano   | 9       | 3     | HOLDIR      | 2          |
| Bloco de notas    |                 | Bloco de notas       | Editor do bloco de notas             | 1       | 3     | NOTEPADDIR  | 0          |
| Leiame     | Bloco de notas         | Leiame        | Arquivo Leiame                | 3       | 3     | NOTEPADDIR  | 0          |
| Esporte      |                 | Eventos de esporte  | Eventos de esporte no parque vermelho   | 12      | 3     | NOTEPADDIR  | 0          |
| Quadra | Esporte           | Quadra    | Jogos de basquete           | 15      | 3     | SPORTDIR    | 2          |
| Opera      | Artes            | Opera         | Desempenho do Opera         | 23      | 3     | ARTSDIR     | 2          |
| Memorial   | Check            | Dia de Memorial  | Inmissões de dia de Memorial    | 11      | 3     | HOLDIR      | 2          |



 

Use o editor de banco de dados para abrir MNP2001.msi e insira os dados a seguir na [tabela FeatureComponents](featurecomponents-table.md)vazia.



| Recurso\_  | Componente\_ |
|------------|-------------|
| Beisebol   | Beisebol    |
| Concerto    | Concerto     |
| Dance      | Dance       |
| Comemorar   | Comemorar    |
| Ajuda       | Ajuda        |
| Janeiro    | Janeiro     |
| NewYears   | NewYears    |
| Bloco de notas    | Bloco de notas     |
| Leiame     | Bloco de notas     |
| Quadra | Quadra  |
| Opera      | Opera       |
| Memorial   | Memorial    |



 

[Continuar](updating-shortcuts-for-an-upgrade.md)

 

 



