---
description: O método mid extrai uma subcadeia de caracteres nCount de comprimento de uma cadeia de caracteres CHString, começando na posição nPrimeiro (baseada em zero). O método retorna uma cópia da subcadeia de caracteres extraída.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'Métodos CHString:: mid (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772588"
---
# <a name="chstringmid-methods"></a><span data-ttu-id="9a5d7-104">Métodos CHString:: mid</span><span class="sxs-lookup"><span data-stu-id="9a5d7-104">CHString::Mid methods</span></span>

<span data-ttu-id="9a5d7-105">\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="9a5d7-106">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="9a5d7-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="9a5d7-107">O método **mid** extrai uma subcadeia de caracteres *nCount* de comprimento de uma cadeia de caracteres [**CHString**](chstring.md) , começando na posição *nPrimeiro* (baseada em zero).</span><span class="sxs-lookup"><span data-stu-id="9a5d7-107">The **Mid** method extracts a substring of length *nCount* characters from a [**CHString**](chstring.md) string, starting at position *nFirst* (zero-based).</span></span> <span data-ttu-id="9a5d7-108">O método retorna uma cópia da subcadeia de caracteres extraída.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-108">The method returns a copy of the extracted substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9a5d7-109">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="9a5d7-109">Overload list</span></span>



| <span data-ttu-id="9a5d7-110">Método</span><span class="sxs-lookup"><span data-stu-id="9a5d7-110">Method</span></span>                                        | <span data-ttu-id="9a5d7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a5d7-111">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="9a5d7-112">[**Mid (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span><span class="sxs-lookup"><span data-stu-id="9a5d7-112">[**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span></span> | <span data-ttu-id="9a5d7-113">Extrai uma subcadeia de caracteres de comprimento e ponto inicial especificados.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-113">Extracts a substring of specified length and beginning point.</span></span><br/> |
| <span data-ttu-id="9a5d7-114">[**Mid (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="9a5d7-114">[**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>         | <span data-ttu-id="9a5d7-115">Extrai uma subcadeia de caracteres começando em int.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-115">Extracts a substring beginning at int.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="9a5d7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a5d7-116">Requirements</span></span>



| <span data-ttu-id="9a5d7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a5d7-117">Requirement</span></span> | <span data-ttu-id="9a5d7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9a5d7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5d7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a5d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a5d7-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a5d7-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="9a5d7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a5d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a5d7-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a5d7-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="9a5d7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a5d7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a5d7-124"><dt>ChString. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a5d7-124"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a5d7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a5d7-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a5d7-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a5d7-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="9a5d7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9a5d7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a5d7-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a5d7-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="9a5d7-129">�</span><span class="sxs-lookup"><span data-stu-id="9a5d7-129">�</span></span>

<span data-ttu-id="9a5d7-130">�</span><span class="sxs-lookup"><span data-stu-id="9a5d7-130">�</span></span>
