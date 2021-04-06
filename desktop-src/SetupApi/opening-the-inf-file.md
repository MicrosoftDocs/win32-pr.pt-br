---
description: Você deve usar a função SetupOpenInfFile para abrir o arquivo INF antes de poder recuperar informações dele ou acrescentar outros arquivos INF a ele.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Abrindo o arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828689"
---
# <a name="opening-the-inf-file"></a><span data-ttu-id="d7c90-103">Abrindo o arquivo INF</span><span class="sxs-lookup"><span data-stu-id="d7c90-103">Opening the INF File</span></span>

<span data-ttu-id="d7c90-104">Você deve usar a função [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) para abrir o arquivo inf antes de poder recuperar informações dele ou acrescentar outros arquivos INF a ele.</span><span class="sxs-lookup"><span data-stu-id="d7c90-104">You must use the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function to open the INF file before you can retrieve information from it, or append other INF files to it.</span></span>

<span data-ttu-id="d7c90-105">O seguinte abre um arquivo INF usando [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) e retorna um identificador, MyInf, para o arquivo inf aberto.</span><span class="sxs-lookup"><span data-stu-id="d7c90-105">The following opens an INF file using [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) and returns a handle, MyInf, to the opened INF file.</span></span> <span data-ttu-id="d7c90-106">O parâmetro *InfClass* de **SetupOpenInfFile** é especificado como **NULL** para indicar que a classe do arquivo inf deve ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="d7c90-106">The *InfClass* parameter of **SetupOpenInfFile** is specified as **NULL** to indicate that the Class of the INF file should be ignored.</span></span>


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



<span data-ttu-id="d7c90-107">Depois que um arquivo INF é aberto, você pode chamar a função [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) para acrescentar um arquivo ao arquivo inf aberto.</span><span class="sxs-lookup"><span data-stu-id="d7c90-107">After an INF file is opened, you can call the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function to append a file to the open INF file.</span></span> <span data-ttu-id="d7c90-108">Para acrescentar vários arquivos, repita esse processo.</span><span class="sxs-lookup"><span data-stu-id="d7c90-108">To append several files, repeat this process.</span></span> <span data-ttu-id="d7c90-109">Se você chamar a função **SetupOpenAppendInfFile** e o nome de arquivo passado para ela for **NULL**, a função pesquisará a seção versão do arquivo inf aberto (e todos os arquivos INF anexados) de uma chave de layoutfile.</span><span class="sxs-lookup"><span data-stu-id="d7c90-109">If you call the **SetupOpenAppendInfFile** function and the filename passed to it is **NULL**, then the function will search the Version section of the open INF file (and any appended INF files) for a LayoutFile key.</span></span> <span data-ttu-id="d7c90-110">Se a função encontrar uma chave, ela acrescentará o arquivo especificado por essa chave (geralmente o LAYOUT. INF).</span><span class="sxs-lookup"><span data-stu-id="d7c90-110">If the function finds a key, it will append the file specified by that key (usually LAYOUT.INF).</span></span> <span data-ttu-id="d7c90-111">Quando vários arquivos INF tiverem sido combinados, o **SetupOpenAppendInfFile** começará com o último arquivo inf acrescentado quando procurar uma seção de versão.</span><span class="sxs-lookup"><span data-stu-id="d7c90-111">When multiple INF files have been combined, **SetupOpenAppendInfFile** starts with the last appended INF file when it searches for a Version section.</span></span>

 

 



