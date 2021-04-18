---
description: O método FormatMessageW sobrecarregado formata uma cadeia de caracteres de mensagem.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'Métodos CHString:: FormatMessageW (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a4f6be83c2cec8f3ae02cdbafac8a6c10ab72578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791325"
---
# <a name="chstringformatmessagew-methods"></a><span data-ttu-id="68c42-103">Métodos CHString:: FormatMessageW</span><span class="sxs-lookup"><span data-stu-id="68c42-103">CHString::FormatMessageW methods</span></span>

<span data-ttu-id="68c42-104">\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="68c42-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="68c42-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="68c42-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="68c42-106">O método **FormatMessageW** sobrecarregado formata uma cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="68c42-106">The overloaded **FormatMessageW** method formats a message string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="68c42-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="68c42-107">Overload list</span></span>



| <span data-ttu-id="68c42-108">Método</span><span class="sxs-lookup"><span data-stu-id="68c42-108">Method</span></span>                                                              | <span data-ttu-id="68c42-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="68c42-109">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c42-110">[**FormatMessageW (UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="68c42-110">[**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span></span>       | <span data-ttu-id="68c42-111">Formata esta mensagem de acordo com o identificador de recurso especificado pelo **uint**.</span><span class="sxs-lookup"><span data-stu-id="68c42-111">Formats this message according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="68c42-112">[**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="68c42-112">[**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span></span> | <span data-ttu-id="68c42-113">Formata essa cadeia de caracteres de mensagem de acordo com o formato especificado pelo **LPCWSTR**.</span><span class="sxs-lookup"><span data-stu-id="68c42-113">Formats this message string according to the format specified by the **LPCWSTR**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="68c42-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c42-114">Requirements</span></span>



| <span data-ttu-id="68c42-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c42-115">Requirement</span></span> | <span data-ttu-id="68c42-116">Valor</span><span class="sxs-lookup"><span data-stu-id="68c42-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c42-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68c42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68c42-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68c42-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="68c42-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68c42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68c42-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68c42-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="68c42-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68c42-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68c42-122"><dt>ChString. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68c42-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="68c42-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68c42-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="68c42-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68c42-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="68c42-125">DLL</span><span class="sxs-lookup"><span data-stu-id="68c42-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68c42-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68c42-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="68c42-127">�</span><span class="sxs-lookup"><span data-stu-id="68c42-127">�</span></span>

<span data-ttu-id="68c42-128">�</span><span class="sxs-lookup"><span data-stu-id="68c42-128">�</span></span>
