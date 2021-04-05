---
title: Constantes de WINBIO_IDENTITY_TYPE (WinBio \_ Types. h)
description: Especifique o formato das informações de identidade contidas na \_ estrutura de identidade WINBIO.
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918222"
---
# <a name="winbio_identity_type-constants"></a><span data-ttu-id="f28f1-103">Constantes de tipo de \_ identidade WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="f28f1-103">WINBIO\_IDENTITY\_TYPE Constants</span></span>

<span data-ttu-id="f28f1-104">As constantes **de \_ \_ tipo de identidade WINBIO** a seguir podem ser usadas para especificar o formato das informações de identidade contidas na estrutura de [**\_ identidade WINBIO**](winbio-identity.md) .</span><span class="sxs-lookup"><span data-stu-id="f28f1-104">The following **WINBIO\_IDENTITY\_TYPE** constants can be used to specify the format of the identity information contained in the [**WINBIO\_IDENTITY**](winbio-identity.md) structure.</span></span>



| <span data-ttu-id="f28f1-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f28f1-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="f28f1-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f28f1-106">Description</span></span>                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="f28f1-107"><dt>**\_tipo de ID WINBIO \_ \_ NULL**</dt></span><span class="sxs-lookup"><span data-stu-id="f28f1-107"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="f28f1-108">O modelo não tem nenhuma ID associada.</span><span class="sxs-lookup"><span data-stu-id="f28f1-108">The template has no associated ID.</span></span> <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="f28f1-109"><dt>**\_tipo de ID WINBIO \_ \_ curinga**</dt></span><span class="sxs-lookup"><span data-stu-id="f28f1-109"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="f28f1-110">A estrutura corresponde a todas as identidades de modelo.</span><span class="sxs-lookup"><span data-stu-id="f28f1-110">The structure matches all template identities.</span></span><br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="f28f1-111"><dt>**\_GUID do \_ tipo de ID de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f28f1-111"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="f28f1-112">Um GUID identifica o modelo.</span><span class="sxs-lookup"><span data-stu-id="f28f1-112">A GUID identifies the template.</span></span><br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="f28f1-113"><dt>**\_SID do \_ tipo de ID de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f28f1-113"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="f28f1-114">Um SID de conta identifica o modelo.</span><span class="sxs-lookup"><span data-stu-id="f28f1-114">An account SID identifies the template.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="f28f1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f28f1-115">Requirements</span></span>



| <span data-ttu-id="f28f1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f28f1-116">Requirement</span></span> | <span data-ttu-id="f28f1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f28f1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f28f1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f28f1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f28f1-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f28f1-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f28f1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f28f1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f28f1-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f28f1-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f28f1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f28f1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f28f1-123"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f28f1-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f28f1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f28f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f28f1-125">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="f28f1-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="f28f1-126">**\_identidade WINBIO**</span><span class="sxs-lookup"><span data-stu-id="f28f1-126">**WINBIO\_IDENTITY**</span></span>](winbio-identity.md)
</dt> </dl>

 

 





