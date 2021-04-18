---
description: Recupera o algoritmo para os dados criptografados.
ms.assetid: 37bebe69-3c62-44c4-a5e5-c8cdbf087fa4
title: Propriedade EncryptedData. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cd73fbda4a5f77706ac2253782768e8487b8cbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751516"
---
# <a name="encrypteddataalgorithm-property"></a><span data-ttu-id="d4cb5-103">Propriedade EncryptedData. Algorithm</span><span class="sxs-lookup"><span data-stu-id="d4cb5-103">EncryptedData.Algorithm property</span></span>

<span data-ttu-id="d4cb5-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d4cb5-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="d4cb5-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4cb5-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="d4cb5-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="d4cb5-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="d4cb5-108">A propriedade de **algoritmo** recupera o algoritmo para os dados criptografados.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-108">The **Algorithm** property retrieves the algorithm for the encrypted data.</span></span>

<span data-ttu-id="d4cb5-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4cb5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4cb5-110">Syntax</span></span>


```VB
EncryptedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="d4cb5-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d4cb5-111">Property value</span></span>

<span data-ttu-id="d4cb5-112">Um objeto de [**algoritmo**](algorithm.md) que representa o algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="d4cb5-112">An [**Algorithm**](algorithm.md) object that represents the encryption algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4cb5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4cb5-113">Requirements</span></span>



| <span data-ttu-id="d4cb5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4cb5-114">Requirement</span></span> | <span data-ttu-id="d4cb5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d4cb5-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cb5-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d4cb5-116">End of client support</span></span><br/> | <span data-ttu-id="d4cb5-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4cb5-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d4cb5-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d4cb5-118">End of server support</span></span><br/> | <span data-ttu-id="d4cb5-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4cb5-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d4cb5-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d4cb5-120">Redistributable</span></span><br/>       | <span data-ttu-id="d4cb5-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4cb5-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d4cb5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d4cb5-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d4cb5-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4cb5-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4cb5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4cb5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4cb5-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="d4cb5-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
