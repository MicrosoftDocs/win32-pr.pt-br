---
description: O método GetItemsFromUI do objeto item exibe uma caixa de diálogo que permite que um usuário selecione imagens e áudio para transferir de um dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Método item. GetItemsFromUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090806"
---
# <a name="itemgetitemsfromui-method"></a><span data-ttu-id="4d654-103">Método item. GetItemsFromUI</span><span class="sxs-lookup"><span data-stu-id="4d654-103">Item.GetItemsFromUI method</span></span>

<span data-ttu-id="4d654-104">O método **GetItemsFromUI** do objeto [**Item**](-wia-item.md) exibe uma caixa de diálogo que permite que um usuário selecione imagens e áudio para transferir de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d654-104">The **GetItemsFromUI** method of the [**Item**](-wia-item.md) object displays a dialog box that allows a user to select images and audio to transfer from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d654-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d654-105">Syntax</span></span>


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a><span data-ttu-id="4d654-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d654-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d654-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4d654-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d654-108">Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**</span><span class="sxs-lookup"><span data-stu-id="4d654-108">Type: **[**WiaFlag**](-wia-wiaflag.md)**</span></span>

<dt>



 <span data-ttu-id="4d654-109"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="4d654-109">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4d654-110">Padrão.</span><span class="sxs-lookup"><span data-stu-id="4d654-110">Default.</span></span> <span data-ttu-id="4d654-111">\[no \] especifica o comportamento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4d654-111">\[in\] Specifies dialog box behavior.</span></span> <span data-ttu-id="4d654-112">Os valores válidos para esse parâmetro são os mesmos para o parâmetro *lFlags* do método [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .</span><span class="sxs-lookup"><span data-stu-id="4d654-112">The valid values for this parameter are the same as for the *lFlags* parameter of the [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) method.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4d654-113">*Intenção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d654-113">*Intent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d654-114">Tipo: **WiaIntent**</span><span class="sxs-lookup"><span data-stu-id="4d654-114">Type: **WiaIntent**</span></span>

<dt>



 <span data-ttu-id="4d654-115"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="4d654-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4d654-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="4d654-116">Default.</span></span> <span data-ttu-id="4d654-117">\[em \] especifica o tipo de dados que a imagem deve representar.</span><span class="sxs-lookup"><span data-stu-id="4d654-117">\[in\] Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="4d654-118">Para obter uma lista de valores de intenção de imagem, consulte [**constantes de objetivo de imagem**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="4d654-118">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d654-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d654-119">Return value</span></span>

<span data-ttu-id="4d654-120">Tipo: **ICollection**</span><span class="sxs-lookup"><span data-stu-id="4d654-120">Type: **ICollection**</span></span>

<span data-ttu-id="4d654-121">Esse método retorna uma coleção de objetos de [**Item**](-wia-item.md) que representam os itens selecionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4d654-121">This method returns a collection of [**Item**](-wia-item.md) objects that represent the items selected by the user.</span></span> <span data-ttu-id="4d654-122">Se nenhum item for selecionado, a coleção estará vazia.</span><span class="sxs-lookup"><span data-stu-id="4d654-122">If no items are selected, the collection is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d654-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d654-123">Remarks</span></span>

<span data-ttu-id="4d654-124">Para aplicativos Microsoft Visual Basic, adicione uma referência a "biblioteca de tipos do Windows Image Acquisition 1, 1".</span><span class="sxs-lookup"><span data-stu-id="4d654-124">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span>

<span data-ttu-id="4d654-125">Esse método se aplica somente a dispositivos (itens raiz).</span><span class="sxs-lookup"><span data-stu-id="4d654-125">This method applies only to devices (root items).</span></span> <span data-ttu-id="4d654-126">O método retorna uma coleção de objetos de [**Item**](-wia-item.md) que representam as imagens ou os clipes de áudio selecionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4d654-126">The method returns a collection of [**Item**](-wia-item.md) objects that represent the images or audio clips selected by the user.</span></span>

<span data-ttu-id="4d654-127">Se nenhum item for selecionado pelo usuário, o método retornará uma coleção vazia.</span><span class="sxs-lookup"><span data-stu-id="4d654-127">If no items are selected by the user, the method returns an empty collection.</span></span>

## <a name="examples"></a><span data-ttu-id="4d654-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d654-128">Examples</span></span>

<span data-ttu-id="4d654-129">O exemplo a seguir demonstra o uso do método **GetItemsFromUI** para permitir que um usuário selecione imagens em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4d654-129">The following example demonstrates the use of the **GetItemsFromUI** method to allow a user to select images from a dialog box.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="4d654-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d654-130">Requirements</span></span>



| <span data-ttu-id="4d654-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d654-131">Requirement</span></span> | <span data-ttu-id="4d654-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4d654-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d654-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d654-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4d654-134">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4d654-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d654-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d654-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4d654-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d654-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4d654-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4d654-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d654-138"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4d654-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




