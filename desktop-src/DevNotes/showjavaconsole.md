---
description: A função ShowJavaConsole é um recurso de depuração para desenvolvedores de Java. Os applets (ou outro código Java) em execução no Internet Explorer podem usá-lo para exibir mensagens de erro e outras informações.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: Função ShowJavaConsole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752189"
---
# <a name="showjavaconsole-function"></a><span data-ttu-id="e4351-104">Função ShowJavaConsole</span><span class="sxs-lookup"><span data-stu-id="e4351-104">ShowJavaConsole function</span></span>

<span data-ttu-id="e4351-105">A função **ShowJavaConsole** é um recurso de depuração para desenvolvedores de Java.</span><span class="sxs-lookup"><span data-stu-id="e4351-105">The **ShowJavaConsole** function is a debugging aid for Java developers.</span></span> <span data-ttu-id="e4351-106">Os applets (ou outro código Java) em execução no Internet Explorer podem usá-lo para exibir mensagens de erro e outras informações.</span><span class="sxs-lookup"><span data-stu-id="e4351-106">Applets (or other Java code) running within Internet Explorer can use it to display error messages and other information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4351-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4351-107">Syntax</span></span>


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a><span data-ttu-id="e4351-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4351-108">Parameters</span></span>

<span data-ttu-id="e4351-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e4351-109">This function has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="e4351-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4351-110">Return value</span></span>

<span data-ttu-id="e4351-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e4351-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4351-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4351-112">Remarks</span></span>

<span data-ttu-id="e4351-113">Chamar **ShowJavaConsole** faz com que a VM (máquina virtual) do Java exiba a janela do console do Java.</span><span class="sxs-lookup"><span data-stu-id="e4351-113">Calling **ShowJavaConsole** causes the Java virtual machine (VM) to display the Java console window.</span></span> <span data-ttu-id="e4351-114">A própria janela do console do Java pode exibir a saída de depuração do código Java em execução no processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4351-114">The Java console window itself can display debugging output from Java code running in the calling process.</span></span> <span data-ttu-id="e4351-115">Normalmente, isso seria usado somente por um aplicativo que hospeda a VM Java.</span><span class="sxs-lookup"><span data-stu-id="e4351-115">Typically, this would be used only by an application hosting the Java VM.</span></span> <span data-ttu-id="e4351-116">Há apenas uma única janela de console Java por processo; várias chamadas para a API resultam na mesma janela exibida.</span><span class="sxs-lookup"><span data-stu-id="e4351-116">There is only a single Java console window per process; multiple calls to the API result in the same window being displayed.</span></span> <span data-ttu-id="e4351-117">Em outras palavras, se a janela do console já estiver sendo exibida, nada acontecerá; se a janela não tiver sido exibida ou o usuário a tiver fechado, a janela será exibida.</span><span class="sxs-lookup"><span data-stu-id="e4351-117">In other words, if the console window is already displayed, nothing happens; if the window has not been displayed, or the user has closed it, then the window pops up.</span></span>

<span data-ttu-id="e4351-118">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e4351-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4351-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4351-119">Requirements</span></span>



| <span data-ttu-id="e4351-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4351-120">Requirement</span></span> | <span data-ttu-id="e4351-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e4351-121">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4351-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e4351-122">DLL</span></span><br/> | <dl> <span data-ttu-id="e4351-123"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4351-123"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
