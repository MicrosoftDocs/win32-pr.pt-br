---
description: Define ou recupera uma cadeia de caracteres que contém um valor de cadeia de OID EKU, conforme definido em Wincrypt. h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'Propriedade IEKU:: OID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757075"
---
# <a name="iekuoid-property"></a><span data-ttu-id="ad2fc-103">Propriedade IEKU:: OID</span><span class="sxs-lookup"><span data-stu-id="ad2fc-103">IEKU::OID property</span></span>

<span data-ttu-id="ad2fc-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ad2fc-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ad2fc-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ad2fc-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ad2fc-106">A propriedade **OID** define ou recupera uma cadeia de caracteres que contém um valor de cadeia de OID EKU, conforme definido em Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="ad2fc-106">The **OID** property sets or retrieves a string that contains an EKU OID string value as defined in Wincrypt.h.</span></span>

<span data-ttu-id="ad2fc-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ad2fc-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2fc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad2fc-108">Syntax</span></span>


```VB
EKU.OID As String
```



## <a name="property-value"></a><span data-ttu-id="ad2fc-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ad2fc-109">Property value</span></span>

<span data-ttu-id="ad2fc-110">Cadeia de caracteres que contém o valor da cadeia de OID EKU, conforme definido em Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="ad2fc-110">String that contains the EKU OID string value as defined in Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad2fc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad2fc-111">Remarks</span></span>

<span data-ttu-id="ad2fc-112">Essa propriedade não usa o objeto [**OID**](oid.md) introduzido no capicom 2,0.</span><span class="sxs-lookup"><span data-stu-id="ad2fc-112">This property does not use the [**OID**](oid.md) object introduced in CAPICOM 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad2fc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad2fc-113">Requirements</span></span>



| <span data-ttu-id="ad2fc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad2fc-114">Requirement</span></span> | <span data-ttu-id="ad2fc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ad2fc-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2fc-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ad2fc-116">End of client support</span></span><br/> | <span data-ttu-id="ad2fc-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad2fc-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ad2fc-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ad2fc-118">End of server support</span></span><br/> | <span data-ttu-id="ad2fc-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad2fc-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ad2fc-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ad2fc-120">Redistributable</span></span><br/>       | <span data-ttu-id="ad2fc-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ad2fc-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ad2fc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ad2fc-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ad2fc-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad2fc-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
