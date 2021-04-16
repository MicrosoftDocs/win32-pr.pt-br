---
description: Mergemod.dll fornece um objeto COM que implementa operações de mesclagem e geração de imagem de origem para módulos de mesclagem. O objeto principal implementa interfaces para programas C/C++ e clientes de automação, incluindo Visual Basic e VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Mesclar automação de módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747540"
---
# <a name="merge-module-automation"></a><span data-ttu-id="c4567-104">Mesclar automação de módulo</span><span class="sxs-lookup"><span data-stu-id="c4567-104">Merge Module Automation</span></span>

<span data-ttu-id="c4567-105">Mergemod.dll fornece um objeto COM que implementa operações de mesclagem e geração de imagem de origem para módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="c4567-105">Mergemod.dll provides a COM object that implements merge operations and source image generation for merge modules.</span></span> <span data-ttu-id="c4567-106">O objeto principal implementa interfaces para programas C/C++ e clientes de automação, incluindo Visual Basic e VBScript.</span><span class="sxs-lookup"><span data-stu-id="c4567-106">The main object implements interfaces for C/C++ programs and automation clients, including Visual Basic and VBScript.</span></span>

<span data-ttu-id="c4567-107">O método preferencial para instalar o Mergemod.dll é usando o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c4567-107">The preferred method for installing Mergemod.dll is by using the Windows Installer.</span></span> <span data-ttu-id="c4567-108">A ID do componente do componente que contém a interface COM do Mergemod.dll é {FD153241-37EC-11D2-8892-00A0C981B015}.</span><span class="sxs-lookup"><span data-stu-id="c4567-108">The Component ID for the component containing the Mergemod.dll COM interface is {FD153241-37EC-11D2-8892-00A0C981B015}.</span></span> <span data-ttu-id="c4567-109">O mesmo binário pode ser usado em todos os sistemas Windows e a dll se registrará automaticamente por meio do regsvr32 em sistemas mais antigos.</span><span class="sxs-lookup"><span data-stu-id="c4567-109">The same binary can be used on all Windows systems and the dll will self-register through regsvr32 on older systems.</span></span>

<span data-ttu-id="c4567-110">Observe que Mergemod.dll requer que o Msvcrt.dll seja instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="c4567-110">Note that Mergemod.dll requires that the Msvcrt.dll be installed on the system.</span></span>

<span data-ttu-id="c4567-111">Observe que Mergemod.dll 2,0 é necessário para criar [módulos de mesclagem configuráveis](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="c4567-111">Note that Mergemod.dll 2.0 is required to create [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="c4567-112">Mergemod.dll versão 2,0 fornece funcionalidade estendida no momento da compilação por meio da interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="c4567-112">Mergemod.dll version 2.0 provides extended functionality at build time through the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Interface.</span></span> <span data-ttu-id="c4567-113">Esse CLSID dá suporte a todas as funcionalidades existentes da interface [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) fornecida pelo Mergemod.dll versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="c4567-113">This CLSID supports all the existing functionality of the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) Interface provided by Mergemod.dll version 1.0.</span></span> <span data-ttu-id="c4567-114">A interface padrão no objeto de [**mesclagem**](merge-object.md) do Mergemod.dll 2,0 é a interface **IMsmMerge2** em vez da interface **IMsmMerge** .</span><span class="sxs-lookup"><span data-stu-id="c4567-114">The default interface on the [**Merge**](merge-object.md) object of Mergemod.dll 2.0 is the **IMsmMerge2** interface instead of the **IMsmMerge** interface.</span></span>

[<span data-ttu-id="c4567-115">Modelo de objeto para Mergemod.dll versão 1,0</span><span class="sxs-lookup"><span data-stu-id="c4567-115">Object Model for Mergemod.dll Version 1.0</span></span>](object-model-for-mergemod-dll-version-1-0.md)

[<span data-ttu-id="c4567-116">Modelo de objeto para Mergemod.dll versão 2,0</span><span class="sxs-lookup"><span data-stu-id="c4567-116">Object Model for Mergemod.dll Version 2.0</span></span>](object-model-for-mergemod-dll-version-2-0.md)

 

 
