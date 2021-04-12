---
description: 'O método CInstance:: GetWBEMINT64 recupera uma propriedade de inteiro de 64 bits.'
ms.assetid: b51d0c51-3b72-4358-8fc3-d1dbc298b4d9
ms.tgt_platform: multiple
title: 'Métodos CInstance:: GetWBEMINT64 (instance. h)'
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
ms.openlocfilehash: 3d7b7a9f4091125bd722aea197c1670defb0c21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297004"
---
# <a name="cinstancegetwbemint64-methods"></a><span data-ttu-id="0e26e-103">Métodos CInstance:: GetWBEMINT64</span><span class="sxs-lookup"><span data-stu-id="0e26e-103">CInstance::GetWBEMINT64 methods</span></span>

<span data-ttu-id="0e26e-104">\[A classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="0e26e-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0e26e-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="0e26e-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0e26e-106">O método **CInstance:: GetWBEMINT64** recupera uma propriedade de inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0e26e-106">The **CInstance::GetWBEMINT64** method retrieves a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0e26e-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="0e26e-107">Overload list</span></span>



| <span data-ttu-id="0e26e-108">Método</span><span class="sxs-lookup"><span data-stu-id="0e26e-108">Method</span></span>                                                                                   | <span data-ttu-id="0e26e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e26e-109">Description</span></span>                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------|
| <span data-ttu-id="0e26e-110">[**GetWBEMINT64 (LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span><span class="sxs-lookup"><span data-stu-id="0e26e-110">[**GetWBEMINT64(LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span></span>   | <span data-ttu-id="0e26e-111">Recupera uma propriedade de inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0e26e-111">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="0e26e-112">[**GetWBEMINT64 (LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="0e26e-112">[**GetWBEMINT64(LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="0e26e-113">Recupera uma propriedade de inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0e26e-113">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="0e26e-114">[**GetWBEMINT64 (LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="0e26e-114">[**GetWBEMINT64(LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="0e26e-115">Recupera uma propriedade de inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0e26e-115">Retrieves a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0e26e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e26e-116">Requirements</span></span>



| <span data-ttu-id="0e26e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e26e-117">Requirement</span></span> | <span data-ttu-id="0e26e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0e26e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e26e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e26e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0e26e-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e26e-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="0e26e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e26e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0e26e-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e26e-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="0e26e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e26e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e26e-124"><dt>Instance. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e26e-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0e26e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e26e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e26e-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e26e-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="0e26e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0e26e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e26e-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e26e-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e26e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e26e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e26e-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="0e26e-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

