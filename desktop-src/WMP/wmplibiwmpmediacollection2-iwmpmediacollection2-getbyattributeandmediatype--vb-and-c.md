---
title: Método IWMPMediaCollection2 getByAttributeAndMediaType
description: O método getByAttributeAndMediaType retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia que têm um tipo de mídia e um atributo especificado.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- método getByAttributeAndMediaType Windows Media Player
- método getByAttributeAndMediaType Windows Media Player, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 Windows Media Player, método getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764104"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a><span data-ttu-id="08808-106">Método IWMPMediaCollection2:: getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="08808-106">IWMPMediaCollection2::getByAttributeAndMediaType method</span></span>

<span data-ttu-id="08808-107">O `getByAttributeAndMediaType` método retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia que têm um tipo de mídia e um atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="08808-107">The `getByAttributeAndMediaType` method returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="08808-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08808-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a><span data-ttu-id="08808-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08808-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08808-110">*bstrattribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08808-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08808-111">O **System. String** que é o atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="08808-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="08808-112">*bstrvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08808-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08808-113">O **System. String** que é o valor especificado para o atributo que é especificado em *bstrattribute*.</span><span class="sxs-lookup"><span data-stu-id="08808-113">The **System.String** that is the specified value for the attribute that is specified in *bstrAttribute*.</span></span>

</dd> <dt>

<span data-ttu-id="08808-114">*bstrMediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08808-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08808-115">O **System. String** que é o tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="08808-115">The **System.String** that is the specified media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08808-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08808-116">Return value</span></span>

<span data-ttu-id="08808-117">Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução recuperada.</span><span class="sxs-lookup"><span data-stu-id="08808-117">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="08808-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08808-118">Requirements</span></span>



| <span data-ttu-id="08808-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="08808-119">Requirement</span></span> | <span data-ttu-id="08808-120">Valor</span><span class="sxs-lookup"><span data-stu-id="08808-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08808-121">Versão</span><span class="sxs-lookup"><span data-stu-id="08808-121">Version</span></span><br/>   | <span data-ttu-id="08808-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="08808-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="08808-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="08808-123">Namespace</span></span><br/> | <span data-ttu-id="08808-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="08808-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="08808-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="08808-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="08808-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="08808-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08808-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="08808-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08808-128">**Interface IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="08808-128">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="08808-129">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="08808-129">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





