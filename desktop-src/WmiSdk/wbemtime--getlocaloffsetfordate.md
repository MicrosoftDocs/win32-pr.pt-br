---
description: O método GetLocalOffsetForDate retorna o deslocamento em minutos (+ ou &\# 8211;) entre GMT e hora local para o tempo fornecido no argumento.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Métodos WBEMTime:: GetLocalOffsetForDate (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829260"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a><span data-ttu-id="f32cc-103">Métodos WBEMTime:: GetLocalOffsetForDate</span><span class="sxs-lookup"><span data-stu-id="f32cc-103">WBEMTime::GetLocalOffsetForDate methods</span></span>

<span data-ttu-id="f32cc-104">\[A classe [**WBEMTime**](wbemtime.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="f32cc-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="f32cc-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="f32cc-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="f32cc-106">O método **GetLocalOffsetForDate** retorna o deslocamento em minutos (+ ou) entre GMT e hora local para o tempo fornecido no argumento.</span><span class="sxs-lookup"><span data-stu-id="f32cc-106">The **GetLocalOffsetForDate** method returns the offset in minutes (+ or �) between GMT and local time for the time supplied in the argument.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f32cc-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="f32cc-107">Overload list</span></span>



| <span data-ttu-id="f32cc-108">Método</span><span class="sxs-lookup"><span data-stu-id="f32cc-108">Method</span></span>                                                                                           | <span data-ttu-id="f32cc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f32cc-109">Description</span></span>                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="f32cc-110">[**GetLocalOffsetForDate (tempo \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="f32cc-110">[**GetLocalOffsetForDate(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span></span>         | <span data-ttu-id="f32cc-111">O argumento é uma referência a uma **hora \_ t**.</span><span class="sxs-lookup"><span data-stu-id="f32cc-111">Argument is a reference to a **time\_t**.</span></span><br/>  |
| <span data-ttu-id="f32cc-112">[**GetLocalOffsetForDate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span><span class="sxs-lookup"><span data-stu-id="f32cc-112">[**GetLocalOffsetForDate(FILETIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span></span>     | <span data-ttu-id="f32cc-113">O argumento é um ponteiro para um **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="f32cc-113">Argument is a pointer to a **FILETIME**.</span></span><br/>   |
| [<span data-ttu-id="f32cc-114">**GetLocalOffsetForDate (struct tm \* )**</span><span class="sxs-lookup"><span data-stu-id="f32cc-114">**GetLocalOffsetForDate(struct tm\*)**</span></span>](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | <span data-ttu-id="f32cc-115">O argumento é uma estrutura de ponteiro para **TM** .</span><span class="sxs-lookup"><span data-stu-id="f32cc-115">Argument is a pointer to **tm** structure.</span></span><br/> |
| <span data-ttu-id="f32cc-116">[**GetLocalOffsetForDate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span><span class="sxs-lookup"><span data-stu-id="f32cc-116">[**GetLocalOffsetForDate(SYSTEMTIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span></span> | <span data-ttu-id="f32cc-117">O argumento é um ponteiro para um **SYSTEMTIME**.</span><span class="sxs-lookup"><span data-stu-id="f32cc-117">Argument is a pointer to a **SYSTEMTIME**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f32cc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f32cc-118">Requirements</span></span>



| <span data-ttu-id="f32cc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f32cc-119">Requirement</span></span> | <span data-ttu-id="f32cc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f32cc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32cc-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f32cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f32cc-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f32cc-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f32cc-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f32cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f32cc-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f32cc-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f32cc-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f32cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f32cc-126"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="f32cc-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="f32cc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f32cc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f32cc-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f32cc-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="f32cc-129">�</span><span class="sxs-lookup"><span data-stu-id="f32cc-129">�</span></span>

<span data-ttu-id="f32cc-130">�</span><span class="sxs-lookup"><span data-stu-id="f32cc-130">�</span></span>
