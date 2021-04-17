---
title: Método de ejeção de IWMPCdrom
description: O método EJECT ejeta o CD ou DVD da unidade. | Método de ejeção de IWMPCdrom
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- método de ejeção do Windows Media Player
- método de ejeção Windows Media Player, interface IWMPCdrom
- Interface IWMPCdrom Windows Media Player, método EJECT
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ca2403b86b648e98861d91a21db80ddb64aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808228"
---
# <a name="iwmpcdromeject-method"></a><span data-ttu-id="883b3-107">Método IWMPCdrom:: Eject</span><span class="sxs-lookup"><span data-stu-id="883b3-107">IWMPCdrom::eject method</span></span>

<span data-ttu-id="883b3-108">O método **EJECT** ejeta o CD ou DVD da unidade.</span><span class="sxs-lookup"><span data-stu-id="883b3-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="883b3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="883b3-109">Syntax</span></span>


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a><span data-ttu-id="883b3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="883b3-110">Parameters</span></span>

<span data-ttu-id="883b3-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="883b3-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="883b3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="883b3-112">Return value</span></span>

<span data-ttu-id="883b3-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="883b3-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="883b3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="883b3-114">Remarks</span></span>

<span data-ttu-id="883b3-115">Se a porta da unidade estiver aberta, esse método fechará a porta.</span><span class="sxs-lookup"><span data-stu-id="883b3-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="883b3-116">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="883b3-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="883b3-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="883b3-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="883b3-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="883b3-118">Examples</span></span>

<span data-ttu-id="883b3-119">O exemplo a seguir usa **EJECT** para abrir a porta da unidade de CD ou DVD que tem o índice de zero em resposta ao evento de clique de um botão.</span><span class="sxs-lookup"><span data-stu-id="883b3-119">The following example uses **eject** to open the door of the CD or DVD drive that has the index of zero in response to the Click event of a button.</span></span> <span data-ttu-id="883b3-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="883b3-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="883b3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="883b3-121">Requirements</span></span>



| <span data-ttu-id="883b3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="883b3-122">Requirement</span></span> | <span data-ttu-id="883b3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="883b3-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="883b3-124">Versão</span><span class="sxs-lookup"><span data-stu-id="883b3-124">Version</span></span><br/>   | <span data-ttu-id="883b3-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="883b3-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="883b3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="883b3-126">Namespace</span></span><br/> | <span data-ttu-id="883b3-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="883b3-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="883b3-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="883b3-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="883b3-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="883b3-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="883b3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="883b3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883b3-131">**AxWindowsMediaPlayer. PlayState (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="883b3-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="883b3-132">**Interface IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="883b3-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="883b3-133">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="883b3-133">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="883b3-134">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="883b3-134">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





