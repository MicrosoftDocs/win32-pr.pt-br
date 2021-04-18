---
description: Recupera o nome do provedor de serviços de criptografia (CSP).
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: Propriedade PrivateKey. ProviderName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754592"
---
# <a name="privatekeyprovidername-property"></a><span data-ttu-id="f826d-103">Propriedade PrivateKey. ProviderName</span><span class="sxs-lookup"><span data-stu-id="f826d-103">PrivateKey.ProviderName property</span></span>

<span data-ttu-id="f826d-104">\[A propriedade **ProviderName** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f826d-104">\[The **ProviderName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f826d-105">Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f826d-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f826d-106">A propriedade **ProviderName** recupera o nome do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="f826d-106">The **ProviderName** property retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="f826d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f826d-107">Syntax</span></span>


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a><span data-ttu-id="f826d-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f826d-108">Property value</span></span>

<span data-ttu-id="f826d-109">Uma cadeia de caracteres que contém o nome do CSP.</span><span class="sxs-lookup"><span data-stu-id="f826d-109">A string that contains the name of the CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="f826d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f826d-110">Requirements</span></span>



| <span data-ttu-id="f826d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f826d-111">Requirement</span></span> | <span data-ttu-id="f826d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f826d-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f826d-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f826d-113">Redistributable</span></span><br/> | <span data-ttu-id="f826d-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f826d-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f826d-115">DLL</span><span class="sxs-lookup"><span data-stu-id="f826d-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="f826d-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f826d-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f826d-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="f826d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f826d-118">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="f826d-118">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
