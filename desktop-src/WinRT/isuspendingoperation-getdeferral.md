---
description: Solicita que a operação de suspensão do aplicativo seja atrasada.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'Método ISuspendingOperation:: getadiamento (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827135"
---
# <a name="isuspendingoperationgetdeferral-method"></a><span data-ttu-id="3f44a-103">Método ISuspendingOperation:: getadiamento</span><span class="sxs-lookup"><span data-stu-id="3f44a-103">ISuspendingOperation::GetDeferral method</span></span>

<span data-ttu-id="3f44a-104">Solicita que a operação de suspensão do aplicativo seja atrasada.</span><span class="sxs-lookup"><span data-stu-id="3f44a-104">Requests that the app suspending operation be delayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f44a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f44a-105">Syntax</span></span>


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a><span data-ttu-id="3f44a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f44a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f44a-107">*adiamento* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3f44a-107">*deferral* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3f44a-108">A suspensão de adiamento.</span><span class="sxs-lookup"><span data-stu-id="3f44a-108">The deferral suspension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f44a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f44a-109">Return value</span></span>

<span data-ttu-id="3f44a-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3f44a-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f44a-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f44a-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f44a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f44a-112">Requirements</span></span>



| <span data-ttu-id="3f44a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f44a-113">Requirement</span></span> | <span data-ttu-id="3f44a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3f44a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f44a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f44a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3f44a-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3f44a-116">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3f44a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f44a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3f44a-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f44a-118">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3f44a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f44a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f44a-120"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f44a-120"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f44a-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="3f44a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f44a-122"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f44a-122"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f44a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f44a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f44a-124">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="3f44a-124">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




