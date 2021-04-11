---
title: Extraindo os exemplos de código
description: Embora os exemplos de código sejam divididos em uma série de lições do tutorial, os agrupamentos de exemplo apropriados podem ser facilmente extraídos da coleção.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363867"
---
# <a name="extracting-the-code-samples"></a><span data-ttu-id="4299c-103">Extraindo os exemplos de código</span><span class="sxs-lookup"><span data-stu-id="4299c-103">Extracting the Code Samples</span></span>

<span data-ttu-id="4299c-104">Embora os exemplos de código sejam divididos em uma série de lições do tutorial, os agrupamentos de exemplo apropriados podem ser facilmente extraídos da coleção.</span><span class="sxs-lookup"><span data-stu-id="4299c-104">Though the code samples are divided into a series of tutorial lessons, the appropriate sample groupings can easily be extracted from the collection.</span></span> <span data-ttu-id="4299c-105">A maioria dos diretórios de exemplo individuais tem como objetivo trabalhar em conjunto com pelo menos um outro diretório de exemplo.</span><span class="sxs-lookup"><span data-stu-id="4299c-105">Most of the individual sample directories are meant to work in conjunction with at least one other sample directory.</span></span> <span data-ttu-id="4299c-106">Os exemplos relacionados a componentes consistem em um par de cliente e servidor, com o servidor que requer o uso do utilitário de amostra de registro.</span><span class="sxs-lookup"><span data-stu-id="4299c-106">The component-related samples consist of a client and server pair, with the server requiring the use of the REGISTER sample utility.</span></span> <span data-ttu-id="4299c-107">Aqui está um resumo dos agrupamentos de exemplo e como extrair cada grupo como uma unidade compilável.</span><span class="sxs-lookup"><span data-stu-id="4299c-107">Here is a summary of the sample groupings and how to extract each group as a buildable unit.</span></span> <span data-ttu-id="4299c-108">Para cada Agrupamento de exemplo, copie o conteúdo dos diretórios mostrados.</span><span class="sxs-lookup"><span data-stu-id="4299c-108">For each sample grouping, copy the content of the directories shown.</span></span> <span data-ttu-id="4299c-109">O diretório pai de \[ destino \] mostrado não requer nenhum conteúdo da ramificação de exemplos.</span><span class="sxs-lookup"><span data-stu-id="4299c-109">The parent \[destination\] directory shown requires no content from the samples branch.</span></span> <span data-ttu-id="4299c-110">No entanto, os menus de ajuda nos exemplos em execução pressupõem que o tutorial apropriado. Arquivos de ajuda HTM estão localizados neste diretório pai de \[ destino \] .</span><span class="sxs-lookup"><span data-stu-id="4299c-110">However, the help menus in the running samples do assume that the appropriate tutorial .HTM help files are located in this parent \[destination\] directory.</span></span>

<span data-ttu-id="4299c-111">Para o aplicativo Win32 READTUT:</span><span class="sxs-lookup"><span data-stu-id="4299c-111">For the Win32 READTUT application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

<span data-ttu-id="4299c-112">Para o aplicativo de esqueleto do Win32 EXE:</span><span class="sxs-lookup"><span data-stu-id="4299c-112">For the Win32 EXE skeleton application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

<span data-ttu-id="4299c-113">Para o esqueleto da DLL do Win32:</span><span class="sxs-lookup"><span data-stu-id="4299c-113">For the Win32 DLL skeleton:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

<span data-ttu-id="4299c-114">Para os exemplos de objeto COM básico:</span><span class="sxs-lookup"><span data-stu-id="4299c-114">For the basic COM object samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

<span data-ttu-id="4299c-115">Para obter os exemplos de cliente/servidor de componente de DLL em processo básico:</span><span class="sxs-lookup"><span data-stu-id="4299c-115">For the basic in-process DLL component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

<span data-ttu-id="4299c-116">Para os exemplos de cliente/servidor de componente licenciado:</span><span class="sxs-lookup"><span data-stu-id="4299c-116">For the licensed component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

<span data-ttu-id="4299c-117">Para os exemplos de marshaling padrão:</span><span class="sxs-lookup"><span data-stu-id="4299c-117">For the standard marshaling samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

<span data-ttu-id="4299c-118">Para os exemplos de cliente/servidor local fora do processo:</span><span class="sxs-lookup"><span data-stu-id="4299c-118">For the out-of-process local client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

<span data-ttu-id="4299c-119">Para os exemplos de cliente de modelo de apartamento/servidor:</span><span class="sxs-lookup"><span data-stu-id="4299c-119">For the apartment model client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

<span data-ttu-id="4299c-120">Para os exemplos de cliente/servidor DCOM (COM distribuído):</span><span class="sxs-lookup"><span data-stu-id="4299c-120">For the DCOM (Distributed COM) client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

<span data-ttu-id="4299c-121">Para os exemplos de cliente/servidor de Threading livre:</span><span class="sxs-lookup"><span data-stu-id="4299c-121">For the free threading client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

<span data-ttu-id="4299c-122">Para os exemplos de cliente/servidor do objeto COM Connect:</span><span class="sxs-lookup"><span data-stu-id="4299c-122">For the connectable COM object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

<span data-ttu-id="4299c-123">Para os exemplos de cliente/servidor de armazenamento estruturado:</span><span class="sxs-lookup"><span data-stu-id="4299c-123">For the structured storage client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

<span data-ttu-id="4299c-124">Para o objeto persistente, exemplos de cliente/servidor:</span><span class="sxs-lookup"><span data-stu-id="4299c-124">For the persistent object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

<span data-ttu-id="4299c-125">Para os exemplos de cliente/servidor de segurança DCOM:</span><span class="sxs-lookup"><span data-stu-id="4299c-125">For the DCOM security client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




