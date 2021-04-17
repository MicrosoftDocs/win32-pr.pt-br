---
description: Define ou recupera a URL de uma descrição do arquivo executável assinado.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Propriedade SignedCode. DescriptionURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779943"
---
# <a name="signedcodedescriptionurl-property"></a><span data-ttu-id="38f22-103">Propriedade SignedCode. DescriptionURL</span><span class="sxs-lookup"><span data-stu-id="38f22-103">SignedCode.DescriptionURL property</span></span>

<span data-ttu-id="38f22-104">\[A propriedade **DescriptionURL** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="38f22-104">\[The **DescriptionURL** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="38f22-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="38f22-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="38f22-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="38f22-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="38f22-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="38f22-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="38f22-108">A propriedade **DescriptionURL** define ou recupera a URL de uma descrição do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="38f22-108">The **DescriptionURL** property sets or retrieves the URL of a description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f22-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38f22-109">Syntax</span></span>


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a><span data-ttu-id="38f22-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="38f22-110">Property value</span></span>

<span data-ttu-id="38f22-111">A URL de uma descrição do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="38f22-111">The URL of a description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f22-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="38f22-112">Remarks</span></span>

<span data-ttu-id="38f22-113">O **DescriptionURL** é a URL para a qual a [**Descrição**](signedcode-description.md) aparece nos links da caixa de diálogo verificação de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="38f22-113">The **DescriptionURL** is the URL to which the [**Description**](signedcode-description.md) that appears in the Authenticode verification dialog box links.</span></span> <span data-ttu-id="38f22-114">Se essa propriedade for **nula**, a **Descrição** não funcionará como um link.</span><span class="sxs-lookup"><span data-stu-id="38f22-114">If this property is **NULL**, the **Description** does not function as a link.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f22-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38f22-115">Requirements</span></span>



| <span data-ttu-id="38f22-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f22-116">Requirement</span></span> | <span data-ttu-id="38f22-117">Valor</span><span class="sxs-lookup"><span data-stu-id="38f22-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38f22-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="38f22-118">Redistributable</span></span><br/> | <span data-ttu-id="38f22-119">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="38f22-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="38f22-120">DLL</span><span class="sxs-lookup"><span data-stu-id="38f22-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="38f22-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38f22-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38f22-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="38f22-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f22-123">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="38f22-123">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
