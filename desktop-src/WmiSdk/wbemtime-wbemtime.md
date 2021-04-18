---
description: O construtor da classe WBEMTime facilita as conversões entre vários formatos de tempo de execução do Windows e ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Construtores WBEMTime:: WBEMTime (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791573"
---
# <a name="wbemtimewbemtime-constructors"></a><span data-ttu-id="70f19-103">Construtores WBEMTime:: WBEMTime</span><span class="sxs-lookup"><span data-stu-id="70f19-103">WBEMTime::WBEMTime constructors</span></span>

<span data-ttu-id="70f19-104">\[A classe [**WBEMTime**](wbemtime.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="70f19-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="70f19-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="70f19-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="70f19-106">O construtor da classe **WBEMTime** facilita as conversões entre vários formatos de tempo de execução do Windows e ANSI C.</span><span class="sxs-lookup"><span data-stu-id="70f19-106">The **WBEMTime** class constructor facilitates conversions between various Windows and ANSI C run-time time formats.</span></span>

### <a name="overload-list"></a><span data-ttu-id="70f19-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="70f19-107">Overload list</span></span>



| <span data-ttu-id="70f19-108">Construtor</span><span class="sxs-lookup"><span data-stu-id="70f19-108">Constructor</span></span>                                                                 | <span data-ttu-id="70f19-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="70f19-109">Description</span></span>                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span data-ttu-id="70f19-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="70f19-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                                   | <span data-ttu-id="70f19-111">Cria um objeto de tempo não inicializado.</span><span class="sxs-lookup"><span data-stu-id="70f19-111">Creates an uninitialized time object.</span></span><br/>                          |
| <span data-ttu-id="70f19-112">[**WBEMTime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="70f19-112">[**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                           | <span data-ttu-id="70f19-113">Inicializa o novo objeto de hora para o valor no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="70f19-113">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="70f19-114">[**WBEMTime (constante de tempo \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="70f19-114">[**WBEMTime(const time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span></span>        | <span data-ttu-id="70f19-115">Inicializa o novo objeto de hora para o valor no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="70f19-115">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="70f19-116">[**WBEMTime (const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span><span class="sxs-lookup"><span data-stu-id="70f19-116">[**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span></span>    | <span data-ttu-id="70f19-117">Inicializa o novo objeto de hora para o valor no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="70f19-117">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="70f19-118">[**WBEMTime (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="70f19-118">[**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span></span>     | <span data-ttu-id="70f19-119">Inicializa o novo objeto de hora para o valor no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="70f19-119">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="70f19-120">[**WBEMTime (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="70f19-120">[**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span></span> | <span data-ttu-id="70f19-121">Inicializa o novo objeto de hora para o valor no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="70f19-121">Initializes the new time object to the value in the parameter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="70f19-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70f19-122">Requirements</span></span>



| <span data-ttu-id="70f19-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="70f19-123">Requirement</span></span> | <span data-ttu-id="70f19-124">Valor</span><span class="sxs-lookup"><span data-stu-id="70f19-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f19-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70f19-125">Minimum supported client</span></span><br/> | <span data-ttu-id="70f19-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70f19-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="70f19-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70f19-127">Minimum supported server</span></span><br/> | <span data-ttu-id="70f19-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70f19-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="70f19-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70f19-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="70f19-130"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="70f19-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="70f19-131">DLL</span><span class="sxs-lookup"><span data-stu-id="70f19-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70f19-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70f19-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="70f19-133">�</span><span class="sxs-lookup"><span data-stu-id="70f19-133">�</span></span>

<span data-ttu-id="70f19-134">�</span><span class="sxs-lookup"><span data-stu-id="70f19-134">�</span></span>
