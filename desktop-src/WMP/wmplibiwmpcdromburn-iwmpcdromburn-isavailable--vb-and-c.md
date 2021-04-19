---
title: Método IsAvailable IWMPCdromBurn
description: O método IsAvailable fornece informações sobre a unidade de CD e a mídia.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- método IsAvailable Windows Media Player
- método IsAvailable Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, método IsAvailable
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780377"
---
# <a name="iwmpcdromburnisavailable-method"></a><span data-ttu-id="b5485-106">Método IWMPCdromBurn:: IsAvailable</span><span class="sxs-lookup"><span data-stu-id="b5485-106">IWMPCdromBurn::isAvailable method</span></span>

<span data-ttu-id="b5485-107">O método **IsAvailable** fornece informações sobre a unidade de CD e a mídia.</span><span class="sxs-lookup"><span data-stu-id="b5485-107">The **isAvailable** method provides information about the CD drive and media.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5485-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5485-108">Syntax</span></span>


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a><span data-ttu-id="b5485-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5485-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5485-110">*bstrItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5485-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5485-111">Um **System. String** que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5485-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="b5485-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b5485-112">Value</span></span> | <span data-ttu-id="b5485-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5485-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="b5485-114">Queima</span><span class="sxs-lookup"><span data-stu-id="b5485-114">Burn</span></span>  | <span data-ttu-id="b5485-115">A unidade é um gravador de CD.</span><span class="sxs-lookup"><span data-stu-id="b5485-115">The drive is a CD burner.</span></span>   |
| <span data-ttu-id="b5485-116">Discos</span><span class="sxs-lookup"><span data-stu-id="b5485-116">Disc</span></span>  | <span data-ttu-id="b5485-117">Há um CD na unidade.</span><span class="sxs-lookup"><span data-stu-id="b5485-117">There is a CD in the drive.</span></span> |
| <span data-ttu-id="b5485-118">Apagar</span><span class="sxs-lookup"><span data-stu-id="b5485-118">Erase</span></span> | <span data-ttu-id="b5485-119">O CD pode ser apagado.</span><span class="sxs-lookup"><span data-stu-id="b5485-119">The CD can be erased.</span></span>       |
| <span data-ttu-id="b5485-120">Gravar</span><span class="sxs-lookup"><span data-stu-id="b5485-120">Write</span></span> | <span data-ttu-id="b5485-121">O CD pode ser gravado.</span><span class="sxs-lookup"><span data-stu-id="b5485-121">The CD can be written to.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5485-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5485-122">Return value</span></span>

<span data-ttu-id="b5485-123">Um **System. Boolean** que indica o resultado.</span><span class="sxs-lookup"><span data-stu-id="b5485-123">A **System.Boolean** that indicates the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5485-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5485-124">Requirements</span></span>



| <span data-ttu-id="b5485-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5485-125">Requirement</span></span> | <span data-ttu-id="b5485-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b5485-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5485-127">Versão</span><span class="sxs-lookup"><span data-stu-id="b5485-127">Version</span></span><br/>   | <span data-ttu-id="b5485-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="b5485-128">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="b5485-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5485-129">Namespace</span></span><br/> | <span data-ttu-id="b5485-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b5485-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b5485-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="b5485-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b5485-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b5485-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5485-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5485-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5485-134">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b5485-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





