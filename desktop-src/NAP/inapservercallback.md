---
title: Interface INapServerCallback (NapSystemHealthValidator. h)
description: Os SHVs usam para sinalizar a conclusão da solicitação assíncrona.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- INapServerCallback da interface NAP
- INapServerCallback interface NAP, descrita
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454663"
---
# <a name="inapservercallback-interface"></a><span data-ttu-id="66f94-105">Interface INapServerCallback</span><span class="sxs-lookup"><span data-stu-id="66f94-105">INapServerCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="66f94-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="66f94-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="66f94-107">O **INapServerCallback** fornece um método que os SHVs usam para sinalizar a conclusão da solicitação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="66f94-107">The **INapServerCallback** provides a method that SHVs use to signal asynchronous request completion.</span></span>

## <a name="members"></a><span data-ttu-id="66f94-108">Membros</span><span class="sxs-lookup"><span data-stu-id="66f94-108">Members</span></span>

<span data-ttu-id="66f94-109">A interface **INapServerCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="66f94-109">The **INapServerCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="66f94-110">**INapServerCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="66f94-110">**INapServerCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="66f94-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="66f94-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="66f94-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="66f94-112">Methods</span></span>

<span data-ttu-id="66f94-113">A interface **INapServerCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="66f94-113">The **INapServerCallback** interface has these methods.</span></span>



| <span data-ttu-id="66f94-114">Método</span><span class="sxs-lookup"><span data-stu-id="66f94-114">Method</span></span>                                                                         | <span data-ttu-id="66f94-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="66f94-115">Description</span></span>                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="66f94-116">**INapServerCallback:: OnComplete**</span><span class="sxs-lookup"><span data-stu-id="66f94-116">**INapServerCallback::OnComplete**</span></span>](inapservercallback-oncomplete-method.md) | <span data-ttu-id="66f94-117">Usado por SHVs para sinalizar a conclusão da solicitação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="66f94-117">Used by SHVs to signal asynchronous request completion.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="66f94-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f94-118">Requirements</span></span>



| <span data-ttu-id="66f94-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f94-119">Requirement</span></span> | <span data-ttu-id="66f94-120">Valor</span><span class="sxs-lookup"><span data-stu-id="66f94-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f94-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66f94-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66f94-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="66f94-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="66f94-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66f94-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66f94-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66f94-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66f94-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66f94-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="66f94-126"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f94-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="66f94-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="66f94-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66f94-128"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66f94-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="66f94-129">DLL</span><span class="sxs-lookup"><span data-stu-id="66f94-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66f94-130"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66f94-130"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="66f94-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="66f94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f94-132">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="66f94-132">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="66f94-133">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="66f94-133">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

