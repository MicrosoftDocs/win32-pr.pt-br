---
description: Recupera uma propriedade especificada de uma CRL.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Função de retorno de chamada CertStoreProvGetCRLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760391"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a><span data-ttu-id="2043f-103">Função de retorno de chamada CertStoreProvGetCRLProperty</span><span class="sxs-lookup"><span data-stu-id="2043f-103">CertStoreProvGetCRLProperty callback function</span></span>

<span data-ttu-id="2043f-104">A função de retorno de chamada **CertStoreProvGetCRLProperty** recupera uma propriedade especificada de uma [*CRL*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2043f-104">The **CertStoreProvGetCRLProperty** callback function retrieves a specified property of a [*CRL*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2043f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2043f-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="2043f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2043f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2043f-107">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2043f-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2043f-108">Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2043f-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2043f-109">*pCrlContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2043f-109">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2043f-110">Um ponteiro para uma estrutura de [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .</span><span class="sxs-lookup"><span data-stu-id="2043f-110">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2043f-111">*dwPropId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2043f-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2043f-112">Indica um identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="2043f-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2043f-113">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2043f-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2043f-114">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="2043f-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="2043f-115">*pvData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2043f-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2043f-116">Um ponteiro para um buffer que contém o ponteiro para uma estrutura de [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) a ser retornada pela função.</span><span class="sxs-lookup"><span data-stu-id="2043f-116">A pointer to a buffer to contain the pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure to be returned by the function.</span></span> <span data-ttu-id="2043f-117">Pode ser definido como **NULL** em uma primeira chamada para a função para obter o valor de *pcbData* antes de alocar memória para o buffer.</span><span class="sxs-lookup"><span data-stu-id="2043f-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2043f-118">*pcbData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2043f-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2043f-119">Um ponteiro para um **DWORD** que indica o comprimento do buffer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="2043f-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2043f-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2043f-120">Return value</span></span>

<span data-ttu-id="2043f-121">Retornará **true** se a função for bem-sucedida ou **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="2043f-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="2043f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2043f-122">Requirements</span></span>



| <span data-ttu-id="2043f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2043f-123">Requirement</span></span> | <span data-ttu-id="2043f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2043f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2043f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2043f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2043f-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2043f-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2043f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2043f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2043f-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2043f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2043f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2043f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2043f-130">**contexto de CRL \_**</span><span class="sxs-lookup"><span data-stu-id="2043f-130">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
