---
title: LIBMAIN. CPP
description: No componente do provedor de exemplo, um exemplo de código do ponto de entrada padrão da DLL para Adssmp.dll está em LibMain. cpp. As rotinas com suporte são listadas na tabela a seguir.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755901"
---
# <a name="libmaincpp"></a><span data-ttu-id="33ca0-104">LIBMAIN. CPP</span><span class="sxs-lookup"><span data-stu-id="33ca0-104">LIBMAIN.CPP</span></span>

<span data-ttu-id="33ca0-105">No componente do provedor de exemplo, um exemplo de código do ponto de entrada padrão da DLL para Adssmp.dll está em LibMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="33ca0-105">In the example provider component, a code example of the standard DLL entry point for Adssmp.dll is in Libmain.cpp.</span></span> <span data-ttu-id="33ca0-106">As rotinas com suporte são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="33ca0-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="33ca0-107">Item</span><span class="sxs-lookup"><span data-stu-id="33ca0-107">Item</span></span>                                  | <span data-ttu-id="33ca0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="33ca0-108">Description</span></span>                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="33ca0-109">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="33ca0-109">**DllGetClassObject**</span></span><br/>      | <span data-ttu-id="33ca0-110">Ponto de entrada de DLL padrão para localizar fábricas de classe.</span><span class="sxs-lookup"><span data-stu-id="33ca0-110">Standard DLL entry point for locating class factories.</span></span><br/>        |
| <span data-ttu-id="33ca0-111">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="33ca0-111">**DllCanUnloadNow**</span></span><br/>        | <span data-ttu-id="33ca0-112">Ponto de entrada de DLL padrão para determinar se a DLL pode ser descarregada.</span><span class="sxs-lookup"><span data-stu-id="33ca0-112">Standard DLL entry point to determine if DLL can be unloaded.</span></span><br/> |
| <span data-ttu-id="33ca0-113">**LibMain**</span><span class="sxs-lookup"><span data-stu-id="33ca0-113">**LibMain**</span></span><br/>                | <span data-ttu-id="33ca0-114">Ponto de entrada de inicialização de DLL padrão.</span><span class="sxs-lookup"><span data-stu-id="33ca0-114">Standard DLL initialization entry point.</span></span><br/>                      |
| <span data-ttu-id="33ca0-115">**IsCompatibleOleVersion**</span><span class="sxs-lookup"><span data-stu-id="33ca0-115">**IsCompatibleOleVersion**</span></span><br/> | <span data-ttu-id="33ca0-116">Verifique a compatibilidade com o tempo de execução do OLE.</span><span class="sxs-lookup"><span data-stu-id="33ca0-116">Verify compatibility with the OLE run time.</span></span><br/>                   |
| <span data-ttu-id="33ca0-117">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="33ca0-117">**DllMain**</span></span><br/>                | <span data-ttu-id="33ca0-118">Ponto de entrada para a maioria das versões do Windows 2000 ou do Windows NT.</span><span class="sxs-lookup"><span data-stu-id="33ca0-118">Entry point for most Windows 2000 or Windows NT versions.</span></span><br/>     |



 

 

 





