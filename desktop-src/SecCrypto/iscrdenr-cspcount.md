---
description: Recupera o número de CSPs (provedores de serviços de criptografia).
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: 'Propriedade ISCrdEnr:: CSPCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297352"
---
# <a name="iscrdenrcspcount-property"></a><span data-ttu-id="03ed3-103">Propriedade ISCrdEnr:: CSPCount</span><span class="sxs-lookup"><span data-stu-id="03ed3-103">ISCrdEnr::CSPCount property</span></span>

<span data-ttu-id="03ed3-104">A propriedade **CSPCount** recupera o número de CSPs ( [*provedores de serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="03ed3-104">The **CSPCount** property retrieves the number of [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

<span data-ttu-id="03ed3-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="03ed3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ed3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03ed3-106">Syntax</span></span>


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="03ed3-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="03ed3-107">Property value</span></span>

<span data-ttu-id="03ed3-108">O número de CSPs.</span><span class="sxs-lookup"><span data-stu-id="03ed3-108">The number of CSPs.</span></span>

## <a name="error-codes"></a><span data-ttu-id="03ed3-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="03ed3-109">Error codes</span></span>

<span data-ttu-id="03ed3-110">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="03ed3-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="03ed3-111">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="03ed3-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="03ed3-112">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="03ed3-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03ed3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03ed3-113">Requirements</span></span>



| <span data-ttu-id="03ed3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ed3-114">Requirement</span></span> | <span data-ttu-id="03ed3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="03ed3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03ed3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03ed3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03ed3-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="03ed3-117">None supported</span></span><br/>                                                               |
| <span data-ttu-id="03ed3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03ed3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03ed3-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03ed3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03ed3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="03ed3-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03ed3-121"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03ed3-121"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="03ed3-122">IID</span><span class="sxs-lookup"><span data-stu-id="03ed3-122">IID</span></span><br/>                      | <span data-ttu-id="03ed3-123">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="03ed3-123">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="03ed3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="03ed3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ed3-125">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="03ed3-125">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="03ed3-126">**ISCrdEnr:: CSPName**</span><span class="sxs-lookup"><span data-stu-id="03ed3-126">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> <dt>

[<span data-ttu-id="03ed3-127">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="03ed3-127">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
