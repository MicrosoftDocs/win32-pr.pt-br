---
description: Antes que as funções de instalação possam acessar informações no INF, você deve abri-las com uma chamada para a função SetupOpenInfFile. Essa função retorna um identificador para o arquivo INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Abrindo e fechando um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505951"
---
# <a name="opening-and-closing-an-inf-file"></a><span data-ttu-id="26bf1-104">Abrindo e fechando um arquivo INF</span><span class="sxs-lookup"><span data-stu-id="26bf1-104">Opening and Closing an INF file</span></span>

<span data-ttu-id="26bf1-105">Antes que as funções de instalação possam acessar informações no INF, você deve abri-las com uma chamada para a função [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) .</span><span class="sxs-lookup"><span data-stu-id="26bf1-105">Before the setup functions can access information in the INF, you must open it with a call to the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function.</span></span> <span data-ttu-id="26bf1-106">Essa função retorna um identificador para o arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="26bf1-106">This function returns a handle to the INF file.</span></span>

<span data-ttu-id="26bf1-107">Se você não souber o nome do arquivo INF que precisa abrir, poderá usar a função [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) para obter uma lista de arquivos INF em um diretório.</span><span class="sxs-lookup"><span data-stu-id="26bf1-107">If you do not know the name of the INF file that you need to open, you can use the [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) function to obtain a list of INF files in a directory.</span></span>

<span data-ttu-id="26bf1-108">Depois de abrir um arquivo INF, você pode acrescentar outros arquivos INF ao arquivo INF aberto usando a função [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) .</span><span class="sxs-lookup"><span data-stu-id="26bf1-108">After you open an INF file, you can append additional INF files to the opened INF file by using the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function.</span></span> <span data-ttu-id="26bf1-109">Isso é funcionalmente semelhante a uma instrução include.</span><span class="sxs-lookup"><span data-stu-id="26bf1-109">This is functionally similar to an include statement.</span></span> <span data-ttu-id="26bf1-110">Quando as funções de configuração subsequentes fazem referência a um arquivo INF aberto, elas também poderão acessar todas as informações armazenadas nos arquivos acrescentados.</span><span class="sxs-lookup"><span data-stu-id="26bf1-110">When subsequent setup functions reference an open INF file, they will also be able to access any information stored in the appended files.</span></span>

<span data-ttu-id="26bf1-111">Se você não especificar um arquivo INF durante a chamada para a função [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , o **SetupOpenAppendInfFile** acrescentará os arquivos especificados pela chave **layoutfile** na seção **versão** do arquivo inf aberto.</span><span class="sxs-lookup"><span data-stu-id="26bf1-111">If you do not specify an INF file during the call to the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function, **SetupOpenAppendInfFile** appends the file(s) specified by the **LayoutFile** key in the **Version** section of the open INF file.</span></span>

<span data-ttu-id="26bf1-112">Quando você não precisar mais das informações no arquivo INF, chame a função [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) para liberar os recursos alocados durante a chamada para [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span><span class="sxs-lookup"><span data-stu-id="26bf1-112">When you no longer need the information in the INF file, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function to release resources allocated during the call to [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span></span>

 

 



