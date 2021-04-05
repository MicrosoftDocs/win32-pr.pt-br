---
description: Enumera novamente todos os perfis de verificação no sistema.
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'Método IScanProfileMgr:: Refresh (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e4af44e95889abf35fe13e1669411513458a16c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921068"
---
# <a name="iscanprofilemgrrefresh-method"></a><span data-ttu-id="d5585-103">Método IScanProfileMgr:: Refresh</span><span class="sxs-lookup"><span data-stu-id="d5585-103">IScanProfileMgr::Refresh method</span></span>

<span data-ttu-id="d5585-104">Enumera novamente todos os perfis de verificação no sistema.</span><span class="sxs-lookup"><span data-stu-id="d5585-104">Re-enumerates all the scan profiles in the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5585-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5585-105">Syntax</span></span>


```C++
HRESULT Refresh();
```



## <a name="parameters"></a><span data-ttu-id="d5585-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5585-106">Parameters</span></span>

<span data-ttu-id="d5585-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d5585-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5585-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5585-108">Return value</span></span>

<span data-ttu-id="d5585-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d5585-109">Type: **HRESULT**</span></span>

<span data-ttu-id="d5585-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d5585-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5585-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5585-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5585-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5585-112">Remarks</span></span>

<span data-ttu-id="d5585-113">Use esse método quando mais de um objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) puder estar criando ou excluindo perfis ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d5585-113">Use this method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5585-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5585-114">Requirements</span></span>



| <span data-ttu-id="d5585-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5585-115">Requirement</span></span> | <span data-ttu-id="d5585-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d5585-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5585-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5585-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5585-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5585-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d5585-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5585-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5585-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5585-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5585-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5585-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5585-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5585-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="d5585-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="d5585-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5585-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5585-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5585-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5585-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5585-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="d5585-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="d5585-127">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="d5585-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




