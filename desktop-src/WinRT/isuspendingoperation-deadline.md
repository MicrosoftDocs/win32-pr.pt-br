---
description: Obtém o tempo restante antes de uma operação de suspensão de aplicativo atrasado continuar.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: ISuspendingOperation::D Propriedade Ora (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920916"
---
# <a name="isuspendingoperationdeadline-property"></a><span data-ttu-id="d3d8b-103">ISuspendingOperation: Propriedade Ora de:D</span><span class="sxs-lookup"><span data-stu-id="d3d8b-103">ISuspendingOperation::Deadline property</span></span>

<span data-ttu-id="d3d8b-104">Obtém o tempo restante antes de uma operação de suspensão de aplicativo atrasado continuar.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-104">Gets the time remaining before a delayed app suspending operation continues.</span></span>

<span data-ttu-id="d3d8b-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d8b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3d8b-106">Syntax</span></span>


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a><span data-ttu-id="d3d8b-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d3d8b-107">Property value</span></span>

<span data-ttu-id="d3d8b-108">O tempo restante antes que uma operação de suspensão de aplicativo adiada continue.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-108">The time remaining before a delayed app suspending operation continues.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d8b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3d8b-109">Requirements</span></span>



| <span data-ttu-id="d3d8b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d8b-110">Requirement</span></span> | <span data-ttu-id="d3d8b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d3d8b-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d8b-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3d8b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d8b-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d3d8b-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d3d8b-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3d8b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d8b-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3d8b-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d3d8b-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3d8b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3d8b-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3d8b-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3d8b-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="d3d8b-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3d8b-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3d8b-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d8b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3d8b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d8b-121">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="d3d8b-121">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




