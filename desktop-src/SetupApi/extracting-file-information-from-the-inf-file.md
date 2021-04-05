---
description: Depois que o arquivo INF for aberto, você poderá coletar informações dele para criar a interface do usuário ou para direcionar o processo de instalação. As funções de instalação fornecem vários níveis de funcionalidade para a coleta de informações de um arquivo INF.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Extraindo informações de arquivo do arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827329"
---
# <a name="extracting-file-information-from-the-inf-file"></a><span data-ttu-id="131f1-104">Extraindo informações de arquivo do arquivo INF</span><span class="sxs-lookup"><span data-stu-id="131f1-104">Extracting File Information from the INF file</span></span>

<span data-ttu-id="131f1-105">Depois que o arquivo INF for aberto, você poderá coletar informações dele para criar a interface do usuário ou para direcionar o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="131f1-105">After the INF file is opened, you can gather information from it to build the user interface, or to direct the installation process.</span></span> <span data-ttu-id="131f1-106">As funções de instalação fornecem vários níveis de funcionalidade para a coleta de informações de um arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="131f1-106">The setup functions provide several levels of functionality for gathering information from an INF file.</span></span>



| <span data-ttu-id="131f1-107">Para coletar informações...</span><span class="sxs-lookup"><span data-stu-id="131f1-107">To gather information…</span></span>                | <span data-ttu-id="131f1-108">Usar estas funções...</span><span class="sxs-lookup"><span data-stu-id="131f1-108">Use these functions…</span></span>                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="131f1-109">Sobre o arquivo INF</span><span class="sxs-lookup"><span data-stu-id="131f1-109">About the INF file</span></span>                    | [<span data-ttu-id="131f1-110">**SetupGetInfInformation**</span><span class="sxs-lookup"><span data-stu-id="131f1-110">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [<span data-ttu-id="131f1-111">**SetupQueryInfFileInformation**</span><span class="sxs-lookup"><span data-stu-id="131f1-111">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | <span data-ttu-id="131f1-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span><span class="sxs-lookup"><span data-stu-id="131f1-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span></span> |
| <span data-ttu-id="131f1-113">Sobre arquivos de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="131f1-113">About source and target files</span></span>         | [<span data-ttu-id="131f1-114">**SetupGetSourceFileLocation**</span><span class="sxs-lookup"><span data-stu-id="131f1-114">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [<span data-ttu-id="131f1-115">**SetupGetSourceFileSize**</span><span class="sxs-lookup"><span data-stu-id="131f1-115">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [<span data-ttu-id="131f1-116">**SetupGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="131f1-116">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [<span data-ttu-id="131f1-117">**SetupGetSourceInfo**</span><span class="sxs-lookup"><span data-stu-id="131f1-117">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| <span data-ttu-id="131f1-118">De uma linha de um arquivo INF</span><span class="sxs-lookup"><span data-stu-id="131f1-118">From a line of an INF file</span></span>            | [<span data-ttu-id="131f1-119">**SetupGetLineText**</span><span class="sxs-lookup"><span data-stu-id="131f1-119">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [<span data-ttu-id="131f1-120">**SetupFindNextLine**</span><span class="sxs-lookup"><span data-stu-id="131f1-120">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [<span data-ttu-id="131f1-121">**SetupFindNextMatchLine**</span><span class="sxs-lookup"><span data-stu-id="131f1-121">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [<span data-ttu-id="131f1-122">**SetupGetLineByIndex**</span><span class="sxs-lookup"><span data-stu-id="131f1-122">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [<span data-ttu-id="131f1-123">**SetupFindFirstLine**</span><span class="sxs-lookup"><span data-stu-id="131f1-123">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| <span data-ttu-id="131f1-124">De um campo de uma linha em um arquivo INF</span><span class="sxs-lookup"><span data-stu-id="131f1-124">From a field of a line in an INF file</span></span> | [<span data-ttu-id="131f1-125">**SetupGetStringField**</span><span class="sxs-lookup"><span data-stu-id="131f1-125">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [<span data-ttu-id="131f1-126">**SetupGetIntField**</span><span class="sxs-lookup"><span data-stu-id="131f1-126">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [<span data-ttu-id="131f1-127">**SetupGetBinaryField**</span><span class="sxs-lookup"><span data-stu-id="131f1-127">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [<span data-ttu-id="131f1-128">**SetupGetMultiSzField**</span><span class="sxs-lookup"><span data-stu-id="131f1-128">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

<span data-ttu-id="131f1-129">O exemplo a seguir usa a função [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) para recuperar a Descrição legível por humanos de uma mídia de origem de um arquivo inf.</span><span class="sxs-lookup"><span data-stu-id="131f1-129">The following example uses the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function to retrieve the human-readable description of a source media from an INF file.</span></span>


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



<span data-ttu-id="131f1-130">No exemplo, MyInf é o identificador para o arquivo INF aberto.</span><span class="sxs-lookup"><span data-stu-id="131f1-130">In the example, MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="131f1-131">SourceID é o identificador de uma mídia de origem específica.</span><span class="sxs-lookup"><span data-stu-id="131f1-131">SourceId is the identifier for a specific source media.</span></span> <span data-ttu-id="131f1-132">O valor SRCINFO \_ Descrição especifica que a função [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) deve recuperar a descrição da mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="131f1-132">The value SRCINFO\_DESCRIPTION specifies that the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function should retrieve the source media description.</span></span> <span data-ttu-id="131f1-133">O buffer aponta para uma cadeia de caracteres que receberá a descrição, MaxBufSize indica os recursos alocados para o buffer e BufSize indica os recursos necessários para armazenar o buffer.</span><span class="sxs-lookup"><span data-stu-id="131f1-133">Buffer points to a string that will receive the description, MaxBufSize indicates the resources allocated to the buffer, and BufSize indicates the resources necessary to store the buffer.</span></span>

<span data-ttu-id="131f1-134">Se BufSize for maior que MaxBufSize, a função retornará **false** e uma chamada subsequente para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um \_ buffer insuficiente de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="131f1-134">If BufSize is greater than MaxBufSize, the function will return **FALSE**, and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return ERROR\_INSUFFICIENT\_BUFFER.</span></span>

 

 
