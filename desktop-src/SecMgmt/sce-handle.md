---
description: O tipo de dados de identificador do SCE \_ é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança. Ele é usado pelas informações de consulta do PFSCE \_ \_ e pelas funções de \_ suporte do PFSCE Set \_ info para passar informações entre o anexo e o banco de dados de segurança.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090183"
---
# <a name="sce_handle"></a><span data-ttu-id="6746b-104">identificador do SCE \_</span><span class="sxs-lookup"><span data-stu-id="6746b-104">SCE\_HANDLE</span></span>

<span data-ttu-id="6746b-105">O tipo de dados de **\_ identificador do SCE** é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="6746b-105">The **SCE\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="6746b-106">Ele é usado pelas [**\_ \_ informações de consulta do PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e pelas funções de suporte do [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) para passar informações entre o anexo e o banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="6746b-106">It is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support functions to pass information between the attachment and the security database.</span></span>


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="6746b-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6746b-107">Requirements</span></span>



| <span data-ttu-id="6746b-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="6746b-108">Requirement</span></span> | <span data-ttu-id="6746b-109">Valor</span><span class="sxs-lookup"><span data-stu-id="6746b-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6746b-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6746b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6746b-111">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6746b-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6746b-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6746b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6746b-113">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6746b-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6746b-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6746b-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="6746b-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="6746b-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6746b-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6746b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6746b-117">**\_informações de consulta do PFSCE \_**</span><span class="sxs-lookup"><span data-stu-id="6746b-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[<span data-ttu-id="6746b-118">**PFSCE \_ definir \_ informações**</span><span class="sxs-lookup"><span data-stu-id="6746b-118">**PFSCE\_SET\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

