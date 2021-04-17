---
description: Recupera o número de objetos de atributo na coleção.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Propriedade Attributes. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749462"
---
# <a name="attributescount-property"></a><span data-ttu-id="9136c-103">Propriedade Attributes. Count</span><span class="sxs-lookup"><span data-stu-id="9136c-103">Attributes.Count property</span></span>

<span data-ttu-id="9136c-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9136c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="9136c-105">Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="9136c-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="9136c-106">A propriedade **Count** recupera o número de objetos de [**atributo**](attribute.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="9136c-106">The **Count** property retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span>

<span data-ttu-id="9136c-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9136c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9136c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9136c-108">Syntax</span></span>


```VB
Attributes.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="9136c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9136c-109">Property value</span></span>

<span data-ttu-id="9136c-110">O número de objetos de [**atributo**](attribute.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="9136c-110">The number of [**Attribute**](attribute.md) objects in the collection.</span></span> <span data-ttu-id="9136c-111">Cada objeto de **atributo** representa um único atributo na coleção.</span><span class="sxs-lookup"><span data-stu-id="9136c-111">Each **Attribute** object represents a single attribute in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="9136c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9136c-112">Remarks</span></span>

<span data-ttu-id="9136c-113">A propriedade **Count** pode ser usada para especificar o último objeto de [**atributo**](attribute.md) na coleção ao recuperar um objeto de **atributo** específico usando a propriedade [**Attributes. Item**](attributes-item.md) .</span><span class="sxs-lookup"><span data-stu-id="9136c-113">The **Count** property can be used to specify the last [**Attribute**](attribute.md) object in the collection when retrieving a specific **Attribute** object by using the [**Attributes.Item**](attributes-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9136c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9136c-114">Requirements</span></span>



| <span data-ttu-id="9136c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9136c-115">Requirement</span></span> | <span data-ttu-id="9136c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9136c-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9136c-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9136c-117">End of client support</span></span><br/> | <span data-ttu-id="9136c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9136c-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9136c-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="9136c-119">End of server support</span></span><br/> | <span data-ttu-id="9136c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9136c-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9136c-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9136c-121">Redistributable</span></span><br/>       | <span data-ttu-id="9136c-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="9136c-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9136c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9136c-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9136c-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9136c-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9136c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9136c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9136c-126">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="9136c-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
