---
description: Define ou recupera a chave privada associada ao certificado.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Propriedade Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755315"
---
# <a name="certificateprivatekey-property"></a><span data-ttu-id="315b9-103">Propriedade Certificate. PrivateKey</span><span class="sxs-lookup"><span data-stu-id="315b9-103">Certificate.PrivateKey property</span></span>

<span data-ttu-id="315b9-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="315b9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="315b9-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="315b9-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="315b9-106">A propriedade **PrivateKey** define ou recupera a chave privada associada ao certificado.</span><span class="sxs-lookup"><span data-stu-id="315b9-106">The **PrivateKey** property sets or retrieves the private key associated with the certificate.</span></span> <span data-ttu-id="315b9-107">Esta propriedade foi introduzida no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="315b9-107">This property was introduced in CAPICOM 2.0.</span></span>

<span data-ttu-id="315b9-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="315b9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="315b9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="315b9-109">Syntax</span></span>


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a><span data-ttu-id="315b9-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="315b9-110">Property value</span></span>

<span data-ttu-id="315b9-111">Um objeto [**PrivateKey**](privatekey.md) que representa a chave privada associada ao certificado.</span><span class="sxs-lookup"><span data-stu-id="315b9-111">A [**PrivateKey**](privatekey.md) object that represents the private key that is associated with the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="315b9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="315b9-112">Remarks</span></span>

<span data-ttu-id="315b9-113">Definir a propriedade **PrivateKey** como Nothing remove a associação entre a chave privada e o certificado, mas não exclui a chave privada.</span><span class="sxs-lookup"><span data-stu-id="315b9-113">Setting the **PrivateKey** property to Nothing removes the association between the private key and the certificate, but it does not delete the private key.</span></span> <span data-ttu-id="315b9-114">Para excluir a chave privada, chame o método [**PrivateKey. Delete**](privatekey-delete.md) e, em seguida, defina essa propriedade como Nothing.</span><span class="sxs-lookup"><span data-stu-id="315b9-114">To delete the private key, call the [**PrivateKey.Delete**](privatekey-delete.md) method, and then set this property to Nothing.</span></span>

<span data-ttu-id="315b9-115">Essa propriedade gera CAPICOM \_ E \_ não \_ são permitidos quando ele é definido de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="315b9-115">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is set from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="315b9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="315b9-116">Requirements</span></span>



| <span data-ttu-id="315b9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="315b9-117">Requirement</span></span> | <span data-ttu-id="315b9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="315b9-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="315b9-119">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="315b9-119">End of client support</span></span><br/> | <span data-ttu-id="315b9-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="315b9-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="315b9-121">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="315b9-121">End of server support</span></span><br/> | <span data-ttu-id="315b9-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="315b9-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="315b9-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="315b9-123">Redistributable</span></span><br/>       | <span data-ttu-id="315b9-124">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="315b9-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="315b9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="315b9-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="315b9-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="315b9-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315b9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="315b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315b9-128">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="315b9-128">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
