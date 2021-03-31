---
description: Um tipo de dados opaco.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169695"
---
# <a name="plsa_client_request"></a><span data-ttu-id="07afe-103">\_solicitação de cliente PLSA \_</span><span class="sxs-lookup"><span data-stu-id="07afe-103">PLSA\_CLIENT\_REQUEST</span></span>

<span data-ttu-id="07afe-104">O tipo de dados de **\_ \_ solicitação do cliente PLSA** é um tipo de dados opaco.</span><span class="sxs-lookup"><span data-stu-id="07afe-104">The **PLSA\_CLIENT\_REQUEST** data type is an opaque data type.</span></span>

<span data-ttu-id="07afe-105">A [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) a usa internamente para manter as informações do cliente relacionadas a solicitações individuais.</span><span class="sxs-lookup"><span data-stu-id="07afe-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) uses it internally to maintain client information related to individual requests.</span></span>


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a><span data-ttu-id="07afe-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07afe-106">Requirements</span></span>



| <span data-ttu-id="07afe-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="07afe-107">Requirement</span></span> | <span data-ttu-id="07afe-108">Valor</span><span class="sxs-lookup"><span data-stu-id="07afe-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07afe-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07afe-109">Minimum supported client</span></span><br/> | <span data-ttu-id="07afe-110">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="07afe-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="07afe-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07afe-111">Minimum supported server</span></span><br/> | <span data-ttu-id="07afe-112">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07afe-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07afe-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07afe-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="07afe-114"><dt>Ntsecpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="07afe-114"><dt>Ntsecpkg.h</dt></span></span> </dl> |



 

 
