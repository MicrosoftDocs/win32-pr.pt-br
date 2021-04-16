---
description: Fornece acesso ao contexto de um objeto de certificado CAPICOM X. 509v3. Esse contexto permite que o certificado capicor seja usado em outras derivações de CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Interface ICertContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758912"
---
# <a name="icertcontext-interface"></a><span data-ttu-id="0d298-104">Interface ICertContext</span><span class="sxs-lookup"><span data-stu-id="0d298-104">ICertContext interface</span></span>

<span data-ttu-id="0d298-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="0d298-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="0d298-106">A interface **ICertContext** fornece acesso ao contexto de um objeto de [**certificado**](certificate.md) CAPICOM X. 509v3.</span><span class="sxs-lookup"><span data-stu-id="0d298-106">The **ICertContext** interface provides access to the context of a CAPICOM X.509v3 [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="0d298-107">Esse contexto permite que o certificado capicor seja usado em outras derivações de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="0d298-107">This context allows the CAPICOM certificate to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0d298-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="0d298-108">When to use</span></span>

<span data-ttu-id="0d298-109">Use essa interface quando precisar usar um objeto de [**certificado**](certificate.md) capicor em outra derivação de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="0d298-109">Use this interface when you need to use a CAPICOM [**Certificate**](certificate.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="0d298-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0d298-110">Members</span></span>

<span data-ttu-id="0d298-111">A interface **ICertContext** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0d298-111">The **ICertContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="0d298-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d298-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0d298-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d298-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0d298-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d298-114">Methods</span></span>

<span data-ttu-id="0d298-115">A interface **ICertContext** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0d298-115">The **ICertContext** interface has these methods.</span></span>



| <span data-ttu-id="0d298-116">Método</span><span class="sxs-lookup"><span data-stu-id="0d298-116">Method</span></span>                                          | <span data-ttu-id="0d298-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d298-117">Description</span></span>                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d298-118">**FreeContext**</span><span class="sxs-lookup"><span data-stu-id="0d298-118">**FreeContext**</span></span>](icertcontext-freecontext.md) | <span data-ttu-id="0d298-119">Libera um \_ contexto PCCERT adquirido por meio da propriedade [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="0d298-119">Releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0d298-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d298-120">Properties</span></span>

<span data-ttu-id="0d298-121">A interface **ICertContext** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d298-121">The **ICertContext** interface has these properties.</span></span>



| <span data-ttu-id="0d298-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0d298-122">Property</span></span>                                                   | <span data-ttu-id="0d298-123">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="0d298-123">Access type</span></span>           | <span data-ttu-id="0d298-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d298-124">Description</span></span>                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="0d298-125">**CertContext**</span><span class="sxs-lookup"><span data-stu-id="0d298-125">**CertContext**</span></span>](icertcontext-certcontext.md)<br/> | <span data-ttu-id="0d298-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d298-126">Read/write</span></span><br/> | <span data-ttu-id="0d298-127">Define ou recupera o \_ contexto PCCERT de um certificado.</span><span class="sxs-lookup"><span data-stu-id="0d298-127">Sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d298-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d298-128">Requirements</span></span>



| <span data-ttu-id="0d298-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d298-129">Requirement</span></span> | <span data-ttu-id="0d298-130">Valor</span><span class="sxs-lookup"><span data-stu-id="0d298-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d298-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0d298-131">Redistributable</span></span><br/> | <span data-ttu-id="0d298-132">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d298-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0d298-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0d298-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="0d298-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d298-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




