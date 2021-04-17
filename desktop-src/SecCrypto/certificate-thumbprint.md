---
description: Recupera uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Propriedade Certificate. Thumbprint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762023"
---
# <a name="certificatethumbprint-property"></a><span data-ttu-id="e2bd9-103">Propriedade Certificate. Thumbprint</span><span class="sxs-lookup"><span data-stu-id="e2bd9-103">Certificate.Thumbprint property</span></span>

<span data-ttu-id="e2bd9-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2bd9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e2bd9-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e2bd9-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e2bd9-106">A propriedade de **impressão digital** recupera uma cadeia de caracteres hexadecimal que contém o hash [*SHA-1*](../secgloss/s-gly.md) do certificado.</span><span class="sxs-lookup"><span data-stu-id="e2bd9-106">The **Thumbprint** property retrieves a hexadecimal string that contains the [*SHA-1*](../secgloss/s-gly.md) hash of the certificate.</span></span>

<span data-ttu-id="e2bd9-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e2bd9-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2bd9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2bd9-108">Syntax</span></span>


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a><span data-ttu-id="e2bd9-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e2bd9-109">Property value</span></span>

<span data-ttu-id="e2bd9-110">Uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado.</span><span class="sxs-lookup"><span data-stu-id="e2bd9-110">A hexadecimal string that contains the SHA-1 hash of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2bd9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2bd9-111">Requirements</span></span>



| <span data-ttu-id="e2bd9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2bd9-112">Requirement</span></span> | <span data-ttu-id="e2bd9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e2bd9-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2bd9-114">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e2bd9-114">End of client support</span></span><br/> | <span data-ttu-id="e2bd9-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2bd9-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e2bd9-116">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e2bd9-116">End of server support</span></span><br/> | <span data-ttu-id="e2bd9-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2bd9-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e2bd9-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e2bd9-118">Redistributable</span></span><br/>       | <span data-ttu-id="e2bd9-119">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2bd9-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e2bd9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e2bd9-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e2bd9-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2bd9-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2bd9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2bd9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2bd9-123">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="e2bd9-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
