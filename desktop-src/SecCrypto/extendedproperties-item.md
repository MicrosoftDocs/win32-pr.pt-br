---
description: A propriedade item recupera um objeto Extended da coleção. Essa é a propriedade padrão.
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: Propriedade ExtendedProperties. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 200e36f232c97c1b5a86c8a8a975783469d64a71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811798"
---
# <a name="extendedpropertiesitem-property"></a><span data-ttu-id="42ff9-104">Propriedade ExtendedProperties. Item</span><span class="sxs-lookup"><span data-stu-id="42ff9-104">ExtendedProperties.Item property</span></span>

<span data-ttu-id="42ff9-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="42ff9-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="42ff9-106">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="42ff9-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="42ff9-107">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="42ff9-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="42ff9-108">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="42ff9-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="42ff9-109">A propriedade **Item** recupera um objeto [**Extended**](extendedproperty.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="42ff9-109">The **Item** property retrieves an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span> <span data-ttu-id="42ff9-110">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="42ff9-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ff9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="42ff9-111">Syntax</span></span>


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="42ff9-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="42ff9-112">Property value</span></span>

<span data-ttu-id="42ff9-113">Um objeto [**estendiproperty**](extendedproperty.md) que representa a propriedade estendida indexada da coleção.</span><span class="sxs-lookup"><span data-stu-id="42ff9-113">An [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="42ff9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42ff9-114">Requirements</span></span>



| <span data-ttu-id="42ff9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="42ff9-115">Requirement</span></span> | <span data-ttu-id="42ff9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="42ff9-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42ff9-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="42ff9-117">End of client support</span></span><br/> | <span data-ttu-id="42ff9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42ff9-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="42ff9-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="42ff9-119">End of server support</span></span><br/> | <span data-ttu-id="42ff9-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42ff9-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="42ff9-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="42ff9-121">Redistributable</span></span><br/>       | <span data-ttu-id="42ff9-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="42ff9-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="42ff9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="42ff9-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="42ff9-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42ff9-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
