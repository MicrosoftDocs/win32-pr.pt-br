---
description: O \_ tipo de dados do identificador KEYSVCC define um identificador de serviço de chave. Um \_ identificador de identificador KEYSVCC é usado pelas funções RKeyOpenKeyService e RKeyCloseKeyService.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1427a4ffd4637e073e517e5df54af72191992d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811791"
---
# <a name="keysvcc_handle"></a><span data-ttu-id="26324-104">identificador de KEYSVCC \_</span><span class="sxs-lookup"><span data-stu-id="26324-104">KEYSVCC\_HANDLE</span></span>

<span data-ttu-id="26324-105">O tipo de dados do **\_ identificador KEYSVCC** define um identificador de serviço de chave.</span><span class="sxs-lookup"><span data-stu-id="26324-105">The **KEYSVCC\_HANDLE** data type defines a key service handle.</span></span> <span data-ttu-id="26324-106">Um identificador de **\_ identificador KEYSVCC** é usado pelas funções [**RKeyOpenKeyService**](rkeyopenkeyservice.md) e [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="26324-106">A **KEYSVCC\_HANDLE** handle is used by the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) and [**RKeyCloseKeyService**](rkeyclosekeyservice.md) functions.</span></span>


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="26324-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26324-107">Requirements</span></span>



| <span data-ttu-id="26324-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="26324-108">Requirement</span></span> | <span data-ttu-id="26324-109">Valor</span><span class="sxs-lookup"><span data-stu-id="26324-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26324-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26324-110">Minimum supported client</span></span><br/> | <span data-ttu-id="26324-111">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="26324-111">None supported</span></span><br/>                                                             |
| <span data-ttu-id="26324-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26324-112">Minimum supported server</span></span><br/> | <span data-ttu-id="26324-113">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26324-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26324-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26324-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="26324-115"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="26324-115"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26324-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="26324-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26324-117">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="26324-117">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="26324-118">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="26324-118">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




