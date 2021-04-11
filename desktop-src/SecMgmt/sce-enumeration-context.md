---
description: O tipo de dados de contexto de enumeração do SCE \_ \_ é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança. Ele é usado pela função de \_ informações de consulta PFSCE \_ para navegar pelo banco de dados de segurança.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296272"
---
# <a name="sce_enumeration_context"></a><span data-ttu-id="cab31-104">\_contexto de enumeração do SCE \_</span><span class="sxs-lookup"><span data-stu-id="cab31-104">SCE\_ENUMERATION\_CONTEXT</span></span>

<span data-ttu-id="cab31-105">O tipo de dados de **\_ \_ contexto de enumeração do SCE** é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="cab31-105">The **SCE\_ENUMERATION\_CONTEXT** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="cab31-106">Ele é usado pela função [**de \_ \_ informações de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) para navegar pelo banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="cab31-106">It is used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a><span data-ttu-id="cab31-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cab31-107">Requirements</span></span>



| <span data-ttu-id="cab31-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="cab31-108">Requirement</span></span> | <span data-ttu-id="cab31-109">Valor</span><span class="sxs-lookup"><span data-stu-id="cab31-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cab31-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cab31-110">Minimum supported client</span></span><br/> | <span data-ttu-id="cab31-111">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cab31-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cab31-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cab31-112">Minimum supported server</span></span><br/> | <span data-ttu-id="cab31-113">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cab31-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cab31-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cab31-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="cab31-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="cab31-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab31-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="cab31-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab31-117">**\_informações de consulta do PFSCE \_**</span><span class="sxs-lookup"><span data-stu-id="cab31-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

