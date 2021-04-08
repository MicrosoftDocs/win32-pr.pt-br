---
description: 'O método CInstance:: GetWBEMINT64 define uma propriedade de inteiro de 64 bits.'
audience: developer
ms.assetid: a1789091-ddb6-44f7-bc02-82e7c0209bf9
ms.tgt_platform: multiple
title: 'Métodos CInstance:: SetWBEMINT64 (instance. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f83e39170125a07f28a25d594ad7203f44750a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922207"
---
# <a name="cinstancesetwbemint64-methods"></a><span data-ttu-id="0b534-103">Métodos CInstance:: SetWBEMINT64</span><span class="sxs-lookup"><span data-stu-id="0b534-103">CInstance::SetWBEMINT64 methods</span></span>

<span data-ttu-id="0b534-104">\[A classe [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="0b534-104">\[The [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0b534-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="0b534-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0b534-106">O método [**CInstance:: GetWBEMINT64**](cinstance-getwbemint64.md) define uma propriedade de inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0b534-106">The [**CInstance::GetWBEMINT64**](cinstance-getwbemint64.md) method sets a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0b534-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="0b534-107">Overload list</span></span>



| <span data-ttu-id="0b534-108">Método</span><span class="sxs-lookup"><span data-stu-id="0b534-108">Method</span></span>                                                                                               | <span data-ttu-id="0b534-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b534-109">Description</span></span>                                |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------|
| <span data-ttu-id="0b534-110">[**SetWBEMINT64 (LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span><span class="sxs-lookup"><span data-stu-id="0b534-110">[**SetWBEMINT64(LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span></span>    | <span data-ttu-id="0b534-111">Define uma propriedade de inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0b534-111">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="0b534-112">[**SetWBEMINT64 (LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="0b534-112">[**SetWBEMINT64(LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span> | <span data-ttu-id="0b534-113">Define uma propriedade de inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0b534-113">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="0b534-114">[**SetWBEMINT64 (LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="0b534-114">[**SetWBEMINT64(LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span>  | <span data-ttu-id="0b534-115">Define uma propriedade de inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0b534-115">Sets a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0b534-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b534-116">Requirements</span></span>



| <span data-ttu-id="0b534-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b534-117">Requirement</span></span> | <span data-ttu-id="0b534-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0b534-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b534-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b534-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b534-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b534-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="0b534-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b534-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b534-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b534-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="0b534-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b534-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b534-124"><dt>Instance. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b534-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0b534-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b534-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b534-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b534-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="0b534-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0b534-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b534-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b534-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b534-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b534-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b534-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="0b534-130">**CInstance**</span></span>](/windows/win32/api/instance/nl-instance-cinstance)
</dt> </dl>

<span data-ttu-id="0b534-131">�</span><span class="sxs-lookup"><span data-stu-id="0b534-131">�</span></span>

<span data-ttu-id="0b534-132">�</span><span class="sxs-lookup"><span data-stu-id="0b534-132">�</span></span>
