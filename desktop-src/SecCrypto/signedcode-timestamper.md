---
description: A propriedade timetimestamper recupera a hora Stamper do arquivo executável assinado.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: Propriedade SignedCode. timetimestamper
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5594cf46e82e47103d456fc7fe147e0470333953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754589"
---
# <a name="signedcodetimestamper-property"></a><span data-ttu-id="19063-103">Propriedade SignedCode. timetimestamper</span><span class="sxs-lookup"><span data-stu-id="19063-103">SignedCode.TimeStamper property</span></span>

<span data-ttu-id="19063-104">\[A propriedade de **carimbo de data/hora** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="19063-104">\[The **TimeStamper** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="19063-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="19063-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="19063-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="19063-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="19063-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="19063-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="19063-108">A propriedade **Timetimestamper** recupera a hora Stamper do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="19063-108">The **TimeStamper** property retrieves the time stamper of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="19063-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="19063-109">Syntax</span></span>


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a><span data-ttu-id="19063-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="19063-110">Property value</span></span>

<span data-ttu-id="19063-111">Um objeto de [**signatário**](signer.md) que fornece acesso ao Stamper de tempo do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="19063-111">A [**Signer**](signer.md) object that provides access to the time stamper of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="19063-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19063-112">Requirements</span></span>



| <span data-ttu-id="19063-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="19063-113">Requirement</span></span> | <span data-ttu-id="19063-114">Valor</span><span class="sxs-lookup"><span data-stu-id="19063-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19063-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="19063-115">Redistributable</span></span><br/> | <span data-ttu-id="19063-116">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="19063-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19063-117">DLL</span><span class="sxs-lookup"><span data-stu-id="19063-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="19063-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19063-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19063-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="19063-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19063-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="19063-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
