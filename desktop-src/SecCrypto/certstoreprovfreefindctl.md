---
description: Chamado quando o certificado retornado pelo retorno de chamada CertStoreProvFindCTL não foi usado e, portanto, foi liberado em uma chamada subsequente para CertStoreProvFindCTL.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Função de retorno de chamada CertStoreProvFreeFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784153"
---
# <a name="certstoreprovfreefindctl-callback-function"></a><span data-ttu-id="d11b5-103">Função de retorno de chamada CertStoreProvFreeFindCTL</span><span class="sxs-lookup"><span data-stu-id="d11b5-103">CertStoreProvFreeFindCTL callback function</span></span>

<span data-ttu-id="d11b5-104">A função de retorno de chamada **CertStoreProvFreeFindCTL** é chamada quando o certificado retornado pelo retorno de chamada [**CertStoreProvFindCTL**](certstoreprovfindctl.md) não foi usado e, portanto, é liberado em uma chamada subsequente para **CertStoreProvFindCTL**.</span><span class="sxs-lookup"><span data-stu-id="d11b5-104">The **CertStoreProvFreeFindCTL** callback function is called when the certificate returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCTL**.</span></span> <span data-ttu-id="d11b5-105">Antes que o retorno de chamada de fechamento seja chamado, todos os certificados retornados pelo retorno de chamada [**CertStoreProvFindCTL**](certstoreprovfindctl.md) devem ser liberados pelo provedor usando **CertStoreProvFindCTL** ou **CertStoreProvFreeFindCTL**.</span><span class="sxs-lookup"><span data-stu-id="d11b5-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback must be released by the provider using **CertStoreProvFindCTL** or **CertStoreProvFreeFindCTL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11b5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d11b5-106">Syntax</span></span>


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d11b5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d11b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d11b5-108">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d11b5-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d11b5-109">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d11b5-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d11b5-110">*pCtlContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d11b5-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d11b5-111">Um ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="d11b5-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d11b5-112">*pvStoreProvFindInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d11b5-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d11b5-113">Um ponteiro para um buffer que contém informações de localização.</span><span class="sxs-lookup"><span data-stu-id="d11b5-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="d11b5-114">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d11b5-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d11b5-115">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="d11b5-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d11b5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d11b5-116">Return value</span></span>

<span data-ttu-id="d11b5-117">Retornará **true** se a função for bem-sucedida ou **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="d11b5-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="d11b5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d11b5-118">Requirements</span></span>



| <span data-ttu-id="d11b5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d11b5-119">Requirement</span></span> | <span data-ttu-id="d11b5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d11b5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d11b5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d11b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d11b5-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d11b5-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d11b5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d11b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d11b5-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d11b5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d11b5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d11b5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d11b5-126">**CertStoreProvFindCTL**</span><span class="sxs-lookup"><span data-stu-id="d11b5-126">**CertStoreProvFindCTL**</span></span>](certstoreprovfindctl.md)
</dt> <dt>

[<span data-ttu-id="d11b5-127">**contexto de CTL \_**</span><span class="sxs-lookup"><span data-stu-id="d11b5-127">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
