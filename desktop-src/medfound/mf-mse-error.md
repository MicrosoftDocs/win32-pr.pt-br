---
description: Define os diferentes Estados de erro da extensão de origem de mídia.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Enumeração de MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091155"
---
# <a name="mf_mse_error-enumeration"></a><span data-ttu-id="4fdc9-103">Enumeração de erros do MF \_ MSE \_</span><span class="sxs-lookup"><span data-stu-id="4fdc9-103">MF\_MSE\_ERROR enumeration</span></span>

<span data-ttu-id="4fdc9-104">Define os diferentes Estados de erro da extensão de origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="4fdc9-104">Defines the different error states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fdc9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fdc9-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a><span data-ttu-id="4fdc9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="4fdc9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4fdc9-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**\_ \_ erro \_ NOERROR do MF MSE**</span><span class="sxs-lookup"><span data-stu-id="4fdc9-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF\_MSE\_ERROR\_NOERROR**</span></span>
</dt> <dd>

<span data-ttu-id="4fdc9-108">Não especifica nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="4fdc9-108">Specifies no error.</span></span>

</dd> <dt>

<span data-ttu-id="4fdc9-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**rede de erros do MF \_ MSE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4fdc9-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF\_MSE\_ERROR\_NETWORK**</span></span>
</dt> <dd>

<span data-ttu-id="4fdc9-110">Especifica um erro com a rede.</span><span class="sxs-lookup"><span data-stu-id="4fdc9-110">Specifies an error with the network.</span></span>

</dd> <dt>

<span data-ttu-id="4fdc9-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**decodificação de \_ erro MF MSE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4fdc9-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF\_MSE\_ERROR\_DECODE**</span></span>
</dt> <dd>

<span data-ttu-id="4fdc9-112">Especifica um erro com decodificação.</span><span class="sxs-lookup"><span data-stu-id="4fdc9-112">Specifies an error with decoding.</span></span>

</dd> <dt>

<span data-ttu-id="4fdc9-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**erro \_ \_ desconhecido de \_ erro \_ do MF MSE**</span><span class="sxs-lookup"><span data-stu-id="4fdc9-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF\_MSE\_ERROR\_UNKNOWN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="4fdc9-114">Especifica um erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4fdc9-114">Specifies an unknown error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fdc9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fdc9-115">Requirements</span></span>



| <span data-ttu-id="4fdc9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fdc9-116">Requirement</span></span> | <span data-ttu-id="4fdc9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4fdc9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fdc9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4fdc9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4fdc9-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4fdc9-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4fdc9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4fdc9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4fdc9-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="4fdc9-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4fdc9-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="4fdc9-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fdc9-123"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fdc9-123"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fdc9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fdc9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fdc9-125">Enumerações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4fdc9-125">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




