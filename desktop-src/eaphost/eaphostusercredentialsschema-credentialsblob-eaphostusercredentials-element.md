---
title: Elemento CredentialsBlob (EapHostUserCredentials)
description: É usado quando a configuração do método é um BLOB binário em vez de no formato de texto XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Elemento CredentialsBlob EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085342"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a><span data-ttu-id="0327f-104">Elemento CredentialsBlob (EapHostUserCredentials)</span><span class="sxs-lookup"><span data-stu-id="0327f-104">CredentialsBlob (EapHostUserCredentials) Element</span></span>

<span data-ttu-id="0327f-105">O elemento **CredentialsBlob (EapHostUserCredentials)** é usado quando a configuração do método é um blob binário em vez de no formato de texto XML.</span><span class="sxs-lookup"><span data-stu-id="0327f-105">The **CredentialsBlob (EapHostUserCredentials)** element is used when the method configuration is a binary BLOB instead of in XML text format.</span></span>

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="0327f-106">O elemento **CredentialsBlob** é definido pelo elemento [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0327f-106">The **CredentialsBlob** element is defined by the [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0327f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0327f-107">Remarks</span></span>

<span data-ttu-id="0327f-108">As [**credenciais**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) e os elementos **CredentialsBlob** não podem ser usados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0327f-108">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and **CredentialsBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="0327f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0327f-109">Requirements</span></span>



| <span data-ttu-id="0327f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0327f-110">Requirement</span></span> | <span data-ttu-id="0327f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="0327f-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0327f-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0327f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0327f-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0327f-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0327f-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0327f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0327f-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0327f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0327f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="0327f-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="0327f-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="0327f-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0327f-118">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="0327f-118">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

<span data-ttu-id="0327f-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="0327f-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0327f-120">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="0327f-120">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[<span data-ttu-id="0327f-121">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="0327f-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0327f-122">Esquema eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="0327f-122">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





