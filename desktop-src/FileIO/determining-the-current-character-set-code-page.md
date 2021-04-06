---
description: A função AreFileApisANSI determina se as funções de e/s de arquivo estão usando a página de código do conjunto de caracteres ANSI ou OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Determinando a página de código do conjunto de caracteres atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828602"
---
# <a name="determining-the-current-character-set-code-page"></a><span data-ttu-id="dda10-103">Determinando a página de código do conjunto de caracteres atual</span><span class="sxs-lookup"><span data-stu-id="dda10-103">Determining the Current Character Set Code Page</span></span>

<span data-ttu-id="dda10-104">A função [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se as funções de e/s de arquivo estão usando a página de código do conjunto de caracteres ANSI ou OEM.</span><span class="sxs-lookup"><span data-stu-id="dda10-104">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span> <span data-ttu-id="dda10-105">A função [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) faz com que as funções usem a página de código ANSI.</span><span class="sxs-lookup"><span data-stu-id="dda10-105">The [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) function causes the functions to use the ANSI code page.</span></span> <span data-ttu-id="dda10-106">A função [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) faz com que as funções usem a página de código OEM.</span><span class="sxs-lookup"><span data-stu-id="dda10-106">The [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) function causes the functions to use the OEM code page.</span></span>

<span data-ttu-id="dda10-107">Por padrão, as funções de e/s de arquivo usam nomes de arquivo ANSI.</span><span class="sxs-lookup"><span data-stu-id="dda10-107">By default, file I/O functions use ANSI file names.</span></span> <span data-ttu-id="dda10-108">As funções exportadas por Kernel32.dll que aceitam ou retornam nomes de arquivo são afetadas pela configuração da página de código do arquivo.</span><span class="sxs-lookup"><span data-stu-id="dda10-108">Functions exported by Kernel32.dll that accept or return file names are affected by the file code page setting.</span></span>

<span data-ttu-id="dda10-109">[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) e [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) definem a página de código por processo, em vez de por thread ou por computador.</span><span class="sxs-lookup"><span data-stu-id="dda10-109">Both [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) and [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) set the code page per process, rather than per thread or per computer.</span></span>

 

 



