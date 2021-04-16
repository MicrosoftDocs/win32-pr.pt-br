---
description: Define ou recupera a descrição do arquivo executável assinado.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Propriedade SignedCode. Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750744"
---
# <a name="signedcodedescription-property"></a><span data-ttu-id="85afb-103">Propriedade SignedCode. Description</span><span class="sxs-lookup"><span data-stu-id="85afb-103">SignedCode.Description property</span></span>

<span data-ttu-id="85afb-104">\[A propriedade **Descrição** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="85afb-104">\[The **Description** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="85afb-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="85afb-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="85afb-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="85afb-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="85afb-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="85afb-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="85afb-108">A propriedade **Description** define ou recupera a descrição do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="85afb-108">The **Description** property sets or retrieves the description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="85afb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="85afb-109">Syntax</span></span>


```VB
SignedCode.Description As String
```



## <a name="property-value"></a><span data-ttu-id="85afb-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="85afb-110">Property value</span></span>

<span data-ttu-id="85afb-111">A descrição do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="85afb-111">The description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="85afb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="85afb-112">Remarks</span></span>

<span data-ttu-id="85afb-113">A descrição é o texto que aparece na caixa de diálogo verificação de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="85afb-113">The description is the text that appears in the Authenticode verification dialog box.</span></span> <span data-ttu-id="85afb-114">O texto deve descrever o arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="85afb-114">The text should describe the signed executable file.</span></span> <span data-ttu-id="85afb-115">Se essa propriedade for **nula**, a caixa de diálogo exibirá o nome do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="85afb-115">If this property is **NULL**, the dialog box displays the name of the executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="85afb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85afb-116">Requirements</span></span>



| <span data-ttu-id="85afb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="85afb-117">Requirement</span></span> | <span data-ttu-id="85afb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="85afb-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85afb-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="85afb-119">Redistributable</span></span><br/> | <span data-ttu-id="85afb-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="85afb-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="85afb-121">DLL</span><span class="sxs-lookup"><span data-stu-id="85afb-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="85afb-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85afb-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85afb-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="85afb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85afb-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="85afb-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
