---
description: Obtém todas as IDs de propriedade disponíveis em um perfil.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Método IScanProfile:: GetAllPropIDs (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763968"
---
# <a name="iscanprofilegetallpropids-method"></a><span data-ttu-id="e3ce9-103">Método IScanProfile:: GetAllPropIDs</span><span class="sxs-lookup"><span data-stu-id="e3ce9-103">IScanProfile::GetAllPropIDs method</span></span>

<span data-ttu-id="e3ce9-104">Obtém todas as IDs de propriedade disponíveis em um perfil.</span><span class="sxs-lookup"><span data-stu-id="e3ce9-104">Gets all available property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ce9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3ce9-105">Syntax</span></span>


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a><span data-ttu-id="e3ce9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3ce9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3ce9-107">*número* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e3ce9-107">*num* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ce9-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="e3ce9-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="e3ce9-109">O número de IDs de propriedade solicitadas ou retornadas.</span><span class="sxs-lookup"><span data-stu-id="e3ce9-109">The number of property IDs requested or returned.</span></span>

</dd> <dt>

<span data-ttu-id="e3ce9-110">_ppid \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3ce9-110">_ppid\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ce9-111">Tipo: \**Propid \** _</span><span class="sxs-lookup"><span data-stu-id="e3ce9-111">Type: \**PROPID\** _</span></span>

<span data-ttu-id="e3ce9-112">Um ponteiro para uma matriz de IDs de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e3ce9-112">A pointer to an array of property IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3ce9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3ce9-113">Return value</span></span>

<span data-ttu-id="e3ce9-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e3ce9-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e3ce9-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3ce9-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3ce9-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3ce9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ce9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3ce9-117">Requirements</span></span>



| <span data-ttu-id="e3ce9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3ce9-118">Requirement</span></span> | <span data-ttu-id="e3ce9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e3ce9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ce9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3ce9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ce9-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3ce9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e3ce9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3ce9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ce9-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3ce9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3ce9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3ce9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3ce9-125"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3ce9-125"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="e3ce9-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="e3ce9-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3ce9-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3ce9-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ce9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3ce9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ce9-129">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="e3ce9-129">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="e3ce9-130">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="e3ce9-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




