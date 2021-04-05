---
title: Constantes gerais (WinBio \_ Types. h)
description: Especifique o comprimento máximo do SID, identificadores, IDs, comprimento máximo da cadeia de caracteres e tamanho máximo do buffer de exemplo.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918446"
---
# <a name="general-constants-winbio_typesh"></a><span data-ttu-id="fd79b-103">Constantes gerais (WinBio \_ Types. h)</span><span class="sxs-lookup"><span data-stu-id="fd79b-103">General Constants (Winbio\_types.h)</span></span>

<span data-ttu-id="fd79b-104">As constantes a seguir são usadas em todo o Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="fd79b-104">The following constants are used throughout the Windows Biometric Framework.</span></span>



| <span data-ttu-id="fd79b-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="fd79b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="fd79b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd79b-106">Description</span></span>                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <span data-ttu-id="fd79b-107"><dt>**\_tamanho máximo de \_ SID \_ de segurança**</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-107"><dt>**SECURITY\_MAX\_SID\_SIZE**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="fd79b-108">O comprimento máximo de um valor de SID (identificador de segurança).</span><span class="sxs-lookup"><span data-stu-id="fd79b-108">The maximum length of a security identifier (SID) value.</span></span> <span data-ttu-id="fd79b-109">Atualmente, isso é 68.</span><span class="sxs-lookup"><span data-stu-id="fd79b-109">Currently this is 68.</span></span><br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <span data-ttu-id="fd79b-110"><dt>**\_ID da unidade WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-110"><dt>**WINBIO\_UNIT\_ID**</dt></span></span> </dl>                                                                                                                | <span data-ttu-id="fd79b-111">Número de identificação de uma unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="fd79b-111">ID number of a biometric unit.</span></span><br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <span data-ttu-id="fd79b-112"><dt>**\_identificador de sessão WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-112"><dt>**WINBIO\_SESSION\_HANDLE**</dt></span></span> </dl>                                                                                           | <span data-ttu-id="fd79b-113">Um inteiro longo sem sinal que contém o identificador para uma sessão biométrica aberta.</span><span class="sxs-lookup"><span data-stu-id="fd79b-113">An unsigned long integer that contains the handle for an open biometric session.</span></span><br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <span data-ttu-id="fd79b-114"><dt>**\_identificador de estrutura WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-114"><dt>**WINBIO\_FRAMEWORK\_HANDLE**</dt></span></span> </dl>                                                                                     | <span data-ttu-id="fd79b-115">Um inteiro longo sem sinal que contém o identificador para uma sessão aberta do Framework.</span><span class="sxs-lookup"><span data-stu-id="fd79b-115">An unsigned long integer that contains the handle for an open framework session.</span></span><br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <span data-ttu-id="fd79b-116"><dt>**UUID de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-116"><dt>**WINBIO\_UUID**</dt></span></span> </dl>                                                                                                                          | <span data-ttu-id="fd79b-117">Uma GUID.</span><span class="sxs-lookup"><span data-stu-id="fd79b-117">A GUID.</span></span><br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <span data-ttu-id="fd79b-118"><dt>**\_cadeia de caracteres WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-118"><dt>**WINBIO\_STRING**</dt></span></span> </dl>                                                                                                                    | <span data-ttu-id="fd79b-119">Uma matriz de bytes que contém uma cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="fd79b-119">A byte array that contains a null-terminated Unicode string.</span></span><br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <span data-ttu-id="fd79b-120"><dt>**WINBIO \_ \_ \_ comp. máximo de cadeia de caracteres**</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-120"><dt>**WINBIO\_MAX\_STRING\_LEN** </dt></span></span> </dl>                                                                                       | <span data-ttu-id="fd79b-121">O comprimento máximo de um valor de **\_ cadeia de caracteres WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="fd79b-121">The maximum length of a **WINBIO\_STRING** value.</span></span> <span data-ttu-id="fd79b-122">Atualmente, isso é 256.</span><span class="sxs-lookup"><span data-stu-id="fd79b-122">Currently this is 256.</span></span><br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <span data-ttu-id="fd79b-123"><dt>**WINBIO \_ \_ \_ \_ Tamanho máximo do buffer de exemplo**</dt> <dt>0x7FFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-123"><dt>**WINBIO\_MAX\_SAMPLE\_BUFFER\_SIZE**</dt> <dt>0x7FFFFFFF</dt></span></span> </dl> | <span data-ttu-id="fd79b-124">O número máximo de bytes em uma única captura de dados biométricas.</span><span class="sxs-lookup"><span data-stu-id="fd79b-124">The maximum number of bytes in a single biometric data capture.</span></span><br/>                  |



## <a name="requirements"></a><span data-ttu-id="fd79b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd79b-125">Requirements</span></span>



| <span data-ttu-id="fd79b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd79b-126">Requirement</span></span> | <span data-ttu-id="fd79b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fd79b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd79b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd79b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fd79b-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd79b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="fd79b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd79b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fd79b-131">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="fd79b-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fd79b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd79b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd79b-133"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd79b-133"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd79b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd79b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd79b-135">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="fd79b-135">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





