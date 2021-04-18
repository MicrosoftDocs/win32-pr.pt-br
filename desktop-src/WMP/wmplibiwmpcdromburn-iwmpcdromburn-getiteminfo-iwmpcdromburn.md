---
title: Método IWMPCdromBurn getItemInfo
description: O método getItemInfo recupera o valor do atributo especificado para o CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768297"
---
# <a name="iwmpcdromburngetiteminfo-method"></a><span data-ttu-id="c85ca-106">Método IWMPCdromBurn:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="c85ca-106">IWMPCdromBurn::getItemInfo method</span></span>

<span data-ttu-id="c85ca-107">O método **getItemInfo** recupera o valor do atributo especificado para o CD.</span><span class="sxs-lookup"><span data-stu-id="c85ca-107">The **getItemInfo** method retrieves the value of the specified attribute for the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="c85ca-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c85ca-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="c85ca-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c85ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c85ca-110">*bstrItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c85ca-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c85ca-111">Um **System. String** que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c85ca-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="c85ca-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c85ca-112">Value</span></span>         | <span data-ttu-id="c85ca-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c85ca-113">Description</span></span>                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85ca-114">Disponíveltime</span><span class="sxs-lookup"><span data-stu-id="c85ca-114">AvailableTime</span></span> | <span data-ttu-id="c85ca-115">Recupera o tempo disponível no CD, em segundos.</span><span class="sxs-lookup"><span data-stu-id="c85ca-115">Retrieves the time available on the CD, in seconds.</span></span>                                          |
| <span data-ttu-id="c85ca-116">Em branco</span><span class="sxs-lookup"><span data-stu-id="c85ca-116">Blank</span></span>         | <span data-ttu-id="c85ca-117">Recupera um **System. Boolean** (representado como uma cadeia de caracteres) indicando se o CD está em branco.</span><span class="sxs-lookup"><span data-stu-id="c85ca-117">Retrieves a **System.Boolean** (represented as a string) indicating whether the CD is blank.</span></span> |
| <span data-ttu-id="c85ca-118">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="c85ca-118">FreeSpace</span></span>     | <span data-ttu-id="c85ca-119">Recupera o espaço livre no CD, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c85ca-119">Retrieves the free space on the CD, in bytes.</span></span>                                                |
| <span data-ttu-id="c85ca-120">TotalSpace</span><span class="sxs-lookup"><span data-stu-id="c85ca-120">TotalSpace</span></span>    | <span data-ttu-id="c85ca-121">Recupera o espaço total no CD, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c85ca-121">Retrieves the total space on the CD, in bytes.</span></span>                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c85ca-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c85ca-122">Return value</span></span>

<span data-ttu-id="c85ca-123">Um **System. String** que é o valor do atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="c85ca-123">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="c85ca-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c85ca-124">Requirements</span></span>



| <span data-ttu-id="c85ca-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c85ca-125">Requirement</span></span> | <span data-ttu-id="c85ca-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c85ca-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85ca-127">Versão</span><span class="sxs-lookup"><span data-stu-id="c85ca-127">Version</span></span><br/>   | <span data-ttu-id="c85ca-128">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="c85ca-128">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="c85ca-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c85ca-129">Namespace</span></span><br/> | <span data-ttu-id="c85ca-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c85ca-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c85ca-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="c85ca-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c85ca-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c85ca-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c85ca-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c85ca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85ca-134">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c85ca-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





