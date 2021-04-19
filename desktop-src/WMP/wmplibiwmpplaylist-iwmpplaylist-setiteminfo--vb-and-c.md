---
title: Método IWMPPlaylist setItemInfo
description: O método setItemInfo define o valor de um atributo da playlist atual.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- método setItemInfo Windows Media Player
- método setItemInfo Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797897"
---
# <a name="iwmpplaylistsetiteminfo-method"></a><span data-ttu-id="2c40d-106">Método IWMPPlaylist:: setItemInfo</span><span class="sxs-lookup"><span data-stu-id="2c40d-106">IWMPPlaylist::setItemInfo method</span></span>

<span data-ttu-id="2c40d-107">O método **setItemInfo** define o valor de um atributo da playlist atual.</span><span class="sxs-lookup"><span data-stu-id="2c40d-107">The **setItemInfo** method sets the value of an attribute of the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c40d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c40d-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="2c40d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c40d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c40d-110">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c40d-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c40d-111">Um **System. String** que é o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="2c40d-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="2c40d-112">*bstrvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c40d-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c40d-113">Um **System. String** que é o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="2c40d-113">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c40d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c40d-114">Return value</span></span>

<span data-ttu-id="2c40d-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2c40d-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c40d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c40d-116">Remarks</span></span>

<span data-ttu-id="2c40d-117">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2c40d-117">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="2c40d-118">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2c40d-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2c40d-119">Consulte a propriedade [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para obter o código de exemplo que usa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="2c40d-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c40d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c40d-120">Requirements</span></span>



| <span data-ttu-id="2c40d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c40d-121">Requirement</span></span> | <span data-ttu-id="2c40d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2c40d-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c40d-123">Versão</span><span class="sxs-lookup"><span data-stu-id="2c40d-123">Version</span></span><br/>   | <span data-ttu-id="2c40d-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="2c40d-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2c40d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c40d-125">Namespace</span></span><br/> | <span data-ttu-id="2c40d-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2c40d-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2c40d-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="2c40d-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2c40d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2c40d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c40d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c40d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c40d-130">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2c40d-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2c40d-131">**IWMPPlaylist. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2c40d-131">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2c40d-132">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2c40d-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2c40d-133">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2c40d-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





