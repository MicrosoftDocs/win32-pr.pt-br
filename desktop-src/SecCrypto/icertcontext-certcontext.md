---
description: Define ou recupera o \_ contexto PCCERT de um certificado.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'Propriedade ICertContext:: CertContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783237"
---
# <a name="icertcontextcertcontext-property"></a><span data-ttu-id="e0cc1-103">Propriedade ICertContext:: CertContext</span><span class="sxs-lookup"><span data-stu-id="e0cc1-103">ICertContext::CertContext property</span></span>

<span data-ttu-id="e0cc1-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="e0cc1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="e0cc1-105">A propriedade **CertContext** define ou recupera o \_ contexto de PCCERT de um certificado.</span><span class="sxs-lookup"><span data-stu-id="e0cc1-105">The **CertContext** property sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="e0cc1-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e0cc1-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0cc1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0cc1-107">Syntax</span></span>


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a><span data-ttu-id="e0cc1-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e0cc1-108">Property value</span></span>

<span data-ttu-id="e0cc1-109">O \_ contexto PCCERT do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0cc1-109">The PCCERT\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0cc1-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e0cc1-110">Error codes</span></span>

<span data-ttu-id="e0cc1-111">Se os métodos de acesso à propriedade **colocarem \_ CertContext** e o **\_ CertContext** forem bem-sucedidos, eles retornarão S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0cc1-111">If the property access methods **put\_CertContext** and **get\_CertContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="e0cc1-112">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="e0cc1-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0cc1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0cc1-113">Remarks</span></span>

<span data-ttu-id="e0cc1-114">Você deve chamar o método [**FreeContext**](icertcontext-freecontext.md) ou a função [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) para liberar o contexto.</span><span class="sxs-lookup"><span data-stu-id="e0cc1-114">You must call either the [**FreeContext**](icertcontext-freecontext.md) method or the [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) function to free the context.</span></span>

<span data-ttu-id="e0cc1-115">Se você definir a propriedade **CertContext** , o estado do objeto de [**certificado**](certificate.md) inteiro será redefinido.</span><span class="sxs-lookup"><span data-stu-id="e0cc1-115">If you set the **CertContext** property, the state of the entire [**Certificate**](certificate.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0cc1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0cc1-116">Requirements</span></span>



| <span data-ttu-id="e0cc1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0cc1-117">Requirement</span></span> | <span data-ttu-id="e0cc1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e0cc1-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0cc1-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e0cc1-119">Redistributable</span></span><br/> | <span data-ttu-id="e0cc1-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0cc1-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e0cc1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e0cc1-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="e0cc1-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0cc1-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0cc1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0cc1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0cc1-124">**ICertContext**</span><span class="sxs-lookup"><span data-stu-id="e0cc1-124">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




