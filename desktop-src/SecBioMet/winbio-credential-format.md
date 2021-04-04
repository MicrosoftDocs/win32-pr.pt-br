---
title: Enumeração de WINBIO_CREDENTIAL_FORMAT (WinBio \_ Types. h)
description: Define sinalizadores que podem ser usados para especificar o formato de credencial do usuário final.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_CREDENTIAL_FORMAT
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085561"
---
# <a name="winbio_credential_format-enumeration"></a><span data-ttu-id="80b42-104">\_Enumeração de formato de credencial WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="80b42-104">WINBIO\_CREDENTIAL\_FORMAT enumeration</span></span>

<span data-ttu-id="80b42-105">Define sinalizadores que podem ser usados para especificar o formato de credencial do usuário final.</span><span class="sxs-lookup"><span data-stu-id="80b42-105">Defines flags that can be used to specify the end-user credential format.</span></span> <span data-ttu-id="80b42-106">Essa enumeração é usada pela função [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .</span><span class="sxs-lookup"><span data-stu-id="80b42-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b42-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="80b42-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="80b42-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="80b42-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="80b42-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ senha \_ genérica**</span><span class="sxs-lookup"><span data-stu-id="80b42-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO\_PASSWORD\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="80b42-110">A senha está em um formato genérico.</span><span class="sxs-lookup"><span data-stu-id="80b42-110">The password is in a generic format.</span></span>

</dd> <dt>

<span data-ttu-id="80b42-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO \_ senha \_ empacotada**</span><span class="sxs-lookup"><span data-stu-id="80b42-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO\_PASSWORD\_PACKED**</span></span>
</dt> <dd>

<span data-ttu-id="80b42-112">A senha está em um formato compactado.</span><span class="sxs-lookup"><span data-stu-id="80b42-112">The password is in a compressed format.</span></span>

</dd> <dt>

<span data-ttu-id="80b42-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ \_ protegido por senha**</span><span class="sxs-lookup"><span data-stu-id="80b42-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO\_PASSWORD\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="80b42-114">A credencial de senha foi encapsulada com [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span><span class="sxs-lookup"><span data-stu-id="80b42-114">The password credential was wrapped with [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80b42-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80b42-115">Requirements</span></span>



| <span data-ttu-id="80b42-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="80b42-116">Requirement</span></span> | <span data-ttu-id="80b42-117">Valor</span><span class="sxs-lookup"><span data-stu-id="80b42-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b42-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80b42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80b42-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="80b42-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="80b42-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80b42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80b42-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="80b42-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="80b42-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80b42-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80b42-123"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80b42-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b42-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="80b42-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b42-125">Enumerações de aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="80b42-125">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="80b42-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="80b42-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

