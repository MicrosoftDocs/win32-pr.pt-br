---
description: A preparação de recursos para um aplicativo MUI dá suporte aos modelos Win32 PE e não Win32 PE.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Preparando recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800048"
---
# <a name="preparing-resources"></a><span data-ttu-id="2eb50-103">Preparando recursos</span><span class="sxs-lookup"><span data-stu-id="2eb50-103">Preparing Resources</span></span>

<span data-ttu-id="2eb50-104">A preparação de recursos para um aplicativo MUI dá suporte aos modelos Win32 PE e não Win32 PE.</span><span class="sxs-lookup"><span data-stu-id="2eb50-104">Resource preparation for a MUI application supports both Win32 PE and non-Win32 PE models.</span></span> <span data-ttu-id="2eb50-105">Os recursos do Win32 PE são fornecidos em arquivos baseados em PE, como arquivos. dll,. exe ou. sys.</span><span class="sxs-lookup"><span data-stu-id="2eb50-105">Win32 PE resources are provided in PE-based files, such as .dll, .exe, or .sys files.</span></span> <span data-ttu-id="2eb50-106">Os recursos do PE não Win32 são fornecidos em um módulo personalizado de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="2eb50-106">Non-Win32 PE resources are furnished in a customized module of your choosing.</span></span>

> [!Note]  
> <span data-ttu-id="2eb50-107">É altamente recomendável que você use recursos do Win32 PE para aplicativos MUI do Win32, pois esses recursos têm suporte completo da tecnologia de recursos do MUI.</span><span class="sxs-lookup"><span data-stu-id="2eb50-107">It is highly recommended for you to use Win32 PE resources for Win32 MUI applications, as these resources are completely supported by the MUI resource technology.</span></span> <span data-ttu-id="2eb50-108">Arquivos de recurso PE não Win32 podem ser localizados chamando a função [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) conforme descrito em [localizando recursos não Win32 PE](locating-non-win32-pe-resources.md), mas o aplicativo deve fornecer sua própria funcionalidade para localizar e carregar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="2eb50-108">Non-Win32 PE resource files can be located by calling the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function as described in [Locating Non-Win32 PE Resources](locating-non-win32-pe-resources.md), but the application must provide its own functionality to find and load the required resources.</span></span>

 

<span data-ttu-id="2eb50-109">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="2eb50-109">This section contains the following topics:</span></span>

-   [<span data-ttu-id="2eb50-110">Criando o arquivo de recurso de idioma base</span><span class="sxs-lookup"><span data-stu-id="2eb50-110">Creating the Base Language Resource File</span></span>](creating-the-base-language-resource-file.md)
-   [<span data-ttu-id="2eb50-111">Usando o redirecionamento de cadeia de caracteres do registro</span><span class="sxs-lookup"><span data-stu-id="2eb50-111">Using Registry String Redirection</span></span>](using-registry-string-redirection.md)
-   [<span data-ttu-id="2eb50-112">Preparando um arquivo de configuração de recurso</span><span class="sxs-lookup"><span data-stu-id="2eb50-112">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)

 

 



