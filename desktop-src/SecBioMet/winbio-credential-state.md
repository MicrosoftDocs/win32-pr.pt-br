---
title: Enumeração de WINBIO_CREDENTIAL_STATE (WinBio \_ Types. h)
description: Define os valores que especificam se uma credencial foi associada aos dados biométricos para um usuário final.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_CREDENTIAL_STATE
- PWINBIO_CREDENTIAL_STATE Windows Biometric Framework API do ponteiro de enumeração
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294769"
---
# <a name="winbio_credential_state-enumeration"></a><span data-ttu-id="9aef7-105">\_Enumeração de estado de credencial WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="9aef7-105">WINBIO\_CREDENTIAL\_STATE enumeration</span></span>

<span data-ttu-id="9aef7-106">Define os valores que especificam se uma credencial foi associada aos dados biométricos para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="9aef7-106">Defines values that specify whether a credential has been associated with the biometric data for an end user.</span></span> <span data-ttu-id="9aef7-107">Essa enumeração é usada pela função [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="9aef7-107">This enumeration is used by the [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aef7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9aef7-108">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a><span data-ttu-id="9aef7-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="9aef7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9aef7-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_credencial WINBIO \_ não \_ definida**</span><span class="sxs-lookup"><span data-stu-id="9aef7-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**WINBIO\_CREDENTIAL\_NOT\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="9aef7-111">Uma credencial foi associada ao usuário final.</span><span class="sxs-lookup"><span data-stu-id="9aef7-111">A credential has been associated with the end user.</span></span>

</dd> <dt>

<span data-ttu-id="9aef7-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**\_conjunto de credenciais WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="9aef7-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO\_CREDENTIAL\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="9aef7-113">Uma credencial não foi associada ao usuário final.</span><span class="sxs-lookup"><span data-stu-id="9aef7-113">A credential has not been associated with the end user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9aef7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aef7-114">Requirements</span></span>



| <span data-ttu-id="9aef7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aef7-115">Requirement</span></span> | <span data-ttu-id="9aef7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9aef7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aef7-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aef7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9aef7-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9aef7-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9aef7-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aef7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9aef7-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="9aef7-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9aef7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aef7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aef7-122"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9aef7-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aef7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9aef7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aef7-124">Enumerações de aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="9aef7-124">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="9aef7-125">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="9aef7-125">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





