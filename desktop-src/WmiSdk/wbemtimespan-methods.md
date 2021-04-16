---
description: A classe WBEMTimeSpan expõe os métodos a seguir.
ms.assetid: 7D450EE2-C52F-4B78-B6B1-9FD74394C3DE
ms.tgt_platform: multiple
title: Métodos WBEMTimeSpan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d516f22a7ecd5468d53bda44ce47edbe4504d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765358"
---
# <a name="wbemtimespan-methods"></a><span data-ttu-id="7d14d-103">Métodos WBEMTimeSpan</span><span class="sxs-lookup"><span data-stu-id="7d14d-103">WBEMTimeSpan Methods</span></span>

<span data-ttu-id="7d14d-104">\[A classe [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="7d14d-104">\[The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7d14d-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="7d14d-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7d14d-106">A classe [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d14d-106">The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7d14d-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7d14d-107">In this section</span></span>

-   <span data-ttu-id="7d14d-108">[**Construtores WbemTimeSpan**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="7d14d-108">[**WbemTimeSpan constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>
-   [<span data-ttu-id="7d14d-109">**Método Clear**</span><span class="sxs-lookup"><span data-stu-id="7d14d-109">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-clear)
-   [<span data-ttu-id="7d14d-110">**Método GetBSTR**</span><span class="sxs-lookup"><span data-stu-id="7d14d-110">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-getbstr)
-   [<span data-ttu-id="7d14d-111">**Método getTime**</span><span class="sxs-lookup"><span data-stu-id="7d14d-111">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-gettime)
-   [<span data-ttu-id="7d14d-112">**Método IsOk**</span><span class="sxs-lookup"><span data-stu-id="7d14d-112">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-isok)
-   <span data-ttu-id="7d14d-113">[**operador = método**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="7d14d-113">[**operator= method**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>
-   [<span data-ttu-id="7d14d-114">**operador + método**</span><span class="sxs-lookup"><span data-stu-id="7d14d-114">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="7d14d-115">**operador + = método**</span><span class="sxs-lookup"><span data-stu-id="7d14d-115">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   [<span data-ttu-id="7d14d-116">**operador-método**</span><span class="sxs-lookup"><span data-stu-id="7d14d-116">**operator- method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub)
-   [<span data-ttu-id="7d14d-117">**operador-= método**</span><span class="sxs-lookup"><span data-stu-id="7d14d-117">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="7d14d-118">**operador = = método**</span><span class="sxs-lookup"><span data-stu-id="7d14d-118">**operator == method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-equal-equal-to)
-   [<span data-ttu-id="7d14d-119">**operador! = método**</span><span class="sxs-lookup"><span data-stu-id="7d14d-119">**operator != method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-not-equal-to)
-   [<span data-ttu-id="7d14d-120">**método de > de operador**</span><span class="sxs-lookup"><span data-stu-id="7d14d-120">**operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="7d14d-121">**operador >= método**</span><span class="sxs-lookup"><span data-stu-id="7d14d-121">**operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="7d14d-122">**método de < de operador**</span><span class="sxs-lookup"><span data-stu-id="7d14d-122">**operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than)
-   [<span data-ttu-id="7d14d-123">**operador <= método**</span><span class="sxs-lookup"><span data-stu-id="7d14d-123">**operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than-equal-to)

 

 
