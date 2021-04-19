---
description: Obtém o número de perfis de verificação criados para o usuário no sistema em que seu aplicativo está sendo executado.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'Método IScanProfileMgr:: GetNumProfiles (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771591"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a><span data-ttu-id="e3cd7-103">Método IScanProfileMgr:: GetNumProfiles</span><span class="sxs-lookup"><span data-stu-id="e3cd7-103">IScanProfileMgr::GetNumProfiles method</span></span>

<span data-ttu-id="e3cd7-104">Obtém o número de perfis de verificação criados para o usuário no sistema em que seu aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-104">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3cd7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3cd7-105">Syntax</span></span>


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="e3cd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3cd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3cd7-107">*pulNumProfiles* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e3cd7-107">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cd7-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="e3cd7-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="e3cd7-109">Um ponteiro para o número de perfis criados para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-109">A pointer to the number of profiles created for the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3cd7-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3cd7-110">Return value</span></span>

<span data-ttu-id="e3cd7-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e3cd7-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e3cd7-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3cd7-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3cd7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3cd7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3cd7-114">Requirements</span></span>



| <span data-ttu-id="e3cd7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3cd7-115">Requirement</span></span> | <span data-ttu-id="e3cd7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e3cd7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3cd7-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3cd7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3cd7-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3cd7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e3cd7-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3cd7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3cd7-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3cd7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3cd7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3cd7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3cd7-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3cd7-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="e3cd7-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="e3cd7-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3cd7-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3cd7-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3cd7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3cd7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3cd7-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="e3cd7-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="e3cd7-127">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="e3cd7-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




