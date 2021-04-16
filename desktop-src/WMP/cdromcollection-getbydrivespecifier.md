---
title: Método cdromCollection. getByDriveSpecifier
description: O método getByDriveSpecifier recupera o objeto de cdrom associado a uma letra de unidade específica.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- método getByDriveSpecifier Windows Media Player
- método getByDriveSpecifier Windows Media Player, classe cdromCollection
- Classe cdromCollection Windows Media Player, método getByDriveSpecifier
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794503"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="6293a-106">Método cdromCollection. getByDriveSpecifier</span><span class="sxs-lookup"><span data-stu-id="6293a-106">CdromCollection.getByDriveSpecifier method</span></span>

<span data-ttu-id="6293a-107">O método **getByDriveSpecifier** recupera o objeto de **cdrom** associado a uma letra de unidade específica.</span><span class="sxs-lookup"><span data-stu-id="6293a-107">The **getByDriveSpecifier** method retrieves the **Cdrom** object associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6293a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6293a-108">Syntax</span></span>


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a><span data-ttu-id="6293a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6293a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6293a-110">*driveSpecifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6293a-110">*driveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6293a-111">**Cadeia de caracteres** que contém a letra da unidade seguida por um caractere de dois-pontos (":").</span><span class="sxs-lookup"><span data-stu-id="6293a-111">**String** containing the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6293a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6293a-112">Return value</span></span>

<span data-ttu-id="6293a-113">Esse método retorna um objeto de **cdrom** .</span><span class="sxs-lookup"><span data-stu-id="6293a-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6293a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6293a-114">Remarks</span></span>

<span data-ttu-id="6293a-115">As letras da unidade devem ser fornecidas no formato *x*:, em que *X* representa a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="6293a-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="6293a-116">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6293a-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="6293a-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6293a-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6293a-118">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="6293a-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6293a-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6293a-119">Examples</span></span>

<span data-ttu-id="6293a-120">O exemplo de JScript a seguir usa *cdromCollection*. **getByDriveSpecifier** para recuperar o objeto de **cdrom** que corresponde a uma letra de unidade fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6293a-120">The following JScript example uses *CdromCollection*.**getByDriveSpecifier** to retrieve the **Cdrom** object that corresponds to a drive letter provided by the user.</span></span> <span data-ttu-id="6293a-121">Um elemento de texto HTML foi criado, com NAME = "MyText", para entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="6293a-121">An HTML text element was created, with NAME = "MyText", for user input.</span></span> <span data-ttu-id="6293a-122">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6293a-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a><span data-ttu-id="6293a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6293a-123">Requirements</span></span>



| <span data-ttu-id="6293a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6293a-124">Requirement</span></span> | <span data-ttu-id="6293a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6293a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6293a-126">Versão</span><span class="sxs-lookup"><span data-stu-id="6293a-126">Version</span></span><br/> | <span data-ttu-id="6293a-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6293a-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6293a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6293a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="6293a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6293a-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6293a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6293a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6293a-131">**Objeto cdrom**</span><span class="sxs-lookup"><span data-stu-id="6293a-131">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="6293a-132">**Cdrom. ejeção**</span><span class="sxs-lookup"><span data-stu-id="6293a-132">**Cdrom.eject**</span></span>](cdrom-eject.md)
</dt> <dt>

[<span data-ttu-id="6293a-133">**Objeto cdromCollection**</span><span class="sxs-lookup"><span data-stu-id="6293a-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="6293a-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6293a-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="6293a-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6293a-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





