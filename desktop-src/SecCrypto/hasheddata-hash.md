---
description: Cria um hash da cadeia de caracteres especificada.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: Método HashedData. hash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755047"
---
# <a name="hasheddatahash-method"></a><span data-ttu-id="18b92-103">Método HashedData. hash</span><span class="sxs-lookup"><span data-stu-id="18b92-103">HashedData.Hash method</span></span>

<span data-ttu-id="18b92-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18b92-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="18b92-105">Em vez disso, use a [**classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="18b92-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="18b92-106">O método de **hash** cria um hash da cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="18b92-106">The **Hash** method creates a hash of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b92-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18b92-107">Syntax</span></span>


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a><span data-ttu-id="18b92-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18b92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b92-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="18b92-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="18b92-110">Cadeia de caracteres que contém o valor para hash.</span><span class="sxs-lookup"><span data-stu-id="18b92-110">String that contains the value to hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b92-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18b92-111">Return value</span></span>

<span data-ttu-id="18b92-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="18b92-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18b92-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="18b92-113">Remarks</span></span>

<span data-ttu-id="18b92-114">Para criar o hash de uma grande quantidade de dados, chame o método de **hash** para cada dado.</span><span class="sxs-lookup"><span data-stu-id="18b92-114">To create the hash of a large amount of data, call the **Hash** method for each piece of data.</span></span> <span data-ttu-id="18b92-115">O hash de cada parte dos dados é concatenado à propriedade [**Value**](hasheddata-value.md) até que a propriedade seja lida.</span><span class="sxs-lookup"><span data-stu-id="18b92-115">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="18b92-116">O conteúdo da propriedade **Value** é redefinido quando a propriedade é lida.</span><span class="sxs-lookup"><span data-stu-id="18b92-116">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b92-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18b92-117">Requirements</span></span>



| <span data-ttu-id="18b92-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="18b92-118">Requirement</span></span> | <span data-ttu-id="18b92-119">Valor</span><span class="sxs-lookup"><span data-stu-id="18b92-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18b92-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="18b92-120">End of client support</span></span><br/> | <span data-ttu-id="18b92-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18b92-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="18b92-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="18b92-122">End of server support</span></span><br/> | <span data-ttu-id="18b92-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18b92-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="18b92-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="18b92-124">Redistributable</span></span><br/>       | <span data-ttu-id="18b92-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="18b92-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="18b92-126">DLL</span><span class="sxs-lookup"><span data-stu-id="18b92-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="18b92-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18b92-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
