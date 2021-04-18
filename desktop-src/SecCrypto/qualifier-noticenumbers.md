---
description: Recupera a coleção de números de aviso do usuário.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Propriedade Qualifier. NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751315"
---
# <a name="qualifiernoticenumbers-property"></a><span data-ttu-id="6c014-103">Propriedade Qualifier. NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="6c014-103">Qualifier.NoticeNumbers property</span></span>

<span data-ttu-id="6c014-104">\[A propriedade **NoticeNumbers** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6c014-104">\[The **NoticeNumbers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c014-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="6c014-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="6c014-106">A propriedade **NoticeNumbers** recupera a coleção de números de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="6c014-106">The **NoticeNumbers** property retrieves the collection of user notice numbers.</span></span> <span data-ttu-id="6c014-107">Esta propriedade pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="6c014-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c014-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c014-108">Syntax</span></span>


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a><span data-ttu-id="6c014-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6c014-109">Property value</span></span>

<span data-ttu-id="6c014-110">A coleção de números de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="6c014-110">The collection of user notice numbers.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c014-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c014-111">Requirements</span></span>



| <span data-ttu-id="6c014-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c014-112">Requirement</span></span> | <span data-ttu-id="6c014-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6c014-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c014-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6c014-114">Redistributable</span></span><br/> | <span data-ttu-id="6c014-115">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c014-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6c014-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6c014-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="6c014-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c014-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c014-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c014-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c014-119">**Qualificador**</span><span class="sxs-lookup"><span data-stu-id="6c014-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
