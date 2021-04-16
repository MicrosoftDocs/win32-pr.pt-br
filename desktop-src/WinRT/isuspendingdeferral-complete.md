---
description: Notifica o sistema que o aplicativo salvou seus dados e está pronto para ser suspenso.
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'Método ISuspendingDeferral:: Complete (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764974"
---
# <a name="isuspendingdeferralcomplete-method"></a><span data-ttu-id="ee4ff-103">Método ISuspendingDeferral:: Complete</span><span class="sxs-lookup"><span data-stu-id="ee4ff-103">ISuspendingDeferral::Complete method</span></span>

<span data-ttu-id="ee4ff-104">Notifica o sistema que o aplicativo salvou seus dados e está pronto para ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="ee4ff-104">Notifies the system that the app has saved its data and is ready to be suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee4ff-105">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="ee4ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee4ff-106">Parameters</span></span>

<span data-ttu-id="ee4ff-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ee4ff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee4ff-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee4ff-108">Return value</span></span>

<span data-ttu-id="ee4ff-109">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ee4ff-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee4ff-110">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee4ff-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee4ff-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee4ff-111">Requirements</span></span>



| <span data-ttu-id="ee4ff-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4ff-112">Requirement</span></span> | <span data-ttu-id="ee4ff-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ee4ff-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4ff-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee4ff-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4ff-115">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ee4ff-115">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ee4ff-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee4ff-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4ff-117">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee4ff-117">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ee4ff-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee4ff-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4ff-119"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ff-119"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee4ff-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="ee4ff-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee4ff-121"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ff-121"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee4ff-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee4ff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4ff-123">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="ee4ff-123">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 




