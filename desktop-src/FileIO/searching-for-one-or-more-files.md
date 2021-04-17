---
description: Um aplicativo pode pesquisar o diretório atual em busca de todos os nomes de arquivo que correspondam a um determinado padrão usando as funções FindFirstfile, FindFirstFileEx, FindNextFile e FindClose.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Procurando um ou mais arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775750"
---
# <a name="searching-for-one-or-more-files"></a>Procurando um ou mais arquivos

Um aplicativo pode pesquisar o diretório atual em busca de todos os nomes de arquivo que correspondam a um determinado padrão usando as funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) . O padrão deve ser um nome de arquivo válido e pode incluir caracteres curinga.

As funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) criam identificadores que o **FindFirstFileEx** usa para pesquisar outros arquivos com o mesmo padrão. Todas as funções retornam informações sobre o arquivo encontrado. Essas informações incluem o nome do arquivo, o tamanho, os atributos e a hora.

A função [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) também permite que um aplicativo pesquise arquivos com base em critérios de pesquisa adicionais. A função pode limitar pesquisas a nomes de dispositivos ou nomes de diretório.

A função [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) destrói os identificadores criados por [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).

Um aplicativo pode pesquisar um único arquivo em um caminho específico usando a função [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .

 

 
