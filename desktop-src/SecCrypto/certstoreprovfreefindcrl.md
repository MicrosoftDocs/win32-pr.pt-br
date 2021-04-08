---
description: Chamado quando o certificado retornado pelo retorno de chamada CertStoreProvFindCRL não foi usado e, portanto, foi liberado em uma chamada subsequente para CertStoreProvFindCRL.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Função de retorno de chamada CertStoreProvFreeFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829414"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a><span data-ttu-id="a63c9-103">Função de retorno de chamada CertStoreProvFreeFindCRL</span><span class="sxs-lookup"><span data-stu-id="a63c9-103">CertStoreProvFreeFindCRL callback function</span></span>

<span data-ttu-id="a63c9-104">A função de retorno de chamada **CertStoreProvFreeFindCRL** é chamada quando o certificado retornado pelo retorno de chamada [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) não foi usado e, portanto, é liberado em uma chamada subsequente para **CertStoreProvFindCRL**.</span><span class="sxs-lookup"><span data-stu-id="a63c9-104">The **CertStoreProvFreeFindCRL** callback function is called when the certificate returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCRL**.</span></span> <span data-ttu-id="a63c9-105">Antes que o retorno de chamada de fechamento seja chamado, todos os certificados retornados pelo retorno de chamada [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) devem ser liberados pelo provedor usando **CertStoreProvFindCRL** ou **CertStoreProvFreeFindCRL**.</span><span class="sxs-lookup"><span data-stu-id="a63c9-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback must be released by the provider using **CertStoreProvFindCRL** or **CertStoreProvFreeFindCRL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a63c9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a63c9-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a63c9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a63c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a63c9-108">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a63c9-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a63c9-109">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a63c9-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a63c9-110">*pCrlContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a63c9-110">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a63c9-111">Um ponteiro para um [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="a63c9-111">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="a63c9-112">*pvStoreProvFindInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a63c9-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a63c9-113">Um ponteiro para um buffer que contém informações de localização.</span><span class="sxs-lookup"><span data-stu-id="a63c9-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="a63c9-114">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a63c9-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a63c9-115">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="a63c9-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a63c9-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a63c9-116">Return value</span></span>

<span data-ttu-id="a63c9-117">Retornará **true** se a função for bem-sucedida ou **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="a63c9-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="a63c9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a63c9-118">Requirements</span></span>



| <span data-ttu-id="a63c9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a63c9-119">Requirement</span></span> | <span data-ttu-id="a63c9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a63c9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a63c9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a63c9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a63c9-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a63c9-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a63c9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a63c9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a63c9-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a63c9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a63c9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a63c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63c9-126">**CertStoreProvFindCRL**</span><span class="sxs-lookup"><span data-stu-id="a63c9-126">**CertStoreProvFindCRL**</span></span>](certstoreprovfindcrl.md)
</dt> <dt>

[<span data-ttu-id="a63c9-127">**contexto de CRL \_**</span><span class="sxs-lookup"><span data-stu-id="a63c9-127">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
