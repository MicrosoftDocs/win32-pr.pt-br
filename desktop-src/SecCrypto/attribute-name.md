---
description: Define ou recupera o nome do CAPICOM do atributo. Essa é a propriedade padrão.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Propriedade Attribute.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750762"
---
# <a name="attributename-property"></a><span data-ttu-id="39c9d-104">Propriedade Attribute.Name</span><span class="sxs-lookup"><span data-stu-id="39c9d-104">Attribute.Name property</span></span>

<span data-ttu-id="39c9d-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="39c9d-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="39c9d-106">Em vez disso, use a [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="39c9d-106">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="39c9d-107">A propriedade **Name** define ou recupera o nome do CAPICOM do atributo.</span><span class="sxs-lookup"><span data-stu-id="39c9d-107">The **Name** property sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="39c9d-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="39c9d-108">This is the default property.</span></span>

<span data-ttu-id="39c9d-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="39c9d-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c9d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="39c9d-110">Syntax</span></span>


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a><span data-ttu-id="39c9d-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="39c9d-111">Property value</span></span>

<span data-ttu-id="39c9d-112">Um valor da enumeração [**do \_ atributo capicor**](capicom-attribute.md) que especifica o nome do CAPICOM do atributo.</span><span class="sxs-lookup"><span data-stu-id="39c9d-112">A value of the [**CAPICOM\_ATTRIBUTE**](capicom-attribute.md) enumeration that specifies the CAPICOM name of the attribute.</span></span> <span data-ttu-id="39c9d-113">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="39c9d-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="39c9d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="39c9d-114">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="39c9d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="39c9d-115">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <span data-ttu-id="39c9d-116"><dt>**tempo de assinatura do atributo capicod \_ autenticado \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39c9d-116"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</dt></span></span> </dl>                         | <span data-ttu-id="39c9d-117">O atributo contém a hora em que a assinatura foi criada.</span><span class="sxs-lookup"><span data-stu-id="39c9d-117">The attribute contains the time that the signature was created.</span></span><br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <span data-ttu-id="39c9d-118"><dt>**\_nome do documento de atributos autenticados do CApicom \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39c9d-118"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</dt></span></span> </dl>                      | <span data-ttu-id="39c9d-119">O atributo contém o nome do documento assinado.</span><span class="sxs-lookup"><span data-stu-id="39c9d-119">The attribute contains the name of the signed document.</span></span><br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <span data-ttu-id="39c9d-120"><dt>**\_Descrição do documento de atributos autenticados CApicom \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39c9d-120"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</dt></span></span> </dl> | <span data-ttu-id="39c9d-121">O atributo contém uma descrição do documento assinado.</span><span class="sxs-lookup"><span data-stu-id="39c9d-121">The attribute contains a description of the signed document.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="39c9d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="39c9d-122">Remarks</span></span>

<span data-ttu-id="39c9d-123">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o estado inteiro do objeto é redefinido.</span><span class="sxs-lookup"><span data-stu-id="39c9d-123">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c9d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c9d-124">Requirements</span></span>



| <span data-ttu-id="39c9d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c9d-125">Requirement</span></span> | <span data-ttu-id="39c9d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="39c9d-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39c9d-127">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="39c9d-127">End of client support</span></span><br/> | <span data-ttu-id="39c9d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39c9d-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="39c9d-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="39c9d-129">End of server support</span></span><br/> | <span data-ttu-id="39c9d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39c9d-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="39c9d-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="39c9d-131">Redistributable</span></span><br/>       | <span data-ttu-id="39c9d-132">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="39c9d-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="39c9d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="39c9d-133">DLL</span></span><br/>                   | <dl> <span data-ttu-id="39c9d-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39c9d-134"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c9d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="39c9d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c9d-136">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="39c9d-136">**Attribute**</span></span>](attribute.md)
</dt> </dl>

 

 
