---
description: Define ou recupera o conteúdo a ser criptografado ou descriptografado.
ms.assetid: fdab0f19-c69e-443b-b4b3-079d23028921
title: Propriedade EncryptedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b873d40ed04270defe04fd59f0ce00a0f84040a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752337"
---
# <a name="encrypteddatacontent-property"></a><span data-ttu-id="e8c4e-103">Propriedade EncryptedData. Content</span><span class="sxs-lookup"><span data-stu-id="e8c4e-103">EncryptedData.Content property</span></span>

<span data-ttu-id="e8c4e-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e8c4e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e8c4e-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens.</span><span class="sxs-lookup"><span data-stu-id="e8c4e-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="e8c4e-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8c4e-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="e8c4e-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="e8c4e-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="e8c4e-108">A propriedade de **conteúdo** define ou recupera o conteúdo a ser criptografado ou descriptografado.</span><span class="sxs-lookup"><span data-stu-id="e8c4e-108">The **Content** property sets or retrieves the content to be encrypted or decrypted.</span></span> <span data-ttu-id="e8c4e-109">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="e8c4e-109">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c4e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8c4e-110">Syntax</span></span>


```VB
EncryptedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="e8c4e-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e8c4e-111">Property value</span></span>

<span data-ttu-id="e8c4e-112">O conteúdo a ser criptografado ou descriptografado.</span><span class="sxs-lookup"><span data-stu-id="e8c4e-112">The content to be encrypted or decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c4e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8c4e-113">Requirements</span></span>



| <span data-ttu-id="e8c4e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c4e-114">Requirement</span></span> | <span data-ttu-id="e8c4e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e8c4e-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c4e-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e8c4e-116">End of client support</span></span><br/> | <span data-ttu-id="e8c4e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8c4e-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e8c4e-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e8c4e-118">End of server support</span></span><br/> | <span data-ttu-id="e8c4e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8c4e-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e8c4e-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e8c4e-120">Redistributable</span></span><br/>       | <span data-ttu-id="e8c4e-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8c4e-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e8c4e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e8c4e-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e8c4e-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8c4e-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c4e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8c4e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c4e-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="e8c4e-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
