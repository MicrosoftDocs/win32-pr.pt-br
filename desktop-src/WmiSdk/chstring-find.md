---
description: O método Find pesquisa uma cadeia de caracteres para a primeira correspondência de uma subcadeia de caracteres.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: 'Métodos CHString:: find (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5996ca5c06e2101fad834ce2e37df31ee435fbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761695"
---
# <a name="chstringfind-methods"></a><span data-ttu-id="53de5-103">Métodos CHString:: find</span><span class="sxs-lookup"><span data-stu-id="53de5-103">CHString::Find methods</span></span>

<span data-ttu-id="53de5-104">\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="53de5-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="53de5-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="53de5-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="53de5-106">O método **Find** pesquisa uma cadeia de caracteres para a primeira correspondência de uma subcadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="53de5-106">The **Find** method searches a string for the first match of a substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="53de5-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="53de5-107">Overload list</span></span>



| <span data-ttu-id="53de5-108">Método</span><span class="sxs-lookup"><span data-stu-id="53de5-108">Method</span></span>                                          | <span data-ttu-id="53de5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="53de5-109">Description</span></span>                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| <span data-ttu-id="53de5-110">[**Localizar (WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="53de5-110">[**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span>     | <span data-ttu-id="53de5-111">Procura o **WSTR** nesta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="53de5-111">Searches for the **WSTR** in this string.</span></span><br/>    |
| <span data-ttu-id="53de5-112">[**Localizar (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="53de5-112">[**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span> | <span data-ttu-id="53de5-113">Procura o **LPCWSTR** nesta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="53de5-113">Searches for the **LPCWSTR** in this string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="53de5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53de5-114">Requirements</span></span>



| <span data-ttu-id="53de5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="53de5-115">Requirement</span></span> | <span data-ttu-id="53de5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="53de5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53de5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53de5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53de5-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53de5-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="53de5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53de5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53de5-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53de5-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="53de5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53de5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="53de5-122"><dt>ChString. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53de5-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="53de5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53de5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="53de5-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53de5-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="53de5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="53de5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53de5-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53de5-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="53de5-127">�</span><span class="sxs-lookup"><span data-stu-id="53de5-127">�</span></span>

<span data-ttu-id="53de5-128">�</span><span class="sxs-lookup"><span data-stu-id="53de5-128">�</span></span>
