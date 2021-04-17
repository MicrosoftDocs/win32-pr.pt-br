---
description: Especifica permissões de controle de acesso para um arquivo em um cartão inteligente.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Enumeração de CARD_FILE_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783242"
---
# <a name="card_file_access_condition-enumeration"></a><span data-ttu-id="51539-103">\_Enumeração de \_ condição de acesso do arquivo de cartão \_</span><span class="sxs-lookup"><span data-stu-id="51539-103">CARD\_FILE\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="51539-104">A **enumeração \_ \_ \_ condição de acesso ao arquivo do cartão** especifica permissões de controle de acesso para um arquivo em um [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="51539-104">The **CARD\_FILE\_ACCESS\_CONDITION** enumeration specifies access control permissions for a file on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="51539-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51539-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="51539-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="51539-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="51539-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="51539-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="51539-108">Esse valor não é válido.</span><span class="sxs-lookup"><span data-stu-id="51539-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="51539-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span><span class="sxs-lookup"><span data-stu-id="51539-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="51539-110">Todos podem ler o arquivo.</span><span class="sxs-lookup"><span data-stu-id="51539-110">Everyone can read the file.</span></span> <span data-ttu-id="51539-111">Usuários específicos podem gravar no arquivo.</span><span class="sxs-lookup"><span data-stu-id="51539-111">Specific users can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="51539-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span><span class="sxs-lookup"><span data-stu-id="51539-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span></span>
</dt> <dd>

<span data-ttu-id="51539-113">Somente usuários específicos podem ler ou gravar no arquivo.</span><span class="sxs-lookup"><span data-stu-id="51539-113">Only specific users can read or write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="51539-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span><span class="sxs-lookup"><span data-stu-id="51539-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="51539-115">Todos podem ler o arquivo.</span><span class="sxs-lookup"><span data-stu-id="51539-115">Everyone can read the file.</span></span> <span data-ttu-id="51539-116">Os administradores podem gravar no arquivo.</span><span class="sxs-lookup"><span data-stu-id="51539-116">Administrators can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="51539-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span><span class="sxs-lookup"><span data-stu-id="51539-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span></span>
</dt> <dd>

<span data-ttu-id="51539-118">As permissões de acesso para o arquivo são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="51539-118">Access permissions for the file are unknown.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51539-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51539-119">Requirements</span></span>



| <span data-ttu-id="51539-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="51539-120">Requirement</span></span> | <span data-ttu-id="51539-121">Valor</span><span class="sxs-lookup"><span data-stu-id="51539-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51539-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51539-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51539-123">\[Somente aplicativos da área de trabalho do Windows XP, Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="51539-123">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="51539-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51539-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51539-125">Somente aplicativos de área de trabalho do Windows Server 2003, Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="51539-125">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="51539-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51539-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="51539-127"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="51539-127"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51539-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="51539-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51539-129">Provedor de serviços de criptografia de cartão inteligente base da Microsoft</span><span class="sxs-lookup"><span data-stu-id="51539-129">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="51539-130">**\_informações do arquivo de cartão \_**</span><span class="sxs-lookup"><span data-stu-id="51539-130">**CARD\_FILE\_INFO**</span></span>](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[<span data-ttu-id="51539-131">**CardCreateFile**</span><span class="sxs-lookup"><span data-stu-id="51539-131">**CardCreateFile**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
