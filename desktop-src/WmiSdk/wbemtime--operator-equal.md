---
description: Os operadores de atribuição de classe WBEMTime estão sobrecarregados para facilitar as conversões entre vários formatos de tempo de execução do Windows e ANSI C. As várias assinaturas sobrecarregadas são listadas abaixo.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Operadores WBEMTime:: Operator = (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297571"
---
# <a name="wbemtimeoperator-operators"></a><span data-ttu-id="8e374-104">Operadores WBEMTime:: Operator =</span><span class="sxs-lookup"><span data-stu-id="8e374-104">WBEMTime::operator= operators</span></span>

<span data-ttu-id="8e374-105">\[A classe [**WBEMTime**](wbemtime.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="8e374-105">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="8e374-106">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="8e374-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="8e374-107">Os operadores de atribuição de classe [**WBEMTime**](wbemtime.md) estão sobrecarregados para facilitar as conversões entre vários formatos de tempo de execução do Windows e ANSI C.</span><span class="sxs-lookup"><span data-stu-id="8e374-107">The [**WBEMTime**](wbemtime.md) class assignment operators are overloaded to facilitate conversions between various Windows and ANSI C run-time time formats.</span></span> <span data-ttu-id="8e374-108">As várias assinaturas sobrecarregadas são listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="8e374-108">The various overloaded signatures are listed below.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8e374-109">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="8e374-109">Overload list</span></span>



| <span data-ttu-id="8e374-110">Operador</span><span class="sxs-lookup"><span data-stu-id="8e374-110">Operator</span></span>                                                                     | <span data-ttu-id="8e374-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e374-111">Description</span></span>                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span data-ttu-id="8e374-112">[**operador = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span><span class="sxs-lookup"><span data-stu-id="8e374-112">[**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span></span>               | <span data-ttu-id="8e374-113">Converte um **BSTR** em formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="8e374-113">Converts a **BSTR** to **WBEMTime** format.</span></span><br/>         |
| <span data-ttu-id="8e374-114">[**Operator = (tempo \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="8e374-114">[**operator=(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span></span>        | <span data-ttu-id="8e374-115">Converte o **tempo \_ t** em formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="8e374-115">Converts **time\_t** to **WBEMTime** format.</span></span><br/>        |
| <span data-ttu-id="8e374-116">[**Operator = (& FILETIME)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="8e374-116">[**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>     | <span data-ttu-id="8e374-117">Converte **FILETIME** em formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="8e374-117">Converts **FILETIME** to **WBEMTime** format.</span></span><br/>       |
| <span data-ttu-id="8e374-118">[**Operator = (struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span><span class="sxs-lookup"><span data-stu-id="8e374-118">[**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span></span>   | <span data-ttu-id="8e374-119">Converte uma estrutura **TM** em formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="8e374-119">Converts a **tm** structure to **WBEMTime** format.</span></span><br/> |
| <span data-ttu-id="8e374-120">[**Operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="8e374-120">[**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span></span> | <span data-ttu-id="8e374-121">Converte **SYSTEMTIME** em formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="8e374-121">Converts **SYSTEMTIME** to **WBEMTime** format.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="8e374-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e374-122">Requirements</span></span>



| <span data-ttu-id="8e374-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e374-123">Requirement</span></span> | <span data-ttu-id="8e374-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8e374-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e374-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e374-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8e374-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e374-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="8e374-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e374-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8e374-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e374-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="8e374-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e374-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e374-130"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e374-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="8e374-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8e374-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e374-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e374-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="8e374-133">�</span><span class="sxs-lookup"><span data-stu-id="8e374-133">�</span></span>

<span data-ttu-id="8e374-134">�</span><span class="sxs-lookup"><span data-stu-id="8e374-134">�</span></span>
