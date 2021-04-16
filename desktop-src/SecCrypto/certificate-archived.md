---
description: Define ou recupera um valor booliano que indica se o certificado está arquivado.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Propriedade Certificate. Arquived
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747846"
---
# <a name="certificatearchived-property"></a><span data-ttu-id="2317d-103">Propriedade Certificate. Arquived</span><span class="sxs-lookup"><span data-stu-id="2317d-103">Certificate.Archived property</span></span>

<span data-ttu-id="2317d-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2317d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2317d-105">Em vez disso, use a [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2317d-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2317d-106">A propriedade **arquivada** define ou recupera um valor booliano que indica se o certificado está arquivado.</span><span class="sxs-lookup"><span data-stu-id="2317d-106">The **Archived** property sets or retrieves a Boolean value that indicates whether the certificate is archived.</span></span>

<span data-ttu-id="2317d-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2317d-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2317d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2317d-108">Syntax</span></span>


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a><span data-ttu-id="2317d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2317d-109">Property value</span></span>

<span data-ttu-id="2317d-110">Um valor booliano que indica se o certificado é arquivado.</span><span class="sxs-lookup"><span data-stu-id="2317d-110">A Boolean value that indicates whether the certificate is archived.</span></span> <span data-ttu-id="2317d-111">Se for **true**, o certificado será arquivado.</span><span class="sxs-lookup"><span data-stu-id="2317d-111">If **true**, the certificate is archived.</span></span> <span data-ttu-id="2317d-112">Observe que a alteração do valor de **false** para **true** arquiva o certificado.</span><span class="sxs-lookup"><span data-stu-id="2317d-112">Note that changing the value from **false** to **true** archives the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="2317d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2317d-113">Remarks</span></span>

<span data-ttu-id="2317d-114">Essa propriedade gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="2317d-114">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

> [!Note]  
> <span data-ttu-id="2317d-115">Um certificado arquivado não é visível na interface do usuário do gerenciamento de certificados.</span><span class="sxs-lookup"><span data-stu-id="2317d-115">An archived certificate is not visible in the certificate management user interface.</span></span> <span data-ttu-id="2317d-116">Além disso, os certificados arquivados não serão incluídos no método [**Store. Open**](store-open.md) , a menos que o capicote \_ Store \_ Open \_ include \_ arquivo morto seja especificado.</span><span class="sxs-lookup"><span data-stu-id="2317d-116">Also, archived certificates will not be included in the [**Store.Open**](store-open.md) method unless CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED is specified.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2317d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2317d-117">Requirements</span></span>



| <span data-ttu-id="2317d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2317d-118">Requirement</span></span> | <span data-ttu-id="2317d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2317d-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2317d-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2317d-120">End of client support</span></span><br/> | <span data-ttu-id="2317d-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2317d-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2317d-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2317d-122">End of server support</span></span><br/> | <span data-ttu-id="2317d-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2317d-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2317d-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2317d-124">Redistributable</span></span><br/>       | <span data-ttu-id="2317d-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2317d-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2317d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2317d-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2317d-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2317d-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
