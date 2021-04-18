---
title: Método IWMPPlaylist getItemInfo
description: O método getItemInfo retorna o valor de um atributo de playlist especificado pelo nome.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814117"
---
# <a name="iwmpplaylistgetiteminfo-method"></a><span data-ttu-id="370a3-106">Método IWMPPlaylist:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="370a3-106">IWMPPlaylist::getItemInfo method</span></span>

<span data-ttu-id="370a3-107">O método **getItemInfo** retorna o valor de um atributo de playlist especificado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="370a3-107">The **getItemInfo** method returns the value of a playlist attribute specified by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="370a3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="370a3-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="370a3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="370a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="370a3-110">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="370a3-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="370a3-111">Um **System. String** que é o nome do atributo playlist.</span><span class="sxs-lookup"><span data-stu-id="370a3-111">A **System.String** that is the name of the playlist attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="370a3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="370a3-112">Return value</span></span>

<span data-ttu-id="370a3-113">Um **System. String** que é o valor do atributo playlist.</span><span class="sxs-lookup"><span data-stu-id="370a3-113">A **System.String** that is the value of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="370a3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="370a3-114">Remarks</span></span>

<span data-ttu-id="370a3-115">Antes de usar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="370a3-115">Before using this method, you must have read access to the library.</span></span> <span data-ttu-id="370a3-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="370a3-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="370a3-117">Consulte a propriedade [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para obter o código de exemplo que usa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="370a3-117">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="370a3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="370a3-118">Requirements</span></span>



| <span data-ttu-id="370a3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="370a3-119">Requirement</span></span> | <span data-ttu-id="370a3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="370a3-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="370a3-121">Versão</span><span class="sxs-lookup"><span data-stu-id="370a3-121">Version</span></span><br/>   | <span data-ttu-id="370a3-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="370a3-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="370a3-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="370a3-123">Namespace</span></span><br/> | <span data-ttu-id="370a3-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="370a3-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="370a3-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="370a3-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="370a3-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="370a3-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="370a3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="370a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370a3-128">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="370a3-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="370a3-129">**IWMPPlaylist. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="370a3-129">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





