---
description: Define ou recupera o \_ \_ contexto de cadeia de PCCERT de um certificado.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'Propriedade IChainContext:: ChainContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761395"
---
# <a name="ichaincontextchaincontext-property"></a><span data-ttu-id="9a58f-103">Propriedade IChainContext:: ChainContext</span><span class="sxs-lookup"><span data-stu-id="9a58f-103">IChainContext::ChainContext property</span></span>

<span data-ttu-id="9a58f-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="9a58f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="9a58f-105">A propriedade **chainContext** define ou recupera o \_ \_ contexto de cadeia de PCCERT de um certificado.</span><span class="sxs-lookup"><span data-stu-id="9a58f-105">The **ChainContext** property sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="9a58f-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9a58f-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a58f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a58f-107">Syntax</span></span>


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a><span data-ttu-id="9a58f-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9a58f-108">Property value</span></span>

<span data-ttu-id="9a58f-109">O \_ \_ contexto da cadeia de PCCERT do certificado.</span><span class="sxs-lookup"><span data-stu-id="9a58f-109">The PCCERT\_CHAIN\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a58f-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="9a58f-110">Error codes</span></span>

<span data-ttu-id="9a58f-111">Se os métodos de acesso à propriedade **colocarem \_ chainContext** e o **\_ chainContext** forem bem-sucedidos, eles retornarão S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9a58f-111">If the property access methods **put\_ChainContext** and **get\_ChainContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="9a58f-112">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="9a58f-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a58f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a58f-113">Remarks</span></span>

<span data-ttu-id="9a58f-114">Você deve chamar o método [**FreeContext**](ichaincontext-freecontext.md) ou a função [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) para liberar o contexto.</span><span class="sxs-lookup"><span data-stu-id="9a58f-114">You must call either the [**FreeContext**](ichaincontext-freecontext.md) method or the [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) function to free the context.</span></span>

<span data-ttu-id="9a58f-115">Se você definir a propriedade **chainContext** , o estado do objeto de [**cadeia**](chain.md) inteiro será redefinido.</span><span class="sxs-lookup"><span data-stu-id="9a58f-115">If you set the **ChainContext** property, the state of the entire [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a58f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a58f-116">Requirements</span></span>



| <span data-ttu-id="9a58f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a58f-117">Requirement</span></span> | <span data-ttu-id="9a58f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9a58f-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a58f-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9a58f-119">Redistributable</span></span><br/> | <span data-ttu-id="9a58f-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a58f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9a58f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9a58f-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="9a58f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a58f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a58f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a58f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a58f-124">**IChainContext**</span><span class="sxs-lookup"><span data-stu-id="9a58f-124">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




