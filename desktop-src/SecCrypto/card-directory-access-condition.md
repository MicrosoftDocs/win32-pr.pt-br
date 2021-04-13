---
description: Especifica permissões de controle de acesso para um diretório em um cartão inteligente.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Enumeração de CARD_DIRECTORY_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164405"
---
# <a name="card_directory_access_condition-enumeration"></a><span data-ttu-id="ac542-103">\_Enumeração de \_ condição de acesso ao diretório de cartão \_</span><span class="sxs-lookup"><span data-stu-id="ac542-103">CARD\_DIRECTORY\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="ac542-104">A **enumeração \_ \_ \_ condição de acesso ao diretório de cartão** especifica permissões de controle de acesso para um diretório em um [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ac542-104">The **CARD\_DIRECTORY\_ACCESS\_CONDITION** enumeration specifies access control permissions for a directory on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac542-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac542-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="ac542-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ac542-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ac542-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="ac542-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="ac542-108">Esse valor não é válido.</span><span class="sxs-lookup"><span data-stu-id="ac542-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ac542-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="ac542-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="ac542-110">Usuários específicos podem ler, gravar e excluir o diretório.</span><span class="sxs-lookup"><span data-stu-id="ac542-110">Specific users can read, write, and delete the directory.</span></span>

</dd> <dt>

<span data-ttu-id="ac542-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="ac542-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="ac542-112">Os administradores podem ler, gravar e excluir o diretório.</span><span class="sxs-lookup"><span data-stu-id="ac542-112">Administrators can read, write, and delete the directory.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac542-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac542-113">Requirements</span></span>



| <span data-ttu-id="ac542-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac542-114">Requirement</span></span> | <span data-ttu-id="ac542-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ac542-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac542-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac542-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ac542-117">\[Somente aplicativos da área de trabalho do Windows XP, Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ac542-117">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ac542-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac542-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ac542-119">Somente aplicativos de área de trabalho do Windows Server 2003, Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac542-119">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="ac542-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac542-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac542-121"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac542-121"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac542-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac542-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac542-123">Provedor de serviços de criptografia de cartão inteligente base da Microsoft</span><span class="sxs-lookup"><span data-stu-id="ac542-123">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="ac542-124">**CardCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="ac542-124">**CardCreateDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[<span data-ttu-id="ac542-125">**CardDeleteDirectory**</span><span class="sxs-lookup"><span data-stu-id="ac542-125">**CardDeleteDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
