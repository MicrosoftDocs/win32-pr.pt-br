---
description: Cada um dos construtores a seguir inicializa um novo objeto CHString com os dados especificados.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'Construtores CHString:: CHString (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169808"
---
# <a name="chstringchstring-constructors"></a><span data-ttu-id="a5445-103">Construtores CHString:: CHString</span><span class="sxs-lookup"><span data-stu-id="a5445-103">CHString::CHString constructors</span></span>

<span data-ttu-id="a5445-104">\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="a5445-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="a5445-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="a5445-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="a5445-106">Cada um dos construtores a seguir inicializa um novo objeto [**CHString**](chstring.md) com os dados especificados.</span><span class="sxs-lookup"><span data-stu-id="a5445-106">Each of the following constructors initializes a new [**CHString**](chstring.md) object with the specified data.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a5445-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="a5445-107">Overload list</span></span>



| <span data-ttu-id="a5445-108">Construtor</span><span class="sxs-lookup"><span data-stu-id="a5445-108">Constructor</span></span>                                                                        | <span data-ttu-id="a5445-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5445-109">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="a5445-110">**CHString()**</span><span class="sxs-lookup"><span data-stu-id="a5445-110">**CHString()**</span></span>](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | <span data-ttu-id="a5445-111">Cria um objeto CHString vazio.</span><span class="sxs-lookup"><span data-stu-id="a5445-111">Creates an empty CHString object.</span></span><br/>                 |
| <span data-ttu-id="a5445-112">[**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span><span class="sxs-lookup"><span data-stu-id="a5445-112">[**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span></span>                              | <span data-ttu-id="a5445-113">Inicializa com o valor LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a5445-113">Initializes with the LPCSTR value.</span></span><br/>                |
| <span data-ttu-id="a5445-114">[**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="a5445-114">[**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span></span>                            | <span data-ttu-id="a5445-115">Inicializa com o valor LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="a5445-115">Initializes with the LPCWSTR value.</span></span><br/>               |
| <span data-ttu-id="a5445-116">[**CHString (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span><span class="sxs-lookup"><span data-stu-id="a5445-116">[**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span></span>                        | <span data-ttu-id="a5445-117">Inicializa com cópias int do valor WCHAR.</span><span class="sxs-lookup"><span data-stu-id="a5445-117">Initializes with int copies of the WCHAR value.</span></span><br/>   |
| <span data-ttu-id="a5445-118">[**CHString (LPCWSTR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span><span class="sxs-lookup"><span data-stu-id="a5445-118">[**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span></span>                    | <span data-ttu-id="a5445-119">Inicializa com cópias int do valor LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="a5445-119">Initializes with int copies of the LPCWSTR value.</span></span><br/> |
| <span data-ttu-id="a5445-120">[**CHString (const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="a5445-120">[**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span></span>            | <span data-ttu-id="a5445-121">Replica o parâmetro CHString.</span><span class="sxs-lookup"><span data-stu-id="a5445-121">Replicates the CHString parameter.</span></span><br/>                |
| <span data-ttu-id="a5445-122">[**CHString (const não assinado \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span><span class="sxs-lookup"><span data-stu-id="a5445-122">[**CHString(const unsigned char\*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span></span> | <span data-ttu-id="a5445-123">Inicializa com o valor apontado por Char \* .</span><span class="sxs-lookup"><span data-stu-id="a5445-123">Initializes with the value pointed to by char\*.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="a5445-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5445-124">Requirements</span></span>



| <span data-ttu-id="a5445-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5445-125">Requirement</span></span> | <span data-ttu-id="a5445-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a5445-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5445-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5445-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a5445-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5445-128">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a5445-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5445-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a5445-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5445-130">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="a5445-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5445-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5445-132"><dt>ChString. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5445-132"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a5445-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5445-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5445-134"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5445-134"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="a5445-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a5445-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5445-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5445-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="a5445-137">�</span><span class="sxs-lookup"><span data-stu-id="a5445-137">�</span></span>

<span data-ttu-id="a5445-138">�</span><span class="sxs-lookup"><span data-stu-id="a5445-138">�</span></span>
