---
description: Representa uma única propriedade EKU (uso estendido de chave) de um certificado.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Objeto EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766829"
---
# <a name="eku-object"></a><span data-ttu-id="479fb-103">Objeto EKU</span><span class="sxs-lookup"><span data-stu-id="479fb-103">EKU object</span></span>

<span data-ttu-id="479fb-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="479fb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="479fb-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="479fb-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="479fb-106">O objeto **EKU** representa uma única propriedade EKU (uso estendido de chave) de um certificado.</span><span class="sxs-lookup"><span data-stu-id="479fb-106">The **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="479fb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="479fb-107">Members</span></span>

<span data-ttu-id="479fb-108">O objeto **EKU** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="479fb-108">The **EKU** object has these types of members:</span></span>

-   [<span data-ttu-id="479fb-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="479fb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="479fb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="479fb-110">Properties</span></span>

<span data-ttu-id="479fb-111">O objeto **EKU** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="479fb-111">The **EKU** object has these properties.</span></span>



| <span data-ttu-id="479fb-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="479fb-112">Property</span></span>                            | <span data-ttu-id="479fb-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="479fb-113">Access type</span></span>           | <span data-ttu-id="479fb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="479fb-114">Description</span></span>                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="479fb-115">**Nome**</span><span class="sxs-lookup"><span data-stu-id="479fb-115">**Name**</span></span>](eku-name.md)<br/> | <span data-ttu-id="479fb-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="479fb-116">Read/write</span></span><br/> | <span data-ttu-id="479fb-117">Define ou recupera um valor de enumeração que especifica o nome do CAPICOM do EKU.</span><span class="sxs-lookup"><span data-stu-id="479fb-117">Sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="479fb-118">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="479fb-118">This is the default property.</span></span><br/>                                                                                   |
| [<span data-ttu-id="479fb-119">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="479fb-119">**OID**</span></span>](eku-oid.md)<br/>   | <span data-ttu-id="479fb-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="479fb-120">Read/write</span></span><br/> | <span data-ttu-id="479fb-121">Define ou recupera uma cadeia de caracteres que contém um valor de cadeia de caracteres OID ( [*identificador de objeto*](../secgloss/o-gly.md) EKU), conforme definido em Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="479fb-121">Sets or retrieves a string that contains an EKU [*object identifier*](../secgloss/o-gly.md) (OID) string value as defined in Wincrypt.h.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="479fb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="479fb-122">Remarks</span></span>

<span data-ttu-id="479fb-123">O objeto **EKU** é usado pela seguinte coleção e Propriedade:</span><span class="sxs-lookup"><span data-stu-id="479fb-123">The **EKU** object is used by the following collection and property:</span></span>

-   <span data-ttu-id="479fb-124">Coleção [**EKUs**](ekus.md)</span><span class="sxs-lookup"><span data-stu-id="479fb-124">[**EKUs**](ekus.md) collection</span></span>
-   <span data-ttu-id="479fb-125">Propriedade [**CertificateStatus. EKU**](certificatestatus-eku.md)</span><span class="sxs-lookup"><span data-stu-id="479fb-125">[**CertificateStatus.EKU**](certificatestatus-eku.md) property</span></span>

<span data-ttu-id="479fb-126">Não é possível criar o objeto **EKU** .</span><span class="sxs-lookup"><span data-stu-id="479fb-126">The **EKU** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="479fb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="479fb-127">Requirements</span></span>



| <span data-ttu-id="479fb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="479fb-128">Requirement</span></span> | <span data-ttu-id="479fb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="479fb-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="479fb-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="479fb-130">End of client support</span></span><br/> | <span data-ttu-id="479fb-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="479fb-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="479fb-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="479fb-132">End of server support</span></span><br/> | <span data-ttu-id="479fb-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="479fb-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="479fb-134">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="479fb-134">Redistributable</span></span><br/>       | <span data-ttu-id="479fb-135">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="479fb-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="479fb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="479fb-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="479fb-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="479fb-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
