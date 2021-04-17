---
title: Propriedade IWMPCdrom driveSpecifier
description: A propriedade driveSpecifier Obtém a letra da unidade de CD ou DVD.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- Propriedade driveSpecifier Windows Media Player
- Propriedade driveSpecifier Windows Media Player, interface IWMPCdrom
- Interface IWMPCdrom Windows Media Player, Propriedade driveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811591"
---
# <a name="iwmpcdromdrivespecifier-property"></a><span data-ttu-id="06746-106">IWMPCdrom: Propriedade riveSpecifier de:d</span><span class="sxs-lookup"><span data-stu-id="06746-106">IWMPCdrom::driveSpecifier property</span></span>

<span data-ttu-id="06746-107">A propriedade **driveSpecifier** Obtém a letra da unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="06746-107">The **driveSpecifier** property gets the CD or DVD drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="06746-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06746-108">Syntax</span></span>


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a><span data-ttu-id="06746-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="06746-109">Property value</span></span>

<span data-ttu-id="06746-110">Um **System. String** que é a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="06746-110">A **System.String** that is the drive letter.</span></span>

## <a name="remarks"></a><span data-ttu-id="06746-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="06746-111">Remarks</span></span>

<span data-ttu-id="06746-112">Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídias em DVD.</span><span class="sxs-lookup"><span data-stu-id="06746-112">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="06746-113">Essa propriedade Obtém uma letra da unidade para um índice de unidade com base em zero dentro do intervalo recuperado usando **IWMPCdromCollection. Count**.</span><span class="sxs-lookup"><span data-stu-id="06746-113">This property gets a drive letter for a zero-based drive index within the range retrieved using **IWMPCdromCollection.count**.</span></span> <span data-ttu-id="06746-114">O valor recuperado assume a forma *X*:, em que *X* representa a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="06746-114">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="06746-115">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="06746-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="06746-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="06746-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="06746-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06746-117">Examples</span></span>

<span data-ttu-id="06746-118">O exemplo a seguir usa **driveSpecifier** para criar uma cadeia de caracteres que contém uma lista de unidades de CD e DVD disponíveis e exibe essa cadeia de caracteres em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="06746-118">The following example uses **driveSpecifier** to build a string that contains a list of available CD and DVD drives and displays that string in a message box.</span></span> <span data-ttu-id="06746-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="06746-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a><span data-ttu-id="06746-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06746-120">Requirements</span></span>



| <span data-ttu-id="06746-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="06746-121">Requirement</span></span> | <span data-ttu-id="06746-122">Valor</span><span class="sxs-lookup"><span data-stu-id="06746-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06746-123">Versão</span><span class="sxs-lookup"><span data-stu-id="06746-123">Version</span></span><br/>   | <span data-ttu-id="06746-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="06746-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="06746-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="06746-125">Namespace</span></span><br/> | <span data-ttu-id="06746-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="06746-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="06746-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="06746-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="06746-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="06746-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06746-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="06746-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06746-130">**Interface IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="06746-130">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06746-131">**IWMPCdromCollection. Count (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="06746-131">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06746-132">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="06746-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06746-133">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="06746-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





