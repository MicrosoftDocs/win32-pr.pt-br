---
description: Obtém a operação de suspensão do aplicativo.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'Propriedade ISuspendingEventArgs:: SuspendingOperation (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827136"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a><span data-ttu-id="81378-103">Propriedade ISuspendingEventArgs:: SuspendingOperation</span><span class="sxs-lookup"><span data-stu-id="81378-103">ISuspendingEventArgs::SuspendingOperation property</span></span>

<span data-ttu-id="81378-104">Obtém a operação de suspensão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81378-104">Gets the app suspending operation.</span></span>

<span data-ttu-id="81378-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="81378-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="81378-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="81378-106">Syntax</span></span>


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a><span data-ttu-id="81378-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="81378-107">Property value</span></span>

<span data-ttu-id="81378-108">A operação de suspensão.</span><span class="sxs-lookup"><span data-stu-id="81378-108">The suspending operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="81378-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81378-109">Requirements</span></span>



| <span data-ttu-id="81378-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="81378-110">Requirement</span></span> | <span data-ttu-id="81378-111">Valor</span><span class="sxs-lookup"><span data-stu-id="81378-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81378-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81378-112">Minimum supported client</span></span><br/> | <span data-ttu-id="81378-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="81378-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="81378-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81378-114">Minimum supported server</span></span><br/> | <span data-ttu-id="81378-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81378-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="81378-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81378-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="81378-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="81378-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="81378-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="81378-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81378-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81378-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81378-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="81378-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81378-121">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="81378-121">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 




