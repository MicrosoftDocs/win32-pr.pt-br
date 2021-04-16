---
description: Define ou recupera os dados de propriedade estendida.
ms.assetid: 115bb52a-e64d-4d84-a491-35f6dba25a58
title: Propriedade Extended. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ebbd977a107d92661110ceff02f3a5bb0bea191e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779366"
---
# <a name="extendedpropertyvalue-property"></a><span data-ttu-id="3bec5-103">Propriedade Extended. Value</span><span class="sxs-lookup"><span data-stu-id="3bec5-103">ExtendedProperty.Value property</span></span>

<span data-ttu-id="3bec5-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3bec5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3bec5-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="3bec5-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="3bec5-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="3bec5-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="3bec5-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="3bec5-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="3bec5-108">A propriedade **Value** define ou recupera os dados da propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="3bec5-108">The **Value** property sets or retrieves the extended property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bec5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bec5-109">Syntax</span></span>


```VB
ExtendedProperty.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a><span data-ttu-id="3bec5-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3bec5-110">Property value</span></span>

<span data-ttu-id="3bec5-111">Os dados da propriedade estendida, no formato especificado por *EncodingType*.</span><span class="sxs-lookup"><span data-stu-id="3bec5-111">The extended property data, in the format specified by *EncodingType*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bec5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bec5-112">Requirements</span></span>



| <span data-ttu-id="3bec5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bec5-113">Requirement</span></span> | <span data-ttu-id="3bec5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3bec5-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bec5-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3bec5-115">End of client support</span></span><br/> | <span data-ttu-id="3bec5-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3bec5-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3bec5-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3bec5-117">End of server support</span></span><br/> | <span data-ttu-id="3bec5-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bec5-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3bec5-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3bec5-119">Redistributable</span></span><br/>       | <span data-ttu-id="3bec5-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="3bec5-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3bec5-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3bec5-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3bec5-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bec5-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
