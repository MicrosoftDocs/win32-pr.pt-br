---
description: 'O operador de subtração de classe WBEMTime (&\# 8211;) foi sobrecarregado para:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Operadores WBEMTime:: Operator (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771276"
---
# <a name="wbemtimeoperator--operators"></a><span data-ttu-id="24b91-103">Operadores WBEMTime:: Operator</span><span class="sxs-lookup"><span data-stu-id="24b91-103">WBEMTime::operator- operators</span></span>

<span data-ttu-id="24b91-104">\[A classe [**WBEMTime**](wbemtime.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="24b91-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="24b91-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="24b91-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="24b91-106">O operador de subtração da classe [**WBEMTime**](wbemtime.md) () foi sobrecarregado para:</span><span class="sxs-lookup"><span data-stu-id="24b91-106">The [**WBEMTime**](wbemtime.md) class subtraction operator (�) has been overloaded to:</span></span>

-   <span data-ttu-id="24b91-107">Subtraia um período de tempo do tempo de um objeto para produzir um novo objeto de hora que contenha o tempo resultante.</span><span class="sxs-lookup"><span data-stu-id="24b91-107">Subtract a time span from an object's time to produce a new time object that contains the resulting time.</span></span>
-   <span data-ttu-id="24b91-108">Subtraia uma hora do tempo do objeto para produzir um novo objeto de intervalo de tempo que contenha a diferença entre as duas horas.</span><span class="sxs-lookup"><span data-stu-id="24b91-108">Subtract a time from the object's time to produce a new time span object that contains the difference between the two times.</span></span>

### <a name="overload-list"></a><span data-ttu-id="24b91-109">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="24b91-109">Overload list</span></span>



| <span data-ttu-id="24b91-110">Operador</span><span class="sxs-lookup"><span data-stu-id="24b91-110">Operator</span></span>                                                                         | <span data-ttu-id="24b91-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="24b91-111">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="24b91-112">**Operator-(WBEMTime&)**</span><span class="sxs-lookup"><span data-stu-id="24b91-112">**operator-(WBEMTime&)**</span></span>](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | <span data-ttu-id="24b91-113">Subtrai um **WBEMTime** de um **WBEMTime**.</span><span class="sxs-lookup"><span data-stu-id="24b91-113">Subtracts a **WBEMTime** from a **WBEMTime**.</span></span><br/>                         |
| <span data-ttu-id="24b91-114">[**Operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span><span class="sxs-lookup"><span data-stu-id="24b91-114">[**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span></span> | <span data-ttu-id="24b91-115">Subtrai um [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) de um **WBEMTime**.</span><span class="sxs-lookup"><span data-stu-id="24b91-115">Subtracts a [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) from a **WBEMTime**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="24b91-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24b91-116">Requirements</span></span>



| <span data-ttu-id="24b91-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b91-117">Requirement</span></span> | <span data-ttu-id="24b91-118">Valor</span><span class="sxs-lookup"><span data-stu-id="24b91-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b91-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24b91-119">Minimum supported client</span></span><br/> | <span data-ttu-id="24b91-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24b91-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="24b91-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24b91-121">Minimum supported server</span></span><br/> | <span data-ttu-id="24b91-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24b91-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="24b91-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24b91-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b91-124"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="24b91-124"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="24b91-125">DLL</span><span class="sxs-lookup"><span data-stu-id="24b91-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24b91-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24b91-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="24b91-127">�</span><span class="sxs-lookup"><span data-stu-id="24b91-127">�</span></span>

<span data-ttu-id="24b91-128">�</span><span class="sxs-lookup"><span data-stu-id="24b91-128">�</span></span>
