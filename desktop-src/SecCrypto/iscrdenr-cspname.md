---
description: Define ou recupera o nome do CSP (provedor de serviços de criptografia).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'Propriedade ISCrdEnr:: CSPName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011670"
---
# <a name="iscrdenrcspname-property"></a><span data-ttu-id="605ab-103">Propriedade ISCrdEnr:: CSPName</span><span class="sxs-lookup"><span data-stu-id="605ab-103">ISCrdEnr::CSPName property</span></span>

<span data-ttu-id="605ab-104">A propriedade **CSPName** define ou recupera o nome do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="605ab-104">The **CSPName** property sets or retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="605ab-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="605ab-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="605ab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="605ab-106">Syntax</span></span>


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="605ab-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="605ab-107">Property value</span></span>

<span data-ttu-id="605ab-108">O nome do CSP.</span><span class="sxs-lookup"><span data-stu-id="605ab-108">The name of the CSP.</span></span>

## <a name="error-codes"></a><span data-ttu-id="605ab-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="605ab-109">Error codes</span></span>

<span data-ttu-id="605ab-110">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="605ab-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="605ab-111">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="605ab-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="605ab-112">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="605ab-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="605ab-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="605ab-113">Remarks</span></span>

<span data-ttu-id="605ab-114">Defina essa propriedade para especificar o nome do CSP a ser usado com o controle de registro de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="605ab-114">Set this property to specify the name of the CSP to use with the Smart Card Enrollment Control.</span></span> <span data-ttu-id="605ab-115">Obtenha essa propriedade para recuperar o nome do CSP especificado.</span><span class="sxs-lookup"><span data-stu-id="605ab-115">Get this property to retrieve the name of the specified CSP.</span></span> <span data-ttu-id="605ab-116">Se você não especificar um valor para essa propriedade, a propriedade **CSPName** definirá como padrão o nome na lista de CSPs disponíveis.</span><span class="sxs-lookup"><span data-stu-id="605ab-116">If you do not specify a value for this property, the **CSPName** property defaults to the first name in the available list of CSPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="605ab-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="605ab-117">Requirements</span></span>



| <span data-ttu-id="605ab-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="605ab-118">Requirement</span></span> | <span data-ttu-id="605ab-119">Valor</span><span class="sxs-lookup"><span data-stu-id="605ab-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="605ab-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="605ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="605ab-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="605ab-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="605ab-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="605ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="605ab-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="605ab-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="605ab-124">DLL</span><span class="sxs-lookup"><span data-stu-id="605ab-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="605ab-125"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="605ab-125"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="605ab-126">IID</span><span class="sxs-lookup"><span data-stu-id="605ab-126">IID</span></span><br/>                      | <span data-ttu-id="605ab-127">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="605ab-127">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="605ab-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="605ab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605ab-129">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="605ab-129">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="605ab-130">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="605ab-130">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="605ab-131">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="605ab-131">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
