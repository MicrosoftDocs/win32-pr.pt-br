---
title: Método IWMPCdromCollection getByDriveSpecifier
description: O método getByDriveSpecifier retorna uma interface IWMPCdrom associada a uma letra de unidade específica.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- método getByDriveSpecifier Windows Media Player
- método getByDriveSpecifier Windows Media Player, interface IWMPCdromCollection
- Interface IWMPCdromCollection Windows Media Player, método getByDriveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812001"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="bc0c5-106">Método IWMPCdromCollection:: getByDriveSpecifier</span><span class="sxs-lookup"><span data-stu-id="bc0c5-106">IWMPCdromCollection::getByDriveSpecifier method</span></span>

<span data-ttu-id="bc0c5-107">O método **getByDriveSpecifier** retorna uma interface **IWMPCdrom** associada a uma letra de unidade específica.</span><span class="sxs-lookup"><span data-stu-id="bc0c5-107">The **getByDriveSpecifier** method returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc0c5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc0c5-108">Syntax</span></span>


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a><span data-ttu-id="bc0c5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc0c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0c5-110">*bstrDriveSpecifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc0c5-110">*bstrDriveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c5-111">Um **System. String** que é a letra da unidade seguida por um caractere de dois-pontos (":").</span><span class="sxs-lookup"><span data-stu-id="bc0c5-111">A **System.String** that is the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc0c5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc0c5-112">Return value</span></span>

<span data-ttu-id="bc0c5-113">Uma interface **WMPLib. IWMPCdrom** .</span><span class="sxs-lookup"><span data-stu-id="bc0c5-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc0c5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc0c5-114">Remarks</span></span>

<span data-ttu-id="bc0c5-115">As letras da unidade devem ser fornecidas no formato *x*:, em que *X* representa a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="bc0c5-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="bc0c5-116">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bc0c5-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="bc0c5-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bc0c5-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bc0c5-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc0c5-118">Examples</span></span>

<span data-ttu-id="bc0c5-119">O exemplo a seguir usa **getByDriveSpecifier** para obter a interface **IWMPCdrom** que corresponde a uma letra de unidade fornecida pelo usuário em uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="bc0c5-119">The following example uses **getByDriveSpecifier** to get the **IWMPCdrom** interface that corresponds to a drive letter provided by the user in a text box.</span></span> <span data-ttu-id="bc0c5-120">O método **IWMPCdrom. EJECT** é chamado para ejetar a unidade especificada.</span><span class="sxs-lookup"><span data-stu-id="bc0c5-120">The **IWMPCdrom.eject** method is then called to eject the specified drive.</span></span> <span data-ttu-id="bc0c5-121">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="bc0c5-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a><span data-ttu-id="bc0c5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc0c5-122">Requirements</span></span>



| <span data-ttu-id="bc0c5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc0c5-123">Requirement</span></span> | <span data-ttu-id="bc0c5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bc0c5-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0c5-125">Versão</span><span class="sxs-lookup"><span data-stu-id="bc0c5-125">Version</span></span><br/>   | <span data-ttu-id="bc0c5-126">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="bc0c5-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bc0c5-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc0c5-127">Namespace</span></span><br/> | <span data-ttu-id="bc0c5-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bc0c5-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bc0c5-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="bc0c5-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bc0c5-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bc0c5-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc0c5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc0c5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0c5-132">**Interface IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bc0c5-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc0c5-133">**IWMPCdrom. EJECT (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bc0c5-133">**IWMPCdrom.eject (VB and C#)**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc0c5-134">**Interface IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bc0c5-134">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc0c5-135">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bc0c5-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc0c5-136">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bc0c5-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





