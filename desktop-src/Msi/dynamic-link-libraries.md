---
description: Uma ação personalizada pode chamar uma função definida em uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Bibliotecas de Dynamic-Link (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011151"
---
# <a name="dynamic-link-libraries-windows-installer"></a><span data-ttu-id="491a6-103">Bibliotecas de Dynamic-Link (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="491a6-103">Dynamic-Link Libraries (Windows Installer)</span></span>

<span data-ttu-id="491a6-104">Uma ação personalizada pode chamar uma função definida em uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++.</span><span class="sxs-lookup"><span data-stu-id="491a6-104">A custom action can call a function defined in a dynamic-link library (DLL) written in C or C++.</span></span> <span data-ttu-id="491a6-105">A DLL pode existir como um arquivo instalado durante a instalação atual ou como um fluxo binário temporário proveniente da [tabela binária](binary-table.md) do banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="491a6-105">The DLL can exist as a file installed during the current installation or as a temporary binary stream originating from the [Binary table](binary-table.md) of the installation database.</span></span>

<span data-ttu-id="491a6-106">Observe que todas as funções chamadas, incluindo ações personalizadas em DLLs, devem especificar a \_ \_ Convenção de chamada stdcall.</span><span class="sxs-lookup"><span data-stu-id="491a6-106">Note that any called functions, including custom actions in DLLs, must specify the \_\_stdcall calling convention.</span></span> <span data-ttu-id="491a6-107">Por exemplo, para chamar CustomAction, use o seguinte.</span><span class="sxs-lookup"><span data-stu-id="491a6-107">For example, to call CustomAction use the following.</span></span>


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="491a6-108">Para obter mais informações, consulte [acessando a sessão do instalador atual de dentro de uma ação personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span><span class="sxs-lookup"><span data-stu-id="491a6-108">For more information see, [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span></span>

<span data-ttu-id="491a6-109">Os seguintes tipos de ações personalizadas chamam uma biblioteca de vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="491a6-109">The following types of custom actions call a dynamic-link library.</span></span>



| <span data-ttu-id="491a6-110">Tipo de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="491a6-110">Custom action type</span></span>                                 | <span data-ttu-id="491a6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="491a6-111">Description</span></span>                               |
|----------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="491a6-112">Tipo de ação personalizada 1</span><span class="sxs-lookup"><span data-stu-id="491a6-112">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="491a6-113">Arquivo DLL armazenado em um fluxo de tabela binária.</span><span class="sxs-lookup"><span data-stu-id="491a6-113">DLL file stored in a Binary table stream.</span></span> |
| [<span data-ttu-id="491a6-114">Tipo de ação personalizada 17</span><span class="sxs-lookup"><span data-stu-id="491a6-114">Custom Action Type 17</span></span>](custom-action-type-17.md) | <span data-ttu-id="491a6-115">Arquivo DLL instalado com um produto.</span><span class="sxs-lookup"><span data-stu-id="491a6-115">DLL file installed with a product.</span></span>        |



 

> [!Note]  
> <span data-ttu-id="491a6-116">Para usar COM, você precisa chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) na ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="491a6-116">To use COM you need to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in the custom action.</span></span> <span data-ttu-id="491a6-117">Não encerre se você achar que o thread já foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="491a6-117">Do not quit if you find that the thread has already been initialized.</span></span> <span data-ttu-id="491a6-118">Por exemplo, o thread é inicializado em uma instalação por máquina, mas não em uma instalação por usuário.</span><span class="sxs-lookup"><span data-stu-id="491a6-118">For example, the thread is initialized in a per-machine installation but not in a per-user installation.</span></span>

 

<span data-ttu-id="491a6-119">Confira a [lista resumida de todos os tipos de ação personalizada](summary-list-of-all-custom-action-types.md) para obter um resumo de todos os tipos de ações personalizadas e como eles são codificados na [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="491a6-119">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction table](customaction-table.md).</span></span>

 

 
