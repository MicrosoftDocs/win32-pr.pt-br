---
description: Recupera uma propriedade especificada de uma CTL (lista de certificados confiáveis).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Função de retorno de chamada CertStoreProvGetCTLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748396"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a><span data-ttu-id="7e78c-103">Função de retorno de chamada CertStoreProvGetCTLProperty</span><span class="sxs-lookup"><span data-stu-id="7e78c-103">CertStoreProvGetCTLProperty callback function</span></span>

<span data-ttu-id="7e78c-104">A função de retorno de chamada **CertStoreProvGetCTLProperty** recupera uma propriedade especificada de uma CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="7e78c-104">The **CertStoreProvGetCTLProperty** callback function retrieves a specified property of a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e78c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e78c-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="7e78c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e78c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e78c-107">*hStoreProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e78c-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e78c-108">Um identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7e78c-108">A **HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e78c-109">*pCtlContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e78c-109">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e78c-110">Um ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="7e78c-110">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e78c-111">*dwPropId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e78c-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e78c-112">Indica um identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7e78c-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7e78c-113">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e78c-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e78c-114">Quaisquer valores de sinalizador necessários.</span><span class="sxs-lookup"><span data-stu-id="7e78c-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="7e78c-115">*pvData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7e78c-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e78c-116">Um ponteiro para um buffer que contém o ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) a ser retornada pela função.</span><span class="sxs-lookup"><span data-stu-id="7e78c-116">A pointer to a buffer to contain the pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure to be returned by the function.</span></span> <span data-ttu-id="7e78c-117">Para obter o valor de *pcbData* antes de alocar memória para o buffer, esse parâmetro pode ser definido como **NULL** em uma primeira chamada para a função.</span><span class="sxs-lookup"><span data-stu-id="7e78c-117">To get the value of *pcbData* before allocating memory for the buffer, this parameter can be set to **NULL** on a first call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="7e78c-118">*pcbData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7e78c-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e78c-119">Um ponteiro para um **DWORD** que indica o comprimento do buffer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="7e78c-119">A pointer to a **DWORD** that indicates the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e78c-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e78c-120">Return value</span></span>

<span data-ttu-id="7e78c-121">Se a função for realizada com sucesso, a função retornará diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7e78c-121">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="7e78c-122">Se a função falhar, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7e78c-122">If the function fails, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e78c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e78c-123">Requirements</span></span>



| <span data-ttu-id="7e78c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e78c-124">Requirement</span></span> | <span data-ttu-id="7e78c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7e78c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e78c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e78c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7e78c-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7e78c-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7e78c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e78c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7e78c-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e78c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e78c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e78c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e78c-131">**contexto de CTL \_**</span><span class="sxs-lookup"><span data-stu-id="7e78c-131">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
