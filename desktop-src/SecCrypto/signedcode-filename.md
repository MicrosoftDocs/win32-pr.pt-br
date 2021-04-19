---
description: A propriedade FileName define ou recupera o caminho para o arquivo executável. Essa é a propriedade padrão.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Propriedade SignedCode. FileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756854"
---
# <a name="signedcodefilename-property"></a><span data-ttu-id="e354a-104">Propriedade SignedCode. FileName</span><span class="sxs-lookup"><span data-stu-id="e354a-104">SignedCode.FileName property</span></span>

<span data-ttu-id="e354a-105">\[A propriedade **filename** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e354a-105">\[The **FileName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e354a-106">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="e354a-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="e354a-107">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="e354a-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="e354a-108">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="e354a-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="e354a-109">A propriedade **filename** define ou recupera o caminho para o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="e354a-109">The **FileName** property sets or retrieves the path to the executable file.</span></span> <span data-ttu-id="e354a-110">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="e354a-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e354a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e354a-111">Syntax</span></span>


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a><span data-ttu-id="e354a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e354a-112">Property value</span></span>

<span data-ttu-id="e354a-113">O caminho para o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="e354a-113">The path to the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="e354a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e354a-114">Remarks</span></span>

<span data-ttu-id="e354a-115">Se o valor da propriedade **filename** for modificado, o estado do objeto [**SignedCode**](signedcode.md) inteiro será redefinido.</span><span class="sxs-lookup"><span data-stu-id="e354a-115">If the value of the **FileName** property is modified, the state of the entire [**SignedCode**](signedcode.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="e354a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e354a-116">Requirements</span></span>



| <span data-ttu-id="e354a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e354a-117">Requirement</span></span> | <span data-ttu-id="e354a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e354a-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e354a-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e354a-119">Redistributable</span></span><br/> | <span data-ttu-id="e354a-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e354a-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e354a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e354a-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="e354a-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e354a-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e354a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e354a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e354a-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="e354a-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
