---
description: Executa o item de pasta do Shell especificado na estrutura SMDATA acompanhada.
title: Mensagem de SMC_SFEXEC (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b4e414cd7dab9968882272b19b9b21b95da0f1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968048"
---
# <a name="smc_sfexec-message"></a><span data-ttu-id="704f6-103">Mensagem do SMC \_ SFEXEC</span><span class="sxs-lookup"><span data-stu-id="704f6-103">SMC\_SFEXEC message</span></span>

<span data-ttu-id="704f6-104">Executa o item de pasta do Shell especificado na estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) acompanhada.</span><span class="sxs-lookup"><span data-stu-id="704f6-104">Execute the Shell folder item specified in the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFEXEC
            
```



## <a name="parameters"></a><span data-ttu-id="704f6-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="704f6-105">Parameters</span></span>

<span data-ttu-id="704f6-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="704f6-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="704f6-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="704f6-107">Return value</span></span>

<span data-ttu-id="704f6-108">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="704f6-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="704f6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="704f6-109">Remarks</span></span>

<span data-ttu-id="704f6-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="704f6-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="704f6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="704f6-111">Requirements</span></span>



| <span data-ttu-id="704f6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="704f6-112">Requirement</span></span> | <span data-ttu-id="704f6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="704f6-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="704f6-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="704f6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="704f6-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="704f6-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="704f6-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="704f6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="704f6-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="704f6-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="704f6-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="704f6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="704f6-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="704f6-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="704f6-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="704f6-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="704f6-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="704f6-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




