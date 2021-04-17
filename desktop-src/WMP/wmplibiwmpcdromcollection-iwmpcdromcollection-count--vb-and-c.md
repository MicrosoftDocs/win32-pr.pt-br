---
title: Propriedade Count de IWMPCdromCollection
description: A propriedade Count Obtém o número de unidades de CD e DVD disponíveis no sistema.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- Propriedade Count Windows Media Player
- Propriedade Count Windows Media Player, interface IWMPCdromCollection
- Interface IWMPCdromCollection Windows Media Player, Propriedade Count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766423"
---
# <a name="iwmpcdromcollectioncount-property"></a><span data-ttu-id="32eb3-106">Propriedade IWMPCdromCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="32eb3-106">IWMPCdromCollection::count property</span></span>

<span data-ttu-id="32eb3-107">A propriedade **Count** Obtém o número de unidades de CD e DVD disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="32eb3-107">The **count** property gets the number of available CD and DVD drives on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="32eb3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="32eb3-108">Syntax</span></span>


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="32eb3-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="32eb3-109">Property value</span></span>

<span data-ttu-id="32eb3-110">Um **System. Int32** que é a contagem de unidades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="32eb3-110">A **System.Int32** that is the count of available drives.</span></span>

## <a name="remarks"></a><span data-ttu-id="32eb3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="32eb3-111">Remarks</span></span>

<span data-ttu-id="32eb3-112">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="32eb3-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="32eb3-113">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="32eb3-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="32eb3-114">As unidades de DVD são contadas exatamente como unidades de CD.</span><span class="sxs-lookup"><span data-stu-id="32eb3-114">DVD drives are counted exactly like CD drives.</span></span> <span data-ttu-id="32eb3-115">No entanto, o controle ActiveX do Windows Media Player só dá suporte à funcionalidade de DVD para o Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="32eb3-115">However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later.</span></span> <span data-ttu-id="32eb3-116">Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídias em DVD.</span><span class="sxs-lookup"><span data-stu-id="32eb3-116">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

## <a name="examples"></a><span data-ttu-id="32eb3-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="32eb3-117">Examples</span></span>

<span data-ttu-id="32eb3-118">O exemplo a seguir usa Count para exibir o número de unidades de CD e DVD disponíveis em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="32eb3-118">The following example uses count to display the number of available CD and DVD drives in a message box.</span></span> <span data-ttu-id="32eb3-119">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="32eb3-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a><span data-ttu-id="32eb3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32eb3-120">Requirements</span></span>



| <span data-ttu-id="32eb3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="32eb3-121">Requirement</span></span> | <span data-ttu-id="32eb3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="32eb3-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32eb3-123">Versão</span><span class="sxs-lookup"><span data-stu-id="32eb3-123">Version</span></span><br/>   | <span data-ttu-id="32eb3-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="32eb3-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="32eb3-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="32eb3-125">Namespace</span></span><br/> | <span data-ttu-id="32eb3-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="32eb3-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="32eb3-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="32eb3-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="32eb3-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="32eb3-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32eb3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="32eb3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32eb3-130">**Interface IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="32eb3-130">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="32eb3-131">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="32eb3-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="32eb3-132">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="32eb3-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





