---
description: Chamado quando o certificado retornado pelo retorno de chamada CertStoreProvFindCert não foi usado e, portanto, foi liberado em uma chamada subsequente para CertStoreProvFindCert.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Função de retorno de chamada CertStoreProvFreeFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755956"
---
# <a name="certstoreprovfreefindcert-callback-function"></a><span data-ttu-id="02432-103">Função de retorno de chamada CertStoreProvFreeFindCert</span><span class="sxs-lookup"><span data-stu-id="02432-103">CertStoreProvFreeFindCert callback function</span></span>

<span data-ttu-id="02432-104">A função de retorno de chamada **CertStoreProvFreeFindCert** é chamada quando o certificado retornado pelo retorno de chamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) não foi usado e, portanto, é liberado em uma chamada subsequente para **CertStoreProvFindCert**.</span><span class="sxs-lookup"><span data-stu-id="02432-104">The **CertStoreProvFreeFindCert** callback function is called when the certificate returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCert**.</span></span> <span data-ttu-id="02432-105">Antes que o retorno de chamada de fechamento seja chamado, todos os certificados retornados pelo retorno de chamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) devem ser liberados pelo provedor usando **CertStoreProvFindCert** ou **CertStoreProvFreeFindCert**.</span><span class="sxs-lookup"><span data-stu-id="02432-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback must be released by the provider using **CertStoreProvFindCert** or **CertStoreProvFreeFindCert**.</span></span>

## <a name="syntax"></a><span data-ttu-id="02432-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02432-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="02432-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02432-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02432-108">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02432-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02432-109">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="02432-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="02432-110">*pCertContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02432-110">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02432-111">Um ponteiro para um [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="02432-111">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="02432-112">*pvStoreProvFindInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02432-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02432-113">Um ponteiro para um buffer que contém informações de localização.</span><span class="sxs-lookup"><span data-stu-id="02432-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="02432-114">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02432-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02432-115">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="02432-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02432-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02432-116">Return value</span></span>

<span data-ttu-id="02432-117">Retornará **true** se a função for bem-sucedida ou **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="02432-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="02432-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02432-118">Requirements</span></span>



| <span data-ttu-id="02432-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="02432-119">Requirement</span></span> | <span data-ttu-id="02432-120">Valor</span><span class="sxs-lookup"><span data-stu-id="02432-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02432-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02432-121">Minimum supported client</span></span><br/> | <span data-ttu-id="02432-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="02432-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="02432-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02432-123">Minimum supported server</span></span><br/> | <span data-ttu-id="02432-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02432-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02432-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="02432-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02432-126">**contexto do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="02432-126">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="02432-127">**CertStoreProvFindCert**</span><span class="sxs-lookup"><span data-stu-id="02432-127">**CertStoreProvFindCert**</span></span>](certstoreprovfindcert.md)
</dt> </dl>

 

 
