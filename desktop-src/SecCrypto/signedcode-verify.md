---
description: Verifica a assinatura Authenticode no código assinado.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: Método SignedCode. Verify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796369"
---
# <a name="signedcodeverify-method"></a><span data-ttu-id="a6107-103">Método SignedCode. Verify</span><span class="sxs-lookup"><span data-stu-id="a6107-103">SignedCode.Verify method</span></span>

<span data-ttu-id="a6107-104">\[O método **Verify** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a6107-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a6107-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="a6107-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="a6107-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6107-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="a6107-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="a6107-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="a6107-108">O método **Verify** verifica a assinatura Authenticode no código assinado.</span><span class="sxs-lookup"><span data-stu-id="a6107-108">The **Verify** method verifies the Authenticode signature on the signed code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6107-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6107-109">Syntax</span></span>


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a6107-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6107-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6107-111">*bUIAllowed* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a6107-111">*bUIAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a6107-112">Um valor booliano que especifica se uma caixa de diálogo é usada para verificar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6107-112">A Boolean value that specifies whether a dialog box is used to verify the signature.</span></span> <span data-ttu-id="a6107-113">Se for true, uma caixa de diálogo será gerada para determinar se o código é confiável.</span><span class="sxs-lookup"><span data-stu-id="a6107-113">If true, a dialog box is generated to determine whether the code is trusted.</span></span> <span data-ttu-id="a6107-114">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="a6107-114">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6107-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6107-115">Return value</span></span>

<span data-ttu-id="a6107-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a6107-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6107-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6107-117">Requirements</span></span>



| <span data-ttu-id="a6107-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6107-118">Requirement</span></span> | <span data-ttu-id="a6107-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a6107-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6107-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a6107-120">Redistributable</span></span><br/> | <span data-ttu-id="a6107-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6107-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a6107-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a6107-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="a6107-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6107-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6107-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6107-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6107-125">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="a6107-125">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
