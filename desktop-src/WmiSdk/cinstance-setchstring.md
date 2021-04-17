---
description: 'O método CInstance:: SetCHString define uma propriedade de cadeia de caracteres.'
ms.assetid: a75b574d-9ee7-4930-a003-5d71c5f1d687
ms.tgt_platform: multiple
title: 'Métodos CInstance:: SetCHString (instance. h)'
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
ms.openlocfilehash: 187c07b5cf0f867ee838f2f3725d6a82319d4634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762818"
---
# <a name="cinstancesetchstring-methods"></a><span data-ttu-id="d61b4-103">Métodos CInstance:: SetCHString</span><span class="sxs-lookup"><span data-stu-id="d61b4-103">CInstance::SetCHString methods</span></span>

<span data-ttu-id="d61b4-104">\[A classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="d61b4-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d61b4-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="d61b4-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d61b4-106">O método **CInstance:: SetCHString** define uma propriedade de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d61b4-106">The **CInstance::SetCHString** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d61b4-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="d61b4-107">Overload list</span></span>



| <span data-ttu-id="d61b4-108">Método</span><span class="sxs-lookup"><span data-stu-id="d61b4-108">Method</span></span>                                                                                           | <span data-ttu-id="d61b4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d61b4-109">Description</span></span>                        |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="d61b4-110">[**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="d61b4-110">[**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span></span>                   | <span data-ttu-id="d61b4-111">Define uma propriedade de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d61b4-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="d61b4-112">[**SetCHString (LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span><span class="sxs-lookup"><span data-stu-id="d61b4-112">[**SetCHString(LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span></span> | <span data-ttu-id="d61b4-113">Define uma propriedade de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d61b4-113">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d61b4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d61b4-114">Requirements</span></span>



| <span data-ttu-id="d61b4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d61b4-115">Requirement</span></span> | <span data-ttu-id="d61b4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d61b4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d61b4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d61b4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d61b4-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d61b4-118">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d61b4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d61b4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d61b4-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d61b4-120">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d61b4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d61b4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d61b4-122"><dt>Instance. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d61b4-122"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d61b4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d61b4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d61b4-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d61b4-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="d61b4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d61b4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d61b4-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d61b4-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d61b4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d61b4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d61b4-128">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="d61b4-128">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

