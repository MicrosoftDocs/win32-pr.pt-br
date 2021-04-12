---
description: O construtor da classe WBEMTimeSpan cria um objeto de período de tempo. O Construtor está sobrecarregado.
audience: developer
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.tgt_platform: multiple
title: 'Construtores WBEMTimeSpan:: WbemTimeSpan (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: af5724a91ab50b5286e23b3c8095163e415d95e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171965"
---
# <a name="wbemtimespanwbemtimespan-constructors"></a><span data-ttu-id="3352e-104">Construtores WBEMTimeSpan:: WbemTimeSpan</span><span class="sxs-lookup"><span data-stu-id="3352e-104">WBEMTimeSpan::WbemTimeSpan constructors</span></span>

<span data-ttu-id="3352e-105">\[A classe [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="3352e-105">\[The [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="3352e-106">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="3352e-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="3352e-107">O construtor da classe **WBEMTimeSpan** cria um objeto de período de tempo.</span><span class="sxs-lookup"><span data-stu-id="3352e-107">The **WBEMTimeSpan** class constructor creates a time span object.</span></span> <span data-ttu-id="3352e-108">O Construtor está sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="3352e-108">The constructor is overloaded.</span></span>

### <a name="overload-list"></a><span data-ttu-id="3352e-109">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="3352e-109">Overload list</span></span>



| <span data-ttu-id="3352e-110">Construtor</span><span class="sxs-lookup"><span data-stu-id="3352e-110">Constructor</span></span>                                                                                                 | <span data-ttu-id="3352e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3352e-111">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="3352e-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="3352e-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                                      | <span data-ttu-id="3352e-113">Cria um objeto de intervalo de tempo não inicializado.</span><span class="sxs-lookup"><span data-stu-id="3352e-113">Creates an uninitialized time span object.</span></span><br/>                        |
| <span data-ttu-id="3352e-114">[**WBEMTimeSpan (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="3352e-114">[**WBEMTimeSpan(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                               | <span data-ttu-id="3352e-115">Inicializa o novo objeto de intervalo de tempo para o valor no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3352e-115">Initializes the new time span object to value in the parameter.</span></span><br/>   |
| <span data-ttu-id="3352e-116">[**WBEMTimeSpan (int, int, int, int, int, int, int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span><span class="sxs-lookup"><span data-stu-id="3352e-116">[**WBEMTimeSpan(int,int,int,int,int,int,int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span></span> | <span data-ttu-id="3352e-117">Inicializa o novo objeto de intervalo de tempo para valores nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3352e-117">Initializes the new time span object to values in the parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3352e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3352e-118">Requirements</span></span>



| <span data-ttu-id="3352e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3352e-119">Requirement</span></span> | <span data-ttu-id="3352e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3352e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3352e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3352e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3352e-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3352e-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="3352e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3352e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3352e-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3352e-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="3352e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3352e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3352e-126"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="3352e-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="3352e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3352e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3352e-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3352e-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="3352e-129">�</span><span class="sxs-lookup"><span data-stu-id="3352e-129">�</span></span>

<span data-ttu-id="3352e-130">�</span><span class="sxs-lookup"><span data-stu-id="3352e-130">�</span></span>
