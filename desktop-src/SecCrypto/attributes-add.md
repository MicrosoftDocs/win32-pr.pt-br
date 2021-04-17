---
description: Adiciona um objeto de atributo à coleção.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Método Attributes. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770255"
---
# <a name="attributesadd-method"></a><span data-ttu-id="8653d-103">Método Attributes. Add</span><span class="sxs-lookup"><span data-stu-id="8653d-103">Attributes.Add method</span></span>

<span data-ttu-id="8653d-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8653d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="8653d-105">Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="8653d-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="8653d-106">O método **Add** adiciona um objeto de [**atributo**](attribute.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="8653d-106">The **Add** method adds an [**Attribute**](attribute.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8653d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8653d-107">Syntax</span></span>


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a><span data-ttu-id="8653d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8653d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8653d-109">*Atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8653d-109">*Attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8653d-110">O objeto de [**atributo**](attribute.md) a ser adicionado ao final da coleção.</span><span class="sxs-lookup"><span data-stu-id="8653d-110">The [**Attribute**](attribute.md) object to be added at the end of the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8653d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8653d-111">Return value</span></span>

<span data-ttu-id="8653d-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8653d-112">This method does not return a value.</span></span> <span data-ttu-id="8653d-113">Um aplicativo que usa esse método deve conter código para manipular uma exceção gerada por esse método.</span><span class="sxs-lookup"><span data-stu-id="8653d-113">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8653d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8653d-114">Requirements</span></span>



| <span data-ttu-id="8653d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8653d-115">Requirement</span></span> | <span data-ttu-id="8653d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8653d-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8653d-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8653d-117">End of client support</span></span><br/> | <span data-ttu-id="8653d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8653d-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8653d-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="8653d-119">End of server support</span></span><br/> | <span data-ttu-id="8653d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8653d-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8653d-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="8653d-121">Redistributable</span></span><br/>       | <span data-ttu-id="8653d-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="8653d-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8653d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8653d-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8653d-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8653d-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8653d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8653d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8653d-126">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="8653d-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="8653d-127">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="8653d-127">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
