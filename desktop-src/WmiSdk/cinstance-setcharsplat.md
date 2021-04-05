---
description: 'O método CInstance:: SetCharSplat define uma propriedade de cadeia de caracteres.'
ms.assetid: 7f59a2ea-3513-4a14-ac1a-62ed833d7192
ms.tgt_platform: multiple
title: 'Métodos CInstance:: SetCharSplat (instance. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: e60f24023a9fc704f331d1d071e673720bfdc43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922205"
---
# <a name="cinstancesetcharsplat-methods"></a><span data-ttu-id="f5190-103">Métodos CInstance:: SetCharSplat</span><span class="sxs-lookup"><span data-stu-id="f5190-103">CInstance::SetCharSplat methods</span></span>

<span data-ttu-id="f5190-104">\[A classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="f5190-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="f5190-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="f5190-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="f5190-106">O método **CInstance:: SetCharSplat** define uma propriedade de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5190-106">The **CInstance::SetCharSplat** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f5190-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="f5190-107">Overload list</span></span>



| <span data-ttu-id="f5190-108">Método</span><span class="sxs-lookup"><span data-stu-id="f5190-108">Method</span></span>                                                                             | <span data-ttu-id="f5190-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5190-109">Description</span></span>                        |
|:-----------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="f5190-110">[**SetCharSplat (LPCWSTR, DWORD)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_dword))</span><span class="sxs-lookup"><span data-stu-id="f5190-110">[**SetCharSplat(LPCWSTR, DWORD)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_dword))</span></span>     | <span data-ttu-id="f5190-111">Define uma propriedade de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5190-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="f5190-112">[**SetCharSplat(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="f5190-112">[**SetCharSplat(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcstr))</span></span>   | <span data-ttu-id="f5190-113">Define uma propriedade de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5190-113">Sets a string property.</span></span><br/> |
| <span data-ttu-id="f5190-114">[**SetCharSplat(LPCWSTR, LPCWSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="f5190-114">[**SetCharSplat(LPCWSTR, LPCWSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcwstr))</span></span> | <span data-ttu-id="f5190-115">Define uma propriedade de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5190-115">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f5190-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5190-116">Requirements</span></span>



| <span data-ttu-id="f5190-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5190-117">Requirement</span></span> | <span data-ttu-id="f5190-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f5190-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5190-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5190-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5190-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5190-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f5190-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5190-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5190-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5190-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f5190-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5190-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5190-124"><dt>Instance. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5190-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f5190-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5190-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5190-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5190-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="f5190-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f5190-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5190-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5190-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5190-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5190-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5190-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="f5190-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

