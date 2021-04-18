---
description: A \_ Propriedade NewEnum de ExtendedProperties recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).
ms.assetid: 2692f607-3bec-4674-9d8d-3c872d523ace
title: Propriedade ExtendedProperties._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62f07fe7a1a193f93fc0d3bf4c04fbfc5d76ecf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778688"
---
# <a name="extendedproperties_newenum-property"></a><span data-ttu-id="27dd7-104">ExtendedProperties. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="27dd7-104">ExtendedProperties.\_NewEnum property</span></span>

<span data-ttu-id="27dd7-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27dd7-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="27dd7-106">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="27dd7-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="27dd7-107">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="27dd7-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="27dd7-108">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="27dd7-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="27dd7-109">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="27dd7-109">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="27dd7-110">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="27dd7-110">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="27dd7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="27dd7-111">Syntax</span></span>


```VB
ExtendedProperties._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="27dd7-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="27dd7-112">Property value</span></span>

<span data-ttu-id="27dd7-113">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="27dd7-113">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="27dd7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="27dd7-114">Remarks</span></span>

<span data-ttu-id="27dd7-115">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="27dd7-115">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="27dd7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27dd7-116">Requirements</span></span>



| <span data-ttu-id="27dd7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="27dd7-117">Requirement</span></span> | <span data-ttu-id="27dd7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="27dd7-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27dd7-119">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="27dd7-119">End of client support</span></span><br/> | <span data-ttu-id="27dd7-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27dd7-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="27dd7-121">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="27dd7-121">End of server support</span></span><br/> | <span data-ttu-id="27dd7-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27dd7-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="27dd7-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="27dd7-123">Redistributable</span></span><br/>       | <span data-ttu-id="27dd7-124">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="27dd7-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="27dd7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="27dd7-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="27dd7-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27dd7-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
