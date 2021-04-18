---
description: Recupera o número de objetos Extended na coleção.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: Propriedade ExtendedProperties. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4370f7ce5fc215d18b0940d3dbc2edc221af536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749883"
---
# <a name="extendedpropertiescount-property"></a><span data-ttu-id="c28ba-103">Propriedade ExtendedProperties. Count</span><span class="sxs-lookup"><span data-stu-id="c28ba-103">ExtendedProperties.Count property</span></span>

<span data-ttu-id="c28ba-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c28ba-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c28ba-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="c28ba-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="c28ba-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="c28ba-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="c28ba-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="c28ba-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="c28ba-108">A propriedade **Count** recupera o número de objetos [**Extended**](extendedproperty.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="c28ba-108">The **Count** property retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c28ba-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c28ba-109">Syntax</span></span>


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="c28ba-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c28ba-110">Property value</span></span>

<span data-ttu-id="c28ba-111">O número de objetos [**estendiproperty**](extendedproperty.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="c28ba-111">The number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c28ba-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c28ba-112">Requirements</span></span>



| <span data-ttu-id="c28ba-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c28ba-113">Requirement</span></span> | <span data-ttu-id="c28ba-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c28ba-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c28ba-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c28ba-115">End of client support</span></span><br/> | <span data-ttu-id="c28ba-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c28ba-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c28ba-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c28ba-117">End of server support</span></span><br/> | <span data-ttu-id="c28ba-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c28ba-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c28ba-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c28ba-119">Redistributable</span></span><br/>       | <span data-ttu-id="c28ba-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c28ba-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c28ba-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c28ba-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c28ba-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c28ba-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
