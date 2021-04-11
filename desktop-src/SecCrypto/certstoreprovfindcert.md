---
description: Enumera ou localiza o primeiro certificado ou próximo em um repositório externo que corresponda aos critérios especificados.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Função de retorno de chamada CertStoreProvFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297064"
---
# <a name="certstoreprovfindcert-callback-function"></a><span data-ttu-id="95f15-103">Função de retorno de chamada CertStoreProvFindCert</span><span class="sxs-lookup"><span data-stu-id="95f15-103">CertStoreProvFindCert callback function</span></span>

<span data-ttu-id="95f15-104">A função de retorno de chamada **CertStoreProvFindCert** enumera ou localiza o primeiro ou próximo certificado em um [*repositório externo*](../secgloss/e-gly.md) que corresponde aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="95f15-104">The **CertStoreProvFindCert** callback function enumerates or finds the first or next certificate in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95f15-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a><span data-ttu-id="95f15-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95f15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95f15-107">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95f15-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f15-108">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="95f15-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="95f15-109">*pFindInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95f15-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f15-110">Um ponteiro para uma [**loja de certificados \_ \_ Prov \_ encontrar \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) a estrutura de informações contendo todos os parâmetros passados para a função [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .</span><span class="sxs-lookup"><span data-stu-id="95f15-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="95f15-111">*pPrevCertContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95f15-111">*pPrevCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f15-112">Um ponteiro para um [**\_ contexto CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) do certificado encontrado.</span><span class="sxs-lookup"><span data-stu-id="95f15-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) of the certificate found.</span></span> <span data-ttu-id="95f15-113">Na primeira chamada para a função, esse parâmetro deve ser definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="95f15-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="95f15-114">Em chamadas subsequentes, ele deve ser definido como o ponteiro retornado no parâmetro *ppProvCertContext* na última chamada.</span><span class="sxs-lookup"><span data-stu-id="95f15-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCertContext* parameter on the last call.</span></span> <span data-ttu-id="95f15-115">Um ponteiro não **nulo** passado nesse parâmetro é liberado pela função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="95f15-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="95f15-116">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95f15-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f15-117">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="95f15-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="95f15-118">*ppvStoreProvFindInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="95f15-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95f15-119">Um ponteiro para um ponteiro para um buffer para retornar as informações do provedor de repositório.</span><span class="sxs-lookup"><span data-stu-id="95f15-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="95f15-120">Opcionalmente, o retorno de chamada pode retornar um ponteiro para informações de localização internas nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="95f15-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="95f15-121">Após a primeira chamada, esse parâmetro é definido como o ponteiro retornado pela chamada anterior para a função.</span><span class="sxs-lookup"><span data-stu-id="95f15-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="95f15-122">*ppProvCertContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95f15-122">*ppProvCertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95f15-123">Em uma localização bem-sucedida, um ponteiro para o certificado encontrado é retornado nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="95f15-123">On a successful find, a pointer to the certificate found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95f15-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95f15-124">Return value</span></span>

<span data-ttu-id="95f15-125">Retornará **true** se a função for bem-sucedida ou **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="95f15-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="95f15-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95f15-126">Requirements</span></span>



| <span data-ttu-id="95f15-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="95f15-127">Requirement</span></span> | <span data-ttu-id="95f15-128">Valor</span><span class="sxs-lookup"><span data-stu-id="95f15-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95f15-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95f15-129">Minimum supported client</span></span><br/> | <span data-ttu-id="95f15-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="95f15-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="95f15-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95f15-131">Minimum supported server</span></span><br/> | <span data-ttu-id="95f15-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95f15-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95f15-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="95f15-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f15-134">**contexto do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="95f15-134">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="95f15-135">**informações de localização do repositório de certificados \_ \_ Prov \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95f15-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="95f15-136">**CertFindCertificateInStore**</span><span class="sxs-lookup"><span data-stu-id="95f15-136">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
