---
description: Cria uma assinatura de carimbo de data/hora Authenticode no arquivo executável assinado especificado na propriedade SignedCode. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: Método SignedCode. Timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760380"
---
# <a name="signedcodetimestamp-method"></a><span data-ttu-id="41d32-103">Método SignedCode. Timestamp</span><span class="sxs-lookup"><span data-stu-id="41d32-103">SignedCode.Timestamp method</span></span>

<span data-ttu-id="41d32-104">\[O método **timestamp** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="41d32-104">\[The **Timestamp** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="41d32-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="41d32-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="41d32-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="41d32-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="41d32-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="41d32-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="41d32-108">O método timestamp cria uma assinatura de carimbo de data **/** hora Authenticode no arquivo executável assinado especificado na propriedade **SignedCode. FileName** .</span><span class="sxs-lookup"><span data-stu-id="41d32-108">The **Timestamp** method creates an Authenticode time stamp signature on the signed executable file specified in the **SignedCode.FileName** property.</span></span> <span data-ttu-id="41d32-109">Esse carimbo de data/hora é uma assinatura de contador no arquivo executável assinado que é executado por uma autoridade de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="41d32-109">This time stamp is a counter signature on the signed executable file that is performed by a time stamp authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d32-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41d32-110">Syntax</span></span>


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a><span data-ttu-id="41d32-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41d32-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d32-112">*URL* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="41d32-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d32-113">Uma cadeia de caracteres que contém a URL do servidor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="41d32-113">A string that contains the URL of the time stamp server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d32-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41d32-114">Return value</span></span>

<span data-ttu-id="41d32-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="41d32-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41d32-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="41d32-116">Remarks</span></span>

<span data-ttu-id="41d32-117">Um carimbo de data/hora estende a validade de um certificado verificando se o arquivo executável foi assinado no momento em que estava carimbado.</span><span class="sxs-lookup"><span data-stu-id="41d32-117">A time stamp extends the validity of a certificate by verifying that the executable file was signed at the time that it was time stamped.</span></span>

<span data-ttu-id="41d32-118">Antes que esse método possa ser chamado, o arquivo executável assinado deve ser marcado com carimbo de data/hora devem ser especificados na propriedade **SignedCode. FileName** e o método [**SignedCode. Sign**](signedcode-sign.md) deve ser chamado para assinar o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="41d32-118">Before this method can be called, the signed executable file to be time stamped must be specified in the **SignedCode.FileName** property, and the [**SignedCode.Sign**](signedcode-sign.md) method must be called to sign the executable file.</span></span>

<span data-ttu-id="41d32-119">Se o arquivo executável assinado já estiver com carimbo de data/hora, esse método substituirá o carimbo de data/hora existente.</span><span class="sxs-lookup"><span data-stu-id="41d32-119">If the signed executable file is already time stamped, this method overwrites the existing time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="41d32-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41d32-120">Requirements</span></span>



| <span data-ttu-id="41d32-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d32-121">Requirement</span></span> | <span data-ttu-id="41d32-122">Valor</span><span class="sxs-lookup"><span data-stu-id="41d32-122">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d32-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="41d32-123">Redistributable</span></span><br/> | <span data-ttu-id="41d32-124">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="41d32-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="41d32-125">DLL</span><span class="sxs-lookup"><span data-stu-id="41d32-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="41d32-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d32-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d32-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="41d32-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d32-128">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="41d32-128">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
