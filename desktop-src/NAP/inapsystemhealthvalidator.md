---
title: Interface INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Deve ser implementado por desenvolvedores de SHV para permitir que o sistema NAP se comunique com um SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- INapSystemHealthValidator da interface NAP
- INapSystemHealthValidator interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644500"
---
# <a name="inapsystemhealthvalidator-interface"></a><span data-ttu-id="67cd4-105">Interface INapSystemHealthValidator</span><span class="sxs-lookup"><span data-stu-id="67cd4-105">INapSystemHealthValidator interface</span></span>

> [!Note]  
> <span data-ttu-id="67cd4-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="67cd4-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="67cd4-107">O **INapSystemHealthValidator** fornece métodos que devem ser implementados por desenvolvedores de SHV para permitir que o sistema NAP se comunique com um SHV.</span><span class="sxs-lookup"><span data-stu-id="67cd4-107">The **INapSystemHealthValidator** provides methods that must be implemented by SHV developers to enable the NAP system to communicate with an SHV.</span></span>

## <a name="members"></a><span data-ttu-id="67cd4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="67cd4-108">Members</span></span>

<span data-ttu-id="67cd4-109">A interface **INapSystemHealthValidator** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="67cd4-109">The **INapSystemHealthValidator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67cd4-110">**INapSystemHealthValidator** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="67cd4-110">**INapSystemHealthValidator** also has these types of members:</span></span>

-   [<span data-ttu-id="67cd4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="67cd4-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67cd4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="67cd4-112">Methods</span></span>

<span data-ttu-id="67cd4-113">A interface **INapSystemHealthValidator** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="67cd4-113">The **INapSystemHealthValidator** interface has these methods.</span></span>



| <span data-ttu-id="67cd4-114">Método</span><span class="sxs-lookup"><span data-stu-id="67cd4-114">Method</span></span>                                                                                   | <span data-ttu-id="67cd4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="67cd4-115">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67cd4-116">**INapSystemHealthValidator:: Validate**</span><span class="sxs-lookup"><span data-stu-id="67cd4-116">**INapSystemHealthValidator::Validate**</span></span>](inapsystemhealthvalidator-validate-method.md) | <span data-ttu-id="67cd4-117">O sistema NAP chama esse método definido pelo aplicativo para validar o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recebido de um cliente.</span><span class="sxs-lookup"><span data-stu-id="67cd4-117">The NAP system calls this application defined method to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="67cd4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67cd4-118">Requirements</span></span>



| <span data-ttu-id="67cd4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="67cd4-119">Requirement</span></span> | <span data-ttu-id="67cd4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="67cd4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67cd4-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67cd4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67cd4-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="67cd4-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="67cd4-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67cd4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67cd4-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67cd4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67cd4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67cd4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="67cd4-126"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="67cd4-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="67cd4-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="67cd4-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67cd4-128"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67cd4-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67cd4-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="67cd4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67cd4-130">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="67cd4-130">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="67cd4-131">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="67cd4-131">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

