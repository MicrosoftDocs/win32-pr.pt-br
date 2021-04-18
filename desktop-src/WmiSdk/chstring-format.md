---
description: O método Format formata e armazena uma série de caracteres e valores em uma cadeia de caracteres CHString.
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'Métodos CHString:: Format (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7187d2c691c6efb2054d766ae432c55be893cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771419"
---
# <a name="chstringformat-methods"></a><span data-ttu-id="7780b-103">Métodos CHString:: Format</span><span class="sxs-lookup"><span data-stu-id="7780b-103">CHString::Format methods</span></span>

<span data-ttu-id="7780b-104">\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="7780b-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7780b-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="7780b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7780b-106">O método **Format** formata e armazena uma série de caracteres e valores em uma cadeia de caracteres [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="7780b-106">The **Format** method formats and stores a series of characters and values in a [**CHString**](chstring.md) string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7780b-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="7780b-107">Overload list</span></span>



| <span data-ttu-id="7780b-108">Método</span><span class="sxs-lookup"><span data-stu-id="7780b-108">Method</span></span>                                              | <span data-ttu-id="7780b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7780b-109">Description</span></span>                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7780b-110">[**Formato (UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7780b-110">[**Format(UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span></span>       | <span data-ttu-id="7780b-111">Formata esse CHString de acordo com o identificador de recurso especificado pelo **uint**.</span><span class="sxs-lookup"><span data-stu-id="7780b-111">Formats this CHString according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="7780b-112">[**Format (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="7780b-112">[**Format(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span></span> | <span data-ttu-id="7780b-113">Formata esse CHString de acordo com o formato especificado pelo **LPCWSTR**.</span><span class="sxs-lookup"><span data-stu-id="7780b-113">Formats this CHString according to the format specified by the **LPCWSTR**.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="7780b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7780b-114">Requirements</span></span>



| <span data-ttu-id="7780b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7780b-115">Requirement</span></span> | <span data-ttu-id="7780b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7780b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7780b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7780b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7780b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7780b-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="7780b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7780b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7780b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7780b-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="7780b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7780b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7780b-122"><dt>ChString. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7780b-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7780b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7780b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7780b-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7780b-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="7780b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7780b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7780b-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7780b-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="7780b-127">�</span><span class="sxs-lookup"><span data-stu-id="7780b-127">�</span></span>

<span data-ttu-id="7780b-128">�</span><span class="sxs-lookup"><span data-stu-id="7780b-128">�</span></span>
