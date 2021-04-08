---
description: A tabela de registro e as tabelas relacionadas do banco de dados de instalação contêm as informações de registro que o aplicativo precisa gravar no registro do sistema.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Adicionando informações do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb299116b4e5c567d1e1f4b18f23c1e5b0447fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921525"
---
# <a name="adding-registry-information"></a>Adicionando informações do registro

A [tabela de registro](registry-table.md)e as tabelas relacionadas do banco de dados de instalação contêm as informações de registro que o aplicativo precisa gravar no registro do sistema. Consulte o [grupo tabelas do registro](registry-tables-group.md). Nesta seção, você adiciona as informações que serão registradas no computador do usuário pela amostra do bloco de notas.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela vazia do registro.

[Tabela do registro](registry-table.md)



| Registro       | Root | Chave                                 | Nome             | Valor    | Componente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfCharSet        | \#0      | Bloco de notas     |
| ClipPrecision  | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfClipPrecision  | \#2      | Bloco de notas     |
| Escapement     | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfFaceName       | FixedSys | Bloco de notas     |
| Itálico         | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfItalic         | \#0      | Bloco de notas     |
| Orientation    | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfOrientation    | \#0      | Bloco de notas     |
| Inprecisão   | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfOutPrecision   | \#1      | Bloco de notas     |
| PageSettings   | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | fSavePageSetting | \#0      | Bloco de notas     |
| PitchAndFamily | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfPitchAndFamily | \#49     | Bloco de notas     |
| Pontos      | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | iPointSize       | \#120    | Bloco de notas     |
| Qualidade        | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfQuality        | \#2      | Bloco de notas     |
| Riscado      | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfStrikeOut      | \#0      | Bloco de notas     |
| Peso         | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | lfWeight         | \#400    | Bloco de notas     |
| Encapsular           | 2    | Exemplo de SOFTWARE da \\ Microsoft no \\ bloco de notas | fWrap            | \#0      | Bloco de notas     |



 

[Continuar](specifying-shortcuts.md)

 

 



