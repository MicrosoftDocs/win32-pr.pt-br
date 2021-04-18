---
description: Fornece acesso ao contexto de um objeto de armazenamento capicor. Esse contexto permite que o repositório de certificados capicor seja usado em outras derivações de CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Interface ICertStore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789494"
---
# <a name="icertstore-interface"></a><span data-ttu-id="75fe0-104">Interface ICertStore</span><span class="sxs-lookup"><span data-stu-id="75fe0-104">ICertStore interface</span></span>

<span data-ttu-id="75fe0-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="75fe0-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="75fe0-106">A interface **ICertStore** fornece acesso ao contexto de um objeto de [**armazenamento**](store.md) capicor.</span><span class="sxs-lookup"><span data-stu-id="75fe0-106">The **ICertStore** interface provides access to the context of a CAPICOM [**Store**](store.md) object.</span></span> <span data-ttu-id="75fe0-107">Esse contexto permite que o repositório de certificados capicor seja usado em outras derivações de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="75fe0-107">This context allows the CAPICOM certificate store to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="75fe0-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="75fe0-108">When to use</span></span>

<span data-ttu-id="75fe0-109">Use essa interface quando precisar usar um objeto de [**armazenamento**](store.md) capicor em outra derivação de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="75fe0-109">Use this interface when you need to use a CAPICOM [**Store**](store.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="75fe0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="75fe0-110">Members</span></span>

<span data-ttu-id="75fe0-111">A interface **ICertStore** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="75fe0-111">The **ICertStore** interface has these types of members:</span></span>

-   [<span data-ttu-id="75fe0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="75fe0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="75fe0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75fe0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="75fe0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="75fe0-114">Methods</span></span>

<span data-ttu-id="75fe0-115">A interface **ICertStore** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="75fe0-115">The **ICertStore** interface has these methods.</span></span>



| <span data-ttu-id="75fe0-116">Método</span><span class="sxs-lookup"><span data-stu-id="75fe0-116">Method</span></span>                                        | <span data-ttu-id="75fe0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="75fe0-117">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75fe0-118">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="75fe0-118">**CloseHandle**</span></span>](icertstore-closehandle.md) | <span data-ttu-id="75fe0-119">Fecha um identificador HCERTSTORE adquirido por meio da propriedade [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="75fe0-119">Closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="75fe0-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75fe0-120">Properties</span></span>

<span data-ttu-id="75fe0-121">A interface **ICertStore** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="75fe0-121">The **ICertStore** interface has these properties.</span></span>



| <span data-ttu-id="75fe0-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="75fe0-122">Property</span></span>                                                     | <span data-ttu-id="75fe0-123">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="75fe0-123">Access type</span></span>           | <span data-ttu-id="75fe0-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="75fe0-124">Description</span></span>                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75fe0-125">**StoreHandle**</span><span class="sxs-lookup"><span data-stu-id="75fe0-125">**StoreHandle**</span></span>](icertstore-storehandle.md)<br/>     | <span data-ttu-id="75fe0-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="75fe0-126">Read/write</span></span><br/> | <span data-ttu-id="75fe0-127">Define ou recupera o identificador HCERTSTORE de um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="75fe0-127">Sets or retrieves the HCERTSTORE handle of a certificate store.</span></span><br/>                                          |
| [<span data-ttu-id="75fe0-128">**StoreLocation**</span><span class="sxs-lookup"><span data-stu-id="75fe0-128">**StoreLocation**</span></span>](icertstore-storelocation.md)<br/> | <span data-ttu-id="75fe0-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="75fe0-129">Read/write</span></span><br/> | <span data-ttu-id="75fe0-130">Define ou recupera o [**\_ \_ local de armazenamento capicor**](capicom-store-location.md) de um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="75fe0-130">Sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75fe0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75fe0-131">Requirements</span></span>



| <span data-ttu-id="75fe0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="75fe0-132">Requirement</span></span> | <span data-ttu-id="75fe0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="75fe0-133">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75fe0-134">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="75fe0-134">Redistributable</span></span><br/> | <span data-ttu-id="75fe0-135">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="75fe0-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="75fe0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="75fe0-136">DLL</span></span><br/>             | <dl> <span data-ttu-id="75fe0-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75fe0-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




