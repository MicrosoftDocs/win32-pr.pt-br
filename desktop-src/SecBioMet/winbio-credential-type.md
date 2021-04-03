---
title: Enumeração de WINBIO_CREDENTIAL_TYPE (WinBio \_ Types. h)
description: Define sinalizadores que podem ser usados para filtrar o tipo de credencial.
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_CREDENTIAL_TYPE
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae41693db264308d33bc30191bdb73007b6b2dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824782"
---
# <a name="winbio_credential_type-enumeration"></a><span data-ttu-id="95afc-104">\_Enumeração de tipo de credencial WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="95afc-104">WINBIO\_CREDENTIAL\_TYPE enumeration</span></span>

<span data-ttu-id="95afc-105">Define sinalizadores que podem ser usados para filtrar o tipo de credencial.</span><span class="sxs-lookup"><span data-stu-id="95afc-105">Defines flags that can be used to filter on the credential type.</span></span> <span data-ttu-id="95afc-106">Essa enumeração é usada pelas funções [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)e [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="95afc-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential), and [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="95afc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95afc-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a><span data-ttu-id="95afc-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="95afc-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="95afc-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**\_senha de credencial WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="95afc-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO\_CREDENTIAL\_PASSWORD**</span></span>
</dt> <dd>

<span data-ttu-id="95afc-110">Filtra as credenciais de senha.</span><span class="sxs-lookup"><span data-stu-id="95afc-110">Filters password credentials.</span></span>

</dd> <dt>

<span data-ttu-id="95afc-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO \_ credencial \_ All**</span><span class="sxs-lookup"><span data-stu-id="95afc-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO\_CREDENTIAL\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="95afc-112">Filtra todas as credenciais.</span><span class="sxs-lookup"><span data-stu-id="95afc-112">Filters all credentials.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95afc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95afc-113">Requirements</span></span>



| <span data-ttu-id="95afc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="95afc-114">Requirement</span></span> | <span data-ttu-id="95afc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="95afc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95afc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95afc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95afc-117">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="95afc-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="95afc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95afc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95afc-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="95afc-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="95afc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95afc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="95afc-121"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95afc-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95afc-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="95afc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95afc-123">Enumerações de aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="95afc-123">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="95afc-124">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="95afc-124">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[<span data-ttu-id="95afc-125">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="95afc-125">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[<span data-ttu-id="95afc-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="95afc-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





