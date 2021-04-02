---
description: Exclui todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: 'IScanProfileMgr: método eleteAllProfilesForUser de:D (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c5d723379bb542346e3612f70c19a1629d325ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090808"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a><span data-ttu-id="db866-103">IScanProfileMgr: método eleteAllProfilesForUser de:D</span><span class="sxs-lookup"><span data-stu-id="db866-103">IScanProfileMgr::DeleteAllProfilesForUser method</span></span>

<span data-ttu-id="db866-104">Exclui todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="db866-104">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="db866-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db866-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a><span data-ttu-id="db866-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db866-106">Parameters</span></span>

<span data-ttu-id="db866-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="db866-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db866-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db866-108">Return value</span></span>

<span data-ttu-id="db866-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="db866-109">Type: **HRESULT**</span></span>

<span data-ttu-id="db866-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db866-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db866-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db866-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db866-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db866-112">Requirements</span></span>



| <span data-ttu-id="db866-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="db866-113">Requirement</span></span> | <span data-ttu-id="db866-114">Valor</span><span class="sxs-lookup"><span data-stu-id="db866-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="db866-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db866-115">Minimum supported client</span></span><br/> | <span data-ttu-id="db866-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db866-116">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="db866-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db866-117">Minimum supported server</span></span><br/> | <span data-ttu-id="db866-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db866-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db866-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db866-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="db866-120"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="db866-120"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="db866-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="db866-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db866-122"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db866-122"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db866-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="db866-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db866-124">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="db866-124">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="db866-125">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="db866-125">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




