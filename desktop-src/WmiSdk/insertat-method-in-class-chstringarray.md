---
description: O método InsertAt insere um elemento (ou várias cópias de um elemento) ou todos os elementos de outra matriz em um índice especificado.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: 'Métodos CHStringArray:: InsertAt (ChStrArr. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4047b740778c8d0adf1f2b5981b2f3aac5ba9529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764114"
---
# <a name="chstringarrayinsertat-methods"></a><span data-ttu-id="fe01c-103">Métodos CHStringArray:: InsertAt</span><span class="sxs-lookup"><span data-stu-id="fe01c-103">CHStringArray::InsertAt methods</span></span>

<span data-ttu-id="fe01c-104">\[A classe [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="fe01c-104">\[The [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="fe01c-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="fe01c-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="fe01c-106">O método **InsertAt** insere um elemento (ou várias cópias de um elemento) ou todos os elementos de outra matriz em um índice especificado.</span><span class="sxs-lookup"><span data-stu-id="fe01c-106">The **InsertAt** method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.</span></span>

### <a name="overload-list"></a><span data-ttu-id="fe01c-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="fe01c-107">Overload list</span></span>



| <span data-ttu-id="fe01c-108">Método</span><span class="sxs-lookup"><span data-stu-id="fe01c-108">Method</span></span>                                                                               | <span data-ttu-id="fe01c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe01c-109">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe01c-110">[**InsertAt (int, LPCWSTR, int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe01c-110">[**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span></span>       | <span data-ttu-id="fe01c-111">Insere um ou mais elementos em um índice especificado em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="fe01c-111">Inserts one or more elements at a specified index in an array.</span></span><br/>                                               |
| <span data-ttu-id="fe01c-112">[**InsertAt (int, CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="fe01c-112">[**InsertAt(int,CHStringArray\*)**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span> | <span data-ttu-id="fe01c-113">Insere todos os elementos de outro [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) em um índice especificado em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="fe01c-113">Inserts all the elements of another [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) at a specified index in an array.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fe01c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe01c-114">Requirements</span></span>



| <span data-ttu-id="fe01c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe01c-115">Requirement</span></span> | <span data-ttu-id="fe01c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fe01c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe01c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe01c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fe01c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe01c-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="fe01c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe01c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fe01c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe01c-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="fe01c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe01c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe01c-122"><dt>ChStrArr. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe01c-122"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fe01c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe01c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe01c-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe01c-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="fe01c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fe01c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe01c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe01c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe01c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe01c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe01c-128">**CHStringArray**</span><span class="sxs-lookup"><span data-stu-id="fe01c-128">**CHStringArray**</span></span>](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

<span data-ttu-id="fe01c-129">�</span><span class="sxs-lookup"><span data-stu-id="fe01c-129">�</span></span>

<span data-ttu-id="fe01c-130">�</span><span class="sxs-lookup"><span data-stu-id="fe01c-130">�</span></span>
