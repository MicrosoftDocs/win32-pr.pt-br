---
description: Recupera os dados com hash após chamadas bem-sucedidas para o método de hash.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: Propriedade HashedData. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780917"
---
# <a name="hasheddatavalue-property"></a><span data-ttu-id="d075f-103">Propriedade HashedData. Value</span><span class="sxs-lookup"><span data-stu-id="d075f-103">HashedData.Value property</span></span>

<span data-ttu-id="d075f-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d075f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d075f-105">Em vez disso, use a [**classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d075f-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d075f-106">A propriedade **Value** recupera os dados com hash após chamadas bem-sucedidas para o método de [**hash**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="d075f-106">The **Value** property retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="d075f-107">O valor de hash é retornado no formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="d075f-107">The hash value is returned in hexadecimal format.</span></span> <span data-ttu-id="d075f-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="d075f-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d075f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d075f-109">Syntax</span></span>


```VB
HashedData.Value As String
```



## <a name="property-value"></a><span data-ttu-id="d075f-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d075f-110">Property value</span></span>

<span data-ttu-id="d075f-111">Uma cadeia de caracteres que contém os dados com hash no formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="d075f-111">A string that contains the hashed data in hexadecimal format.</span></span>

## <a name="remarks"></a><span data-ttu-id="d075f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d075f-112">Remarks</span></span>

<span data-ttu-id="d075f-113">Para criar o hash de uma grande quantidade de dados, chame o método de [**hash**](hasheddata-hash.md) para cada dado.</span><span class="sxs-lookup"><span data-stu-id="d075f-113">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="d075f-114">O hash de cada parte dos dados é concatenado à propriedade **Value** até que a propriedade seja lida.</span><span class="sxs-lookup"><span data-stu-id="d075f-114">The hash of each piece of data is concatenated to the **Value** property until the property is read.</span></span> <span data-ttu-id="d075f-115">O conteúdo da propriedade **Value** é redefinido quando a propriedade é lida.</span><span class="sxs-lookup"><span data-stu-id="d075f-115">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="d075f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d075f-116">Requirements</span></span>



| <span data-ttu-id="d075f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d075f-117">Requirement</span></span> | <span data-ttu-id="d075f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d075f-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d075f-119">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d075f-119">End of client support</span></span><br/> | <span data-ttu-id="d075f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d075f-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d075f-121">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d075f-121">End of server support</span></span><br/> | <span data-ttu-id="d075f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d075f-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d075f-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d075f-123">Redistributable</span></span><br/>       | <span data-ttu-id="d075f-124">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d075f-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d075f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d075f-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d075f-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d075f-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d075f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d075f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d075f-128">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="d075f-128">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
