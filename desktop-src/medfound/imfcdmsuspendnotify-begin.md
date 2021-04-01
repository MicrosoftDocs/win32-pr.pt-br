---
description: Indica que o processo de suspensão está sendo iniciado e os recursos devem ser colocados em um estado consistente.
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: 'Método IMFCdmSuspendNotify:: Begin'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 84453a6c846e88a9d6e6c32c5253d97d36e89c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646690"
---
# <a name="imfcdmsuspendnotifybegin-method"></a><span data-ttu-id="2f759-103">Método IMFCdmSuspendNotify:: Begin</span><span class="sxs-lookup"><span data-stu-id="2f759-103">IMFCdmSuspendNotify::Begin method</span></span>

<span data-ttu-id="2f759-104">Indica que o processo de suspensão está sendo iniciado e os recursos devem ser colocados em um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="2f759-104">Indicates that the suspend process is starting and resources should be brought into a consistent state.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f759-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f759-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="2f759-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f759-106">Parameters</span></span>

<span data-ttu-id="2f759-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2f759-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f759-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f759-108">Return value</span></span>

<span data-ttu-id="2f759-109">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2f759-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f759-110">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f759-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f759-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f759-111">Requirements</span></span>



| <span data-ttu-id="2f759-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f759-112">Requirement</span></span> | <span data-ttu-id="2f759-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2f759-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f759-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f759-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2f759-115">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f759-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2f759-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f759-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2f759-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="2f759-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2f759-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="2f759-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f759-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f759-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f759-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f759-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f759-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="2f759-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




