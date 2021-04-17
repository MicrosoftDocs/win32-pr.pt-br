---
description: Ao criar um arquivo INF para um aplicativo de instalação, você também deve consultar o formato de arquivo INF documentado em diretrizes gerais para arquivos INF e seções de arquivo INF e diretivas do Microsoft Windows 2000 Driver Development Kit.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Criando um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754109"
---
# <a name="authoring-an-inf-file"></a><span data-ttu-id="e2e2b-103">Criando um arquivo INF</span><span class="sxs-lookup"><span data-stu-id="e2e2b-103">Authoring an INF file</span></span>

<span data-ttu-id="e2e2b-104">Ao criar um arquivo INF para um aplicativo de instalação, você também deve consultar o formato de arquivo INF documentado em *diretrizes gerais para arquivos INF* e *seções de arquivo inf e diretivas* do Microsoft Windows 2000 Driver Development Kit.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-104">When authoring an INF file for a Setup application you should also refer to the INF file format documented in *General Guidelines for INF Files* and *INF File Sections and Directives* of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="e2e2b-105">Ao criar arquivos INF para um aplicativo de instalação, siga as regras a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-105">When authoring INF files for a setup application adhere to the following rules.</span></span>

-   <span data-ttu-id="e2e2b-106">Uma seção de **versão** é necessária em todos os arquivos INF.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-106">A **Version** section is required in every INF file.</span></span>
-   <span data-ttu-id="e2e2b-107">As seções devem começar com o nome da seção entre colchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="e2e2b-107">Sections must begin with the section name enclosed by square brackets (\[\]).</span></span>
-   <span data-ttu-id="e2e2b-108">Os nomes das seções **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **cadeias de caracteres** e **versão** devem ser idênticos ao tipo de seção.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-108">Names of **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings**, and **Version** sections must be identical to the section type.</span></span> <span data-ttu-id="e2e2b-109">Por exemplo, use \[ DestinationDirs \] .</span><span class="sxs-lookup"><span data-stu-id="e2e2b-109">For example use \[DestinationDirs\].</span></span> <span data-ttu-id="e2e2b-110">Os autores podem especificar os nomes de outros tipos de seções.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-110">Authors may specify the names of other types of sections.</span></span>
-   <span data-ttu-id="e2e2b-111">Os nomes das seções **SourceDisksNames** e **SourceDisksFiles** podem ser anexados a um sufixo específico da plataforma.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-111">Names of **SourceDisksNames** and **SourceDisksFiles** sections may be appended with a platform-specific suffix.</span></span> <span data-ttu-id="e2e2b-112">Por exemplo, para mostrar uma seção **SourceDisksNames** específica da Intel, use \[ SourceDisksNames. x86 \] .</span><span class="sxs-lookup"><span data-stu-id="e2e2b-112">For example, to show an Intel-specific **SourceDisksNames** section use \[SourceDisksNames.x86\].</span></span> <span data-ttu-id="e2e2b-113">Se as funções de instalação localizarem seções **SourceDisksNames** e **SourceDisksFiles** específicas da plataforma correspondentes à plataforma do usuário, as funções usarão as seções específicas da plataforma.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-113">If the setup functions find platform-specific **SourceDisksNames** and **SourceDisksFiles** sections matching the user's platform, the functions use the platform-specific sections.</span></span> <span data-ttu-id="e2e2b-114">Caso contrário, as funções de instalação usarão as seções **SourceDisksNames** e **SourceDisksFiles** sem sufixo.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-114">Otherwise the setup functions use the non-suffixed **SourceDisksNames** and **SourceDisksFiles** sections.</span></span> <span data-ttu-id="e2e2b-115">As funções de instalação podem determinar programaticamente o sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-115">The setup functions can programmatically determine the user's system.</span></span> <span data-ttu-id="e2e2b-116">Consulte o [exemplo de seções inf SourceDisksNames e SourceDisksFiles](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span><span class="sxs-lookup"><span data-stu-id="e2e2b-116">See the [INF SourceDisksNames and SourceDisksFiles Sections Example](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span></span>
-   <span data-ttu-id="e2e2b-117">Os valores podem ser expressos como cadeias de caracteres substituíveis usando o formato%*strKey*%.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-117">Values may be expressed as replaceable strings using the form %*strkey*%.</span></span> <span data-ttu-id="e2e2b-118">Para usar um caractere% na cadeia de caracteres, use%%.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-118">To use a % character in the string, use %%.</span></span> <span data-ttu-id="e2e2b-119">O strKey deve ser definido em uma seção de **cadeias de caracteres** do arquivo inf.</span><span class="sxs-lookup"><span data-stu-id="e2e2b-119">The strkey must be defined in a **Strings** section of the INF file.</span></span>

 

 



