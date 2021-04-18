---
description: Adiciona uma propriedade estendida à coleção.
ms.assetid: 1d6b3c39-17b0-4a7c-a5c2-4a3bd866be07
title: Método ExtendedProperties. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06e4170b34dcdca97bc0bae6bb48b4a057a8e9b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749677"
---
# <a name="extendedpropertiesadd-method"></a><span data-ttu-id="eb8a7-103">Método ExtendedProperties. Add</span><span class="sxs-lookup"><span data-stu-id="eb8a7-103">ExtendedProperties.Add method</span></span>

<span data-ttu-id="eb8a7-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eb8a7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="eb8a7-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="eb8a7-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="eb8a7-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="eb8a7-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="eb8a7-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="eb8a7-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="eb8a7-108">O método **Add** adiciona uma propriedade estendida à coleção.</span><span class="sxs-lookup"><span data-stu-id="eb8a7-108">The **Add** method adds an extended property to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb8a7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb8a7-109">Syntax</span></span>


```VB
ExtendedProperties.Add( _
  ByVal valProperty _
)
```



## <a name="parameters"></a><span data-ttu-id="eb8a7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb8a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb8a7-111">*valProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb8a7-111">*valProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb8a7-112">Um objeto [**estendiproperty**](extendedproperty.md) que representa a propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="eb8a7-112">An [**ExtendedProperty**](extendedproperty.md) object that represents the extended property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb8a7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb8a7-113">Return value</span></span>

<span data-ttu-id="eb8a7-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="eb8a7-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb8a7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb8a7-115">Requirements</span></span>



| <span data-ttu-id="eb8a7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb8a7-116">Requirement</span></span> | <span data-ttu-id="eb8a7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="eb8a7-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8a7-118">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="eb8a7-118">End of client support</span></span><br/> | <span data-ttu-id="eb8a7-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb8a7-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="eb8a7-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="eb8a7-120">End of server support</span></span><br/> | <span data-ttu-id="eb8a7-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb8a7-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="eb8a7-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="eb8a7-122">Redistributable</span></span><br/>       | <span data-ttu-id="eb8a7-123">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb8a7-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="eb8a7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="eb8a7-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="eb8a7-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb8a7-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
