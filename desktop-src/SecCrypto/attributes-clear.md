---
description: Limpa todos os objetos de atributo da coleção.
ms.assetid: 98b022f8-15aa-44b4-aaff-de09081d80b6
title: Método Attributes. Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eec570200234f455467c30a3eb12429226400c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753230"
---
# <a name="attributesclear-method"></a><span data-ttu-id="d2f38-103">Método Attributes. Clear</span><span class="sxs-lookup"><span data-stu-id="d2f38-103">Attributes.Clear method</span></span>

<span data-ttu-id="d2f38-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2f38-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d2f38-105">Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="d2f38-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="d2f38-106">O método **Clear** limpa todos os objetos de [**atributo**](attribute.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="d2f38-106">The **Clear** method clears all [**Attribute**](attribute.md) objects from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f38-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2f38-107">Syntax</span></span>


```VB
Attributes.Clear()
```



## <a name="parameters"></a><span data-ttu-id="d2f38-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2f38-108">Parameters</span></span>

<span data-ttu-id="d2f38-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d2f38-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2f38-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2f38-110">Return value</span></span>

<span data-ttu-id="d2f38-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d2f38-111">This method does not return a value.</span></span> <span data-ttu-id="d2f38-112">Um aplicativo que usa esse método deve conter código para manipular uma exceção gerada por esse método.</span><span class="sxs-lookup"><span data-stu-id="d2f38-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f38-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2f38-113">Requirements</span></span>



| <span data-ttu-id="d2f38-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2f38-114">Requirement</span></span> | <span data-ttu-id="d2f38-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d2f38-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f38-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d2f38-116">End of client support</span></span><br/> | <span data-ttu-id="d2f38-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2f38-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d2f38-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d2f38-118">End of server support</span></span><br/> | <span data-ttu-id="d2f38-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2f38-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d2f38-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d2f38-120">Redistributable</span></span><br/>       | <span data-ttu-id="d2f38-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2f38-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d2f38-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d2f38-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d2f38-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2f38-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2f38-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2f38-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f38-125">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="d2f38-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="d2f38-126">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="d2f38-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
