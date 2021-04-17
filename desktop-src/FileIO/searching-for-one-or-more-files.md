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
# <a name="searching-for-one-or-more-files"></a><span data-ttu-id="09b97-103">Procurando um ou mais arquivos</span><span class="sxs-lookup"><span data-stu-id="09b97-103">Searching for One or More Files</span></span>

<span data-ttu-id="09b97-104">Um aplicativo pode pesquisar o diretório atual em busca de todos os nomes de arquivo que correspondam a um determinado padrão usando as funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="09b97-104">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span> <span data-ttu-id="09b97-105">O padrão deve ser um nome de arquivo válido e pode incluir caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="09b97-105">The pattern must be a valid file name and can include wildcard characters.</span></span>

<span data-ttu-id="09b97-106">As funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) criam identificadores que o **FindFirstFileEx** usa para pesquisar outros arquivos com o mesmo padrão.</span><span class="sxs-lookup"><span data-stu-id="09b97-106">The [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) functions create handles that **FindFirstFileEx** uses to search for other files with the same pattern.</span></span> <span data-ttu-id="09b97-107">Todas as funções retornam informações sobre o arquivo encontrado.</span><span class="sxs-lookup"><span data-stu-id="09b97-107">All functions return information about the file that was found.</span></span> <span data-ttu-id="09b97-108">Essas informações incluem o nome do arquivo, o tamanho, os atributos e a hora.</span><span class="sxs-lookup"><span data-stu-id="09b97-108">This information includes the file name, size, attributes, and time.</span></span>

<span data-ttu-id="09b97-109">A função [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) também permite que um aplicativo pesquise arquivos com base em critérios de pesquisa adicionais.</span><span class="sxs-lookup"><span data-stu-id="09b97-109">The [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) function also allows an application to search for files based on additional search criteria.</span></span> <span data-ttu-id="09b97-110">A função pode limitar pesquisas a nomes de dispositivos ou nomes de diretório.</span><span class="sxs-lookup"><span data-stu-id="09b97-110">The function can limit searches to device names or directory names.</span></span>

<span data-ttu-id="09b97-111">A função [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) destrói os identificadores criados por [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span><span class="sxs-lookup"><span data-stu-id="09b97-111">The [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function destroys handles created by [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span></span>

<span data-ttu-id="09b97-112">Um aplicativo pode pesquisar um único arquivo em um caminho específico usando a função [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .</span><span class="sxs-lookup"><span data-stu-id="09b97-112">An application can search for a single file on a specific path by using the [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) function.</span></span>

 

 
