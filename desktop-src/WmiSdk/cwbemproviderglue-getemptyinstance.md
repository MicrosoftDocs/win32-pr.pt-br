---
description: O método GetEmptyInstance recupera uma única instância não populada da classe especificada.
audience: developer
ms.assetid: 2873b466-3782-4d63-a777-5b25e3fb7615
ms.tgt_platform: multiple
title: 'Métodos CWbemProviderGlue:: GetEmptyInstance (WbemGlue. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 853afbf3789969fbfca66d5f9cb40f41eadf7630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765258"
---
# <a name="cwbemprovidergluegetemptyinstance-methods"></a><span data-ttu-id="65bdb-103">Métodos CWbemProviderGlue:: GetEmptyInstance</span><span class="sxs-lookup"><span data-stu-id="65bdb-103">CWbemProviderGlue::GetEmptyInstance methods</span></span>

<span data-ttu-id="65bdb-104">\[A classe [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="65bdb-104">\[The [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="65bdb-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="65bdb-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="65bdb-106">O método **GetEmptyInstance** recupera uma única instância não populada da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="65bdb-106">The **GetEmptyInstance** method retrieves a single unpopulated instance of the specified class.</span></span>

### <a name="overload-list"></a><span data-ttu-id="65bdb-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="65bdb-107">Overload list</span></span>



| <span data-ttu-id="65bdb-108">Método</span><span class="sxs-lookup"><span data-stu-id="65bdb-108">Method</span></span>                                                                                                                                            | <span data-ttu-id="65bdb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="65bdb-109">Description</span></span>                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="65bdb-110">[**GetEmptyInstance (LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="65bdb-110">[**GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>                            | <span data-ttu-id="65bdb-111">Recupera uma única instância não preenchida da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="65bdb-111">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |
| <span data-ttu-id="65bdb-112">[**GetEmptyInstance (MethodContext, LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="65bdb-112">[**GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span> | <span data-ttu-id="65bdb-113">Recupera uma única instância não preenchida da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="65bdb-113">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="65bdb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65bdb-114">Requirements</span></span>



| <span data-ttu-id="65bdb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="65bdb-115">Requirement</span></span> | <span data-ttu-id="65bdb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="65bdb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65bdb-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65bdb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65bdb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65bdb-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="65bdb-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65bdb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65bdb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65bdb-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="65bdb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65bdb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="65bdb-122"><dt>WbemGlue. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65bdb-122"><dt>WbemGlue.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="65bdb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65bdb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="65bdb-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65bdb-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="65bdb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="65bdb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65bdb-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65bdb-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="65bdb-127">�</span><span class="sxs-lookup"><span data-stu-id="65bdb-127">�</span></span>

<span data-ttu-id="65bdb-128">�</span><span class="sxs-lookup"><span data-stu-id="65bdb-128">�</span></span>
