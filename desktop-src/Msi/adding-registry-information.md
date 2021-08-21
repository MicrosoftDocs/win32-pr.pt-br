---
description: A tabela de registro e as tabelas relacionadas do banco de dados de instalação contêm as informações de registro que o aplicativo precisa gravar no registro do sistema.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Adicionando informações do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df31ad20fef317d5d67f7f45a7b877511d4c35b05b1517c529693e787306b44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066406"
---
# <a name="adding-registry-information"></a>Adicionando informações do registro

A [tabela de registro](registry-table.md)e as tabelas relacionadas do banco de dados de instalação contêm as informações de registro que o aplicativo precisa gravar no registro do sistema. Consulte o [grupo tabelas do registro](registry-tables-group.md). nesta seção, você adiciona as informações que serão registradas no computador do usuário pelo Bloco de notas exemplo.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela vazia do registro.

[Tabela do registro](registry-table.md)



| Registro       | Root | Chave                                 | Nome             | Valor    | Componente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfCharSet        | \#0      | Bloco de notas     |
| ClipPrecision  | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfClipPrecision  | \#2      | Bloco de notas     |
| Escapement     | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfFaceName       | FixedSys | Bloco de notas     |
| Itálico         | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfItalic         | \#0      | Bloco de notas     |
| Orientation    | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfOrientation    | \#0      | Bloco de notas     |
| Inprecisão   | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfOutPrecision   | \#1      | Bloco de notas     |
| PageSettings   | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | fSavePageSetting | \#0      | Bloco de notas     |
| PitchAndFamily | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfPitchAndFamily | \#49     | Bloco de notas     |
| Pontos      | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | iPointSize       | \#120    | Bloco de notas     |
| Qualidade        | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfQuality        | \#2      | Bloco de notas     |
| Riscado      | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfStrikeOut      | \#0      | Bloco de notas     |
| Peso         | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | lfWeight         | \#400    | Bloco de notas     |
| Encapsular           | 2    | exemplo de SOFTWARE da \\ Microsoft \\ Bloco de notas | fWrap            | \#0      | Bloco de notas     |



 

[Continuar](specifying-shortcuts.md)

 

 



