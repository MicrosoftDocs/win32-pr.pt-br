---
description: Um método sobrecarregado que libera a memória que contém o caminho.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: 'Métodos CObjectPathParser:: Free (ObjPath. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 86494e569f68d8eff8b691c648ec5e221b28b39d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170620"
---
# <a name="cobjectpathparserfree-methods"></a><span data-ttu-id="d58c2-103">Métodos CObjectPathParser:: Free</span><span class="sxs-lookup"><span data-stu-id="d58c2-103">CObjectPathParser::Free methods</span></span>

<span data-ttu-id="d58c2-104">\[A classe [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="d58c2-104">\[The [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d58c2-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="d58c2-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d58c2-106">Um método sobrecarregado que libera a memória que contém o caminho.</span><span class="sxs-lookup"><span data-stu-id="d58c2-106">An overloaded method that releases the memory that contains the path.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d58c2-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="d58c2-107">Overload list</span></span>



| <span data-ttu-id="d58c2-108">Método</span><span class="sxs-lookup"><span data-stu-id="d58c2-108">Method</span></span>                                                                     | <span data-ttu-id="d58c2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d58c2-109">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| <span data-ttu-id="d58c2-110">[**Gratuito (LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span><span class="sxs-lookup"><span data-stu-id="d58c2-110">[**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span></span>                     | <span data-ttu-id="d58c2-111">Libera a memória que contém o caminho não analisado.</span><span class="sxs-lookup"><span data-stu-id="d58c2-111">Releases the memory that contains the unparsed path.</span></span><br/>                      |
| <span data-ttu-id="d58c2-112">[**Gratuito (ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span><span class="sxs-lookup"><span data-stu-id="d58c2-112">[**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span></span> | <span data-ttu-id="d58c2-113">Libera a memória que contém a estrutura que tem o caminho analisado.</span><span class="sxs-lookup"><span data-stu-id="d58c2-113">Releases the memory that contains the structure that has the parsed path.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d58c2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d58c2-114">Requirements</span></span>



| <span data-ttu-id="d58c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d58c2-115">Requirement</span></span> | <span data-ttu-id="d58c2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d58c2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d58c2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d58c2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d58c2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d58c2-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d58c2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d58c2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d58c2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d58c2-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d58c2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d58c2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d58c2-122"><dt>ObjPath. h (incluir ObjPath. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d58c2-122"><dt>ObjPath.h (include ObjPath.h)</dt></span></span> </dl>                                                      |
| <span data-ttu-id="d58c2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d58c2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d58c2-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d58c2-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="d58c2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d58c2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d58c2-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d58c2-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d58c2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d58c2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d58c2-128">**CObjectPathParser**</span><span class="sxs-lookup"><span data-stu-id="d58c2-128">**CObjectPathParser**</span></span>](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

<span data-ttu-id="d58c2-129">�</span><span class="sxs-lookup"><span data-stu-id="d58c2-129">�</span></span>

<span data-ttu-id="d58c2-130">�</span><span class="sxs-lookup"><span data-stu-id="d58c2-130">�</span></span>
