---
description: Libera um \_ contexto PCCERT adquirido por meio da propriedade CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'Método ICertContext:: FreeContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753401"
---
# <a name="icertcontextfreecontext-method"></a><span data-ttu-id="a1338-103">Método ICertContext:: FreeContext</span><span class="sxs-lookup"><span data-stu-id="a1338-103">ICertContext::FreeContext method</span></span>

<span data-ttu-id="a1338-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="a1338-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="a1338-105">O método **FreeContext** libera um \_ contexto PCCERT adquirido por meio da propriedade [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="a1338-105">The **FreeContext** method releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1338-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1338-106">Syntax</span></span>


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a><span data-ttu-id="a1338-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1338-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1338-108">*pCertContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a1338-108">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1338-109">O contexto de PCCERT \_ a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="a1338-109">The PCCERT\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1338-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1338-110">Return value</span></span>

<span data-ttu-id="a1338-111">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a1338-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a1338-112">Um valor de S \_ OK indica êxito.</span><span class="sxs-lookup"><span data-stu-id="a1338-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="a1338-113">Qualquer outro valor indica que a operação falhou.</span><span class="sxs-lookup"><span data-stu-id="a1338-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1338-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1338-114">Remarks</span></span>

<span data-ttu-id="a1338-115">Esse método não libera o contexto PCCERT \_ contido em um objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="a1338-115">This method does not release the PCCERT\_CONTEXT contained within a [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="a1338-116">Ele deve ser usado apenas para liberar um \_ contexto PCCERT adquirido por meio da propriedade [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="a1338-116">It should be used only to release a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1338-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1338-117">Requirements</span></span>



| <span data-ttu-id="a1338-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1338-118">Requirement</span></span> | <span data-ttu-id="a1338-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a1338-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1338-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a1338-120">Redistributable</span></span><br/> | <span data-ttu-id="a1338-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1338-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a1338-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a1338-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="a1338-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1338-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1338-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1338-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1338-125">**ICertContext**</span><span class="sxs-lookup"><span data-stu-id="a1338-125">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




