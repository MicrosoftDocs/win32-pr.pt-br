---
title: Movimentação de módulo
description: Um instantâneo que inclui a lista de módulos para um processo especificado contém informações sobre cada módulo, arquivo executável ou DLL (biblioteca de vínculo dinâmico), usado pelo processo especificado.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- bibliotecas de vínculo dinâmico
- bibliotecas de vínculo dinâmico, enumerando DLLs
- enumerando
- Enumerando, DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084600"
---
# <a name="module-walking"></a><span data-ttu-id="bb39d-107">Movimentação de módulo</span><span class="sxs-lookup"><span data-stu-id="bb39d-107">Module Walking</span></span>

<span data-ttu-id="bb39d-108">Um instantâneo que inclui a lista de módulos para um processo especificado contém informações sobre cada módulo, arquivo executável ou DLL (biblioteca de vínculo dinâmico), usado pelo processo especificado.</span><span class="sxs-lookup"><span data-stu-id="bb39d-108">A snapshot that includes the module list for a specified process contains information about each module, executable file, or dynamic-link library (DLL), used by the specified process.</span></span> <span data-ttu-id="bb39d-109">Você pode recuperar informações para o primeiro módulo na lista usando a função [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) .</span><span class="sxs-lookup"><span data-stu-id="bb39d-109">You can retrieve information for the first module in the list by using the [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) function.</span></span> <span data-ttu-id="bb39d-110">Depois de recuperar o primeiro módulo na lista, você pode recuperar informações para os módulos subsequentes na lista usando a função [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) .</span><span class="sxs-lookup"><span data-stu-id="bb39d-110">After retrieving the first module in the list, you can retrieve information for subsequent modules in the list by using the [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) function.</span></span> <span data-ttu-id="bb39d-111">**Module32First** e **Module32Next** preenchem uma estrutura [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) com informações sobre o módulo.</span><span class="sxs-lookup"><span data-stu-id="bb39d-111">**Module32First** and **Module32Next** fill a [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) structure with information about the module.</span></span>

<span data-ttu-id="bb39d-112">Você pode recuperar um código de status de erro estendido para [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) e [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) usando a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="bb39d-112">You can retrieve an extended error status code for [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) and [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="bb39d-113">O identificador de módulo, que é especificado no membro **th32ModuleID** de [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), só tem significado no Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bb39d-113">The module identifier, which is specified in the **th32ModuleID** member of [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), only has meaning in 16-bit Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bb39d-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb39d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb39d-115">Atravessando a lista de módulos</span><span class="sxs-lookup"><span data-stu-id="bb39d-115">Traversing the Module List</span></span>](traversing-the-module-list.md)
</dt> </dl>

 

 