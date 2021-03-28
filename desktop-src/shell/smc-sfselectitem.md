---
description: O usuário selecionou o item especificado pela estrutura SMDATA que o acompanha.
title: Mensagem de SMC_SFSELECTITEM (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 82c3dfca-98a8-43ca-bebc-85bfdf640d38
api_name:
- SMC_SFSELECTITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cfb3384fcfff73d264d21c53a91ede554cc7da5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967964"
---
# <a name="smc_sfselectitem-message"></a><span data-ttu-id="038ae-103">Mensagem do SMC \_ SFSELECTITEM</span><span class="sxs-lookup"><span data-stu-id="038ae-103">SMC\_SFSELECTITEM message</span></span>

<span data-ttu-id="038ae-104">O usuário selecionou o item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="038ae-104">The user has selected the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFSELECTITEM
            
```



## <a name="parameters"></a><span data-ttu-id="038ae-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="038ae-105">Parameters</span></span>

<span data-ttu-id="038ae-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="038ae-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="038ae-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="038ae-107">Return value</span></span>

<span data-ttu-id="038ae-108">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="038ae-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="038ae-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="038ae-109">Remarks</span></span>

<span data-ttu-id="038ae-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="038ae-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="038ae-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="038ae-111">Requirements</span></span>



| <span data-ttu-id="038ae-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="038ae-112">Requirement</span></span> | <span data-ttu-id="038ae-113">Valor</span><span class="sxs-lookup"><span data-stu-id="038ae-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="038ae-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="038ae-114">Minimum supported client</span></span><br/> | <span data-ttu-id="038ae-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="038ae-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="038ae-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="038ae-116">Minimum supported server</span></span><br/> | <span data-ttu-id="038ae-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="038ae-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="038ae-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="038ae-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="038ae-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="038ae-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="038ae-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="038ae-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="038ae-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="038ae-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




