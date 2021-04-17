---
description: Recupera uma propriedade especificada de um certificado.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Função de retorno de chamada CertStoreProvGetCertProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811289"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a><span data-ttu-id="3a24d-103">Função de retorno de chamada CertStoreProvGetCertProperty</span><span class="sxs-lookup"><span data-stu-id="3a24d-103">CertStoreProvGetCertProperty callback function</span></span>

<span data-ttu-id="3a24d-104">A função de retorno de chamada **CertStoreProvGetCertProperty** recupera uma propriedade especificada de um certificado.</span><span class="sxs-lookup"><span data-stu-id="3a24d-104">The **CertStoreProvGetCertProperty** callback function retrieves a specified property of a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a24d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a24d-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="3a24d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a24d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a24d-107">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-108">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3a24d-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-109">*pCertContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-109">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-110">Um ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="3a24d-110">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-111">*dwPropId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-112">Indica um identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3a24d-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-113">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-114">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="3a24d-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-115">*pvData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-116">Um ponteiro para um buffer que contém o ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) a ser retornada pela função.</span><span class="sxs-lookup"><span data-stu-id="3a24d-116">A pointer to a buffer to contain the pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure to be returned by the function.</span></span> <span data-ttu-id="3a24d-117">Pode ser definido como **NULL** em uma primeira chamada para a função para obter o valor de *pcbData* antes de alocar memória para o buffer.</span><span class="sxs-lookup"><span data-stu-id="3a24d-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-118">*pcbData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-119">Um ponteiro para um **DWORD** que indica o comprimento do buffer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="3a24d-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a24d-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a24d-120">Return value</span></span>

<span data-ttu-id="3a24d-121">Retornará **true** se a função for bem-sucedida ou **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="3a24d-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a24d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a24d-122">Requirements</span></span>



| <span data-ttu-id="3a24d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a24d-123">Requirement</span></span> | <span data-ttu-id="3a24d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3a24d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a24d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a24d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a24d-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3a24d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a24d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a24d-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a24d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a24d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a24d-130">**contexto do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="3a24d-130">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
