---
description: Recupera um valor booliano que indica se o certificado é para uma autoridade de certificação (CA).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: Propriedade BasicConstraints. IsCertificateAuthority
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750761"
---
# <a name="basicconstraintsiscertificateauthority-property"></a><span data-ttu-id="07560-103">Propriedade BasicConstraints. IsCertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="07560-103">BasicConstraints.IsCertificateAuthority property</span></span>

<span data-ttu-id="07560-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="07560-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="07560-105">Em vez disso, use a [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="07560-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="07560-106">A propriedade **IsCertificateAuthority** recupera um valor booliano que indica se o certificado é para uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="07560-106">The **IsCertificateAuthority** property retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="07560-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="07560-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07560-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07560-108">Syntax</span></span>


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a><span data-ttu-id="07560-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="07560-109">Property value</span></span>

<span data-ttu-id="07560-110">Se **for true**, o certificado será usado somente por uma autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="07560-110">If **True**, the certificate is to be used only by a CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="07560-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07560-111">Requirements</span></span>



| <span data-ttu-id="07560-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="07560-112">Requirement</span></span> | <span data-ttu-id="07560-113">Valor</span><span class="sxs-lookup"><span data-stu-id="07560-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07560-114">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="07560-114">End of client support</span></span><br/> | <span data-ttu-id="07560-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07560-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="07560-116">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="07560-116">End of server support</span></span><br/> | <span data-ttu-id="07560-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07560-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="07560-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="07560-118">Redistributable</span></span><br/>       | <span data-ttu-id="07560-119">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="07560-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="07560-120">DLL</span><span class="sxs-lookup"><span data-stu-id="07560-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="07560-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07560-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
