---
description: Recupera a coleção de certificados no arquivo executável assinado.
ms.assetid: ecc05117-8b98-4e49-9671-71829df24597
title: Propriedade SignedCode. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b24a07041dae1ea2387ced93d1d2ae541a806029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762011"
---
# <a name="signedcodecertificates-property"></a><span data-ttu-id="197a7-103">Propriedade SignedCode. Certificates</span><span class="sxs-lookup"><span data-stu-id="197a7-103">SignedCode.Certificates property</span></span>

<span data-ttu-id="197a7-104">\[A propriedade **Certificates** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="197a7-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="197a7-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="197a7-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="197a7-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="197a7-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="197a7-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="197a7-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="197a7-108">A propriedade **Certificates** recupera a coleção de certificados no arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="197a7-108">The **Certificates** property retrieves the collection of certificates in the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="197a7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="197a7-109">Syntax</span></span>


```VB
SignedCode.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="197a7-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="197a7-110">Property value</span></span>

<span data-ttu-id="197a7-111">A coleção de [**certificados**](certificates.md) que contém todos os certificados no arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="197a7-111">The [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="197a7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="197a7-112">Requirements</span></span>



| <span data-ttu-id="197a7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="197a7-113">Requirement</span></span> | <span data-ttu-id="197a7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="197a7-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="197a7-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="197a7-115">Redistributable</span></span><br/> | <span data-ttu-id="197a7-116">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="197a7-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="197a7-117">DLL</span><span class="sxs-lookup"><span data-stu-id="197a7-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="197a7-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="197a7-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197a7-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="197a7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197a7-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="197a7-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
