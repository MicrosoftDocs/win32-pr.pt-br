---
description: Enumera ou localiza a primeira ou a próxima CRL em um repositório externo que corresponde aos critérios especificados.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Função de retorno de chamada CertStoreProvFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506080"
---
# <a name="certstoreprovfindcrl-callback-function"></a><span data-ttu-id="ad68d-103">Função de retorno de chamada CertStoreProvFindCRL</span><span class="sxs-lookup"><span data-stu-id="ad68d-103">CertStoreProvFindCRL callback function</span></span>

<span data-ttu-id="ad68d-104">A função de retorno de chamada **CertStoreProvFindCRL** enumera ou localiza a primeira ou a próxima [*CRL*](../secgloss/c-gly.md) em um [*repositório*](../secgloss/e-gly.md) externo que corresponde aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="ad68d-104">The **CertStoreProvFindCRL** callback function enumerates or finds the first or next [*CRL*](../secgloss/c-gly.md) in an external [*store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad68d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad68d-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
);
```



## <a name="parameters"></a><span data-ttu-id="ad68d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad68d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad68d-107">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad68d-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad68d-108">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ad68d-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad68d-109">*pFindInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad68d-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad68d-110">Um ponteiro para uma [**loja de certificados \_ \_ Prov \_ encontrar \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) a estrutura de informações contendo todos os parâmetros passados para a função [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .</span><span class="sxs-lookup"><span data-stu-id="ad68d-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="ad68d-111">*pPrevCrlContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad68d-111">*pPrevCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad68d-112">Um ponteiro para uma estrutura de [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) da última CRL encontrada.</span><span class="sxs-lookup"><span data-stu-id="ad68d-112">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure of the last CRL found.</span></span> <span data-ttu-id="ad68d-113">Na primeira chamada para a função, esse parâmetro deve ser definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ad68d-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="ad68d-114">Em chamadas subsequentes, ele deve ser definido como o ponteiro retornado no parâmetro *ppProvCRLContext* na última chamada.</span><span class="sxs-lookup"><span data-stu-id="ad68d-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCRLContext* parameter on the last call.</span></span> <span data-ttu-id="ad68d-115">Um ponteiro não **nulo** passado nesse parâmetro é liberado pela função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ad68d-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="ad68d-116">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad68d-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad68d-117">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="ad68d-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="ad68d-118">*ppvStoreProvFindInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ad68d-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad68d-119">Um ponteiro para um ponteiro para um buffer para retornar as informações do provedor de repositório.</span><span class="sxs-lookup"><span data-stu-id="ad68d-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="ad68d-120">Opcionalmente, o retorno de chamada pode retornar um ponteiro para informações de localização internas nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ad68d-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="ad68d-121">Após a primeira chamada, esse parâmetro é definido como o ponteiro retornado pela chamada anterior para a função.</span><span class="sxs-lookup"><span data-stu-id="ad68d-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="ad68d-122">*ppProvCrlContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ad68d-122">*ppProvCrlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad68d-123">Em uma localização bem-sucedida, um ponteiro para a CRL encontrada é retornado nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ad68d-123">On a successful find, a pointer to the CRL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad68d-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad68d-124">Return value</span></span>

<span data-ttu-id="ad68d-125">Retornará **true** se a função for bem-sucedida ou **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="ad68d-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad68d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad68d-126">Requirements</span></span>



| <span data-ttu-id="ad68d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad68d-127">Requirement</span></span> | <span data-ttu-id="ad68d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ad68d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad68d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad68d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ad68d-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ad68d-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ad68d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad68d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ad68d-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad68d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad68d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad68d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad68d-134">**informações de localização do repositório de certificados \_ \_ Prov \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad68d-134">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="ad68d-135">**CertFindCRLInStore**</span><span class="sxs-lookup"><span data-stu-id="ad68d-135">**CertFindCRLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[<span data-ttu-id="ad68d-136">**contexto de CRL \_**</span><span class="sxs-lookup"><span data-stu-id="ad68d-136">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
