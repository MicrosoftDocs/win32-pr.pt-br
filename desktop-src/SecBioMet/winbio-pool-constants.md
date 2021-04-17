---
title: Constantes de WINBIO_POOL (WinBio \_ Types. h)
description: Especifique o tipo de pool de unidades biométricas a ser usado na sessão.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499790"
---
# <a name="winbio_pool-constants"></a><span data-ttu-id="ecb9e-103">\_Constantes do pool WINBIO</span><span class="sxs-lookup"><span data-stu-id="ecb9e-103">WINBIO\_POOL Constants</span></span>

<span data-ttu-id="ecb9e-104">As constantes a seguir podem ser usadas na função [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar o tipo de pool de unidades biométricas a ser usado na sessão.</span><span class="sxs-lookup"><span data-stu-id="ecb9e-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify the type of biometric unit pool to be used in the session.</span></span>



| <span data-ttu-id="ecb9e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="ecb9e-105">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="ecb9e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ecb9e-106">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="ecb9e-107"><dt>**\_pool WINBIO \_ desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="ecb9e-107"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="ecb9e-108">O tipo de pool é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="ecb9e-108">The pool type is unknown.</span></span><br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="ecb9e-109"><dt>**\_sistema de pool WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ecb9e-109"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>             | <span data-ttu-id="ecb9e-110">Especifica uma coleção compartilhada de unidades biométricas gerenciadas pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="ecb9e-110">Specifies a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="ecb9e-111"><dt>**WINBIO \_ pool \_ privado**</dt></span><span class="sxs-lookup"><span data-stu-id="ecb9e-111"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl>          | <span data-ttu-id="ecb9e-112">Especifica uma coleção de unidades biométricas que são gerenciadas pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="ecb9e-112">Specifies a collection of biometric units that are managed by the caller.</span></span><br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <span data-ttu-id="ecb9e-113"><dt>**POOL WINBIO não \_ \_ atribuído**</dt></span><span class="sxs-lookup"><span data-stu-id="ecb9e-113"><dt>**WINBIO\_POOL\_UNASSIGNED**</dt></span></span> </dl> | <span data-ttu-id="ecb9e-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ecb9e-114">Reserved.</span></span><br/>                                                                         |



## <a name="requirements"></a><span data-ttu-id="ecb9e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecb9e-115">Requirements</span></span>



| <span data-ttu-id="ecb9e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecb9e-116">Requirement</span></span> | <span data-ttu-id="ecb9e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ecb9e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb9e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecb9e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb9e-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ecb9e-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ecb9e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecb9e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb9e-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ecb9e-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ecb9e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ecb9e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecb9e-123"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb9e-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb9e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecb9e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb9e-125">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="ecb9e-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





