---
title: Método IWMPCdromRip startRip
description: O método startRip Rips o CD.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- método startRip Windows Media Player
- método startRip Windows Media Player, interface IWMPCdromRip
- Interface IWMPCdromRip Windows Media Player, método startRip
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751938"
---
# <a name="iwmpcdromripstartrip-method"></a><span data-ttu-id="f5cd7-106">Método IWMPCdromRip:: startRip</span><span class="sxs-lookup"><span data-stu-id="f5cd7-106">IWMPCdromRip::startRip method</span></span>

<span data-ttu-id="f5cd7-107">O método **startRip** Rips o CD.</span><span class="sxs-lookup"><span data-stu-id="f5cd7-107">The **startRip** method rips the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5cd7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5cd7-108">Syntax</span></span>


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a><span data-ttu-id="f5cd7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5cd7-109">Parameters</span></span>

<span data-ttu-id="f5cd7-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f5cd7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5cd7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5cd7-111">Return value</span></span>

<span data-ttu-id="f5cd7-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f5cd7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5cd7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5cd7-113">Remarks</span></span>

<span data-ttu-id="f5cd7-114">Copiar um CD usando a interface **IWMPCdromRip** tem o mesmo efeito que copiar música usando a interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f5cd7-114">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="f5cd7-115">O conteúdo copiado é adicionado automaticamente à biblioteca de acordo com as preferências do usuário.</span><span class="sxs-lookup"><span data-stu-id="f5cd7-115">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="f5cd7-116">Para obter mais informações sobre as preferências do usuário para a cópia de CD, consulte "copiando música de CDs" na ajuda do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f5cd7-116">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5cd7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5cd7-117">Requirements</span></span>



| <span data-ttu-id="f5cd7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5cd7-118">Requirement</span></span> | <span data-ttu-id="f5cd7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f5cd7-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5cd7-120">Versão</span><span class="sxs-lookup"><span data-stu-id="f5cd7-120">Version</span></span><br/>   | <span data-ttu-id="f5cd7-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f5cd7-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="f5cd7-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5cd7-122">Namespace</span></span><br/> | <span data-ttu-id="f5cd7-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f5cd7-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f5cd7-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="f5cd7-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f5cd7-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f5cd7-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5cd7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5cd7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5cd7-127">**Interface IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f5cd7-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5cd7-128">**IWMPCdromRip.stopRip**</span><span class="sxs-lookup"><span data-stu-id="f5cd7-128">**IWMPCdromRip.stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5cd7-129">**Copiando um CD**</span><span class="sxs-lookup"><span data-stu-id="f5cd7-129">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





