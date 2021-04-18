---
description: Enumera ou localiza a primeira ou a próxima CTL em um repositório externo que corresponde aos critérios especificados.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Função de retorno de chamada CertStoreProvFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756153"
---
# <a name="certstoreprovfindctl-callback-function"></a><span data-ttu-id="e76c8-103">Função de retorno de chamada CertStoreProvFindCTL</span><span class="sxs-lookup"><span data-stu-id="e76c8-103">CertStoreProvFindCTL callback function</span></span>

<span data-ttu-id="e76c8-104">A função de retorno de chamada **CertStoreProvFindCTL** enumera ou localiza a primeira ou a próxima [*CTL*](../secgloss/c-gly.md) em um [*repositório externo*](../secgloss/e-gly.md) que corresponde aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="e76c8-104">The **CertStoreProvFindCTL** callback function enumerates or finds the first or next [*CTL*](../secgloss/c-gly.md) in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="e76c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e76c8-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a><span data-ttu-id="e76c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e76c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e76c8-107">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e76c8-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76c8-108">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e76c8-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="e76c8-109">*pFindInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e76c8-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76c8-110">Um ponteiro para uma [**loja de certificados \_ \_ Prov \_ encontrar \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) a estrutura de informações contendo todos os parâmetros passados para o [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="e76c8-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span> <span data-ttu-id="e76c8-111">.</span><span class="sxs-lookup"><span data-stu-id="e76c8-111">function.</span></span>

</dd> <dt>

<span data-ttu-id="e76c8-112">*pPrevCtlContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e76c8-112">*pPrevCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76c8-113">Um ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) da última CTL encontrada.</span><span class="sxs-lookup"><span data-stu-id="e76c8-113">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure of the last CTL found.</span></span> <span data-ttu-id="e76c8-114">Na primeira chamada para a função, esse parâmetro deve ser definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e76c8-114">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="e76c8-115">Em chamadas subsequentes, ele deve ser definido como o ponteiro retornado no parâmetro *ppProvCTLContext* na última chamada.</span><span class="sxs-lookup"><span data-stu-id="e76c8-115">On subsequent calls, it should be set to the pointer returned in the *ppProvCTLContext* parameter on the last call.</span></span> <span data-ttu-id="e76c8-116">Um ponteiro não **nulo** passado nesse parâmetro é liberado pela função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e76c8-116">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="e76c8-117">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e76c8-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76c8-118">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="e76c8-118">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="e76c8-119">*ppvStoreProvFindInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e76c8-119">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e76c8-120">Um ponteiro para um ponteiro para o buffer para retornar as informações do provedor de repositório.</span><span class="sxs-lookup"><span data-stu-id="e76c8-120">A pointer to a pointer to buffer to return the store provider information.</span></span> <span data-ttu-id="e76c8-121">Opcionalmente, o retorno de chamada pode retornar um ponteiro para informações de localização internas nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e76c8-121">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="e76c8-122">Após a primeira chamada, esse parâmetro é definido como o ponteiro retornado pela chamada anterior para a função.</span><span class="sxs-lookup"><span data-stu-id="e76c8-122">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="e76c8-123">*ppProvCtlContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e76c8-123">*ppProvCtlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e76c8-124">Em uma localização bem-sucedida, um ponteiro para a CTL encontrada é retornado nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e76c8-124">On a successful find, a pointer to the CTL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e76c8-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e76c8-125">Return value</span></span>

<span data-ttu-id="e76c8-126">Retornará **true** se a função for bem-sucedida ou **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="e76c8-126">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="e76c8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e76c8-127">Requirements</span></span>



| <span data-ttu-id="e76c8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76c8-128">Requirement</span></span> | <span data-ttu-id="e76c8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e76c8-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e76c8-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e76c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e76c8-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e76c8-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e76c8-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e76c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e76c8-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e76c8-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e76c8-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e76c8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76c8-135">**informações de localização do repositório de certificados \_ \_ Prov \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e76c8-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="e76c8-136">**CertFindCTLInStore**</span><span class="sxs-lookup"><span data-stu-id="e76c8-136">**CertFindCTLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[<span data-ttu-id="e76c8-137">**contexto de CTL \_**</span><span class="sxs-lookup"><span data-stu-id="e76c8-137">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
