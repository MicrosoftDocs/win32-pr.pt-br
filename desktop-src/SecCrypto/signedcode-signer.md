---
description: Recupera o signatário do arquivo executável assinado.
ms.assetid: aafa7006-b47c-4f4e-a5c4-bd96d297f939
title: Propriedade SignedCode. signatário
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 053bb6c98c5b8776da2ca890de24359f41be1389
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783228"
---
# <a name="signedcodesigner-property"></a><span data-ttu-id="3534e-103">Propriedade SignedCode. signatário</span><span class="sxs-lookup"><span data-stu-id="3534e-103">SignedCode.Signer property</span></span>

<span data-ttu-id="3534e-104">\[A propriedade de **signatário** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="3534e-104">\[The **Signer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3534e-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="3534e-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="3534e-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="3534e-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="3534e-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="3534e-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="3534e-108">A propriedade de **signatário** recupera o signatário do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="3534e-108">The **Signer** property retrieves the signer of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3534e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3534e-109">Syntax</span></span>


```VB
SignedCode.Signer As Signer
```



## <a name="property-value"></a><span data-ttu-id="3534e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3534e-110">Property value</span></span>

<span data-ttu-id="3534e-111">Um objeto de [**signatário**](signer.md) que fornece acesso ao assinante do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="3534e-111">A [**Signer**](signer.md) object that provides access to the signer of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3534e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3534e-112">Requirements</span></span>



| <span data-ttu-id="3534e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3534e-113">Requirement</span></span> | <span data-ttu-id="3534e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3534e-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3534e-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3534e-115">Redistributable</span></span><br/> | <span data-ttu-id="3534e-116">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="3534e-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3534e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3534e-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="3534e-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3534e-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3534e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3534e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3534e-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="3534e-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
