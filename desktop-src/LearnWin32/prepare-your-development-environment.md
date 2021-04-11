---
title: Preparar seu ambiente de desenvolvimento
description: Preparar seu ambiente de desenvolvimento
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293992"
---
# <a name="prepare-your-development-environment"></a><span data-ttu-id="bfe22-103">Preparar seu ambiente de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="bfe22-103">Prepare Your Development Environment</span></span>

<span data-ttu-id="bfe22-104">Para escrever um programa do Windows em C ou C++, você deve instalar o SDK (Software Development Kit) do Microsoft Windows ou o Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bfe22-104">To write a Windows program in C or C++, you must install the Microsoft Windows Software Development Kit (SDK) or Microsoft Visual Studio.</span></span> <span data-ttu-id="bfe22-105">O SDK do Windows contém os cabeçalhos e as bibliotecas necessárias para compilar e vincular seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfe22-105">The Windows SDK contains the headers and libraries necessary to compile and link your application.</span></span> <span data-ttu-id="bfe22-106">O SDK do Windows também contém ferramentas de linha de comando para criar aplicativos do Windows, incluindo o compilador Visual C++ e o vinculador.</span><span class="sxs-lookup"><span data-stu-id="bfe22-106">The Windows SDK also contains command-line tools for building Windows applications, including the Visual C++ compiler and linker.</span></span> <span data-ttu-id="bfe22-107">Embora seja possível compilar e criar programas do Windows com as ferramentas de linha de comando, é recomendável usar Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bfe22-107">Although you can compile and build Windows programs with the command-line tools, we recommend using Microsoft Visual Studio.</span></span> <span data-ttu-id="bfe22-108">Você pode baixar um download gratuito da Comunidade do Visual Studio ou avaliações gratuitas de outras versões do Visual Studio [aqui](https://visualstudio.microsoft.com/downloads/).</span><span class="sxs-lookup"><span data-stu-id="bfe22-108">You can download a free download of Visual Studio Community or free trials of other versions of Visual Studio [here](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="bfe22-109">Cada versão do SDK do Windows tem como alvo a versão mais recente do Windows, bem como várias versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="bfe22-109">Each release of the Windows SDK targets the latest version of Windows as well as several previous versions.</span></span> <span data-ttu-id="bfe22-110">As notas de versão listam as plataformas específicas com suporte, mas, a menos que você esteja mantendo um aplicativo para uma versão muito antiga do Windows, instale a versão mais recente do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="bfe22-110">The release notes list the specific platforms that are supported, but unless you are maintaining an application for a very old version of Windows, you should install the latest release of the Windows SDK.</span></span> <span data-ttu-id="bfe22-111">Você pode baixar as SDK do Windows mais recentes [aqui](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="bfe22-111">You can download the latest Windows SDK [here](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="bfe22-112">O SDK do Windows dá suporte ao desenvolvimento de aplicativos de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bfe22-112">The Windows SDK supports development of both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="bfe22-113">As APIs do Windows são projetadas para que o mesmo código possa Compilar para 32 bits ou 64 bits sem alterações.</span><span class="sxs-lookup"><span data-stu-id="bfe22-113">The Windows APIs are designed so that the same code can compile for 32-bit or 64-bit without changes.</span></span>

> [!Note]  
> <span data-ttu-id="bfe22-114">O SDK do Windows não dá suporte ao desenvolvimento de driver de hardware, e esta série não abordará o desenvolvimento de driver.</span><span class="sxs-lookup"><span data-stu-id="bfe22-114">The Windows SDK does not support hardware driver development, and this series will not discuss driver development.</span></span> <span data-ttu-id="bfe22-115">Para obter informações sobre como gravar um driver de hardware, consulte [introdução com drivers do Windows](/windows-hardware/drivers/gettingstarted/).</span><span class="sxs-lookup"><span data-stu-id="bfe22-115">For information about writing a hardware driver, see [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).</span></span>

## <a name="next"></a><span data-ttu-id="bfe22-116">Avançar</span><span class="sxs-lookup"><span data-stu-id="bfe22-116">Next</span></span>

[<span data-ttu-id="bfe22-117">Convenções de codificação do Windows</span><span class="sxs-lookup"><span data-stu-id="bfe22-117">Windows Coding Conventions</span></span>](windows-coding-conventions.md)

## <a name="related-topics"></a><span data-ttu-id="bfe22-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfe22-118">Related topics</span></span>

* [<span data-ttu-id="bfe22-119">Baixar o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bfe22-119">Download Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="bfe22-120">Baixar SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="bfe22-120">Download Windows SDK</span></span>](https://developer.microsoft.com/windows/downloads/windows-10-sdk)