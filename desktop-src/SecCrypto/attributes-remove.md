---
description: Remove um objeto de atributo indexado da coleção.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Método Attributes. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758924"
---
# <a name="attributesremove-method"></a><span data-ttu-id="34f92-103">Método Attributes. Remove</span><span class="sxs-lookup"><span data-stu-id="34f92-103">Attributes.Remove method</span></span>

<span data-ttu-id="34f92-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="34f92-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="34f92-105">Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="34f92-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="34f92-106">O método **Remove** remove um objeto de [**atributo**](attribute.md) indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="34f92-106">The **Remove** method removes an indexed [**Attribute**](attribute.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f92-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34f92-107">Syntax</span></span>


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="34f92-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34f92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34f92-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="34f92-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34f92-110">Índice do objeto de [**atributo**](attribute.md) a ser removido.</span><span class="sxs-lookup"><span data-stu-id="34f92-110">Index of the [**Attribute**](attribute.md) object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34f92-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34f92-111">Return value</span></span>

<span data-ttu-id="34f92-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="34f92-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34f92-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="34f92-113">Remarks</span></span>

<span data-ttu-id="34f92-114">Os aplicativos que usam esse método devem conter código para manipular uma exceção gerada por esse método.</span><span class="sxs-lookup"><span data-stu-id="34f92-114">Applications that use this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f92-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34f92-115">Requirements</span></span>



| <span data-ttu-id="34f92-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="34f92-116">Requirement</span></span> | <span data-ttu-id="34f92-117">Valor</span><span class="sxs-lookup"><span data-stu-id="34f92-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34f92-118">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="34f92-118">End of client support</span></span><br/> | <span data-ttu-id="34f92-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34f92-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="34f92-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="34f92-120">End of server support</span></span><br/> | <span data-ttu-id="34f92-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34f92-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="34f92-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="34f92-122">Redistributable</span></span><br/>       | <span data-ttu-id="34f92-123">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="34f92-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="34f92-124">DLL</span><span class="sxs-lookup"><span data-stu-id="34f92-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="34f92-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34f92-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34f92-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="34f92-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f92-127">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="34f92-127">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="34f92-128">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="34f92-128">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
