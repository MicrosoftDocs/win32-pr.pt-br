---
description: O método GetPropById do objeto DeviceInfo usa a ID de uma propriedade de dispositivo para retornar seu valor.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Método DeviceInfo. GetPropById
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766556"
---
# <a name="deviceinfogetpropbyid-method"></a><span data-ttu-id="31dff-103">Método DeviceInfo. GetPropById</span><span class="sxs-lookup"><span data-stu-id="31dff-103">DeviceInfo.GetPropById method</span></span>

<span data-ttu-id="31dff-104">O método **GetPropById** do objeto [**DEVICEINFO**](-wia-deviceinfo.md) usa a ID de uma propriedade de dispositivo para retornar seu valor.</span><span class="sxs-lookup"><span data-stu-id="31dff-104">The **GetPropById** method of the [**DeviceInfo**](-wia-deviceinfo.md) object uses a device property's ID to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="31dff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31dff-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="31dff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31dff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31dff-107">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="31dff-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31dff-108">Tipo: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="31dff-108">Type: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span></span>

<span data-ttu-id="31dff-109">Especifica a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="31dff-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31dff-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31dff-110">Return value</span></span>

<span data-ttu-id="31dff-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="31dff-111">Type: **VARIANT**</span></span>

<span data-ttu-id="31dff-112">Esse método retorna o valor da propriedade especificada por *ID*.</span><span class="sxs-lookup"><span data-stu-id="31dff-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="31dff-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="31dff-113">Remarks</span></span>

<span data-ttu-id="31dff-114">Use esse método para localizar o valor de uma propriedade de dispositivo de sua ID.</span><span class="sxs-lookup"><span data-stu-id="31dff-114">Use this method to find the value of a device property from its ID.</span></span> <span data-ttu-id="31dff-115">Para obter uma lista de IDs de propriedade, consulte [definições de constante de propriedade WIA](-wia-wia-property-constant-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="31dff-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="31dff-116">Para obter informações sobre as próprias propriedades de aquisição de imagem do Windows (WIA), consulte [constantes da propriedade WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="31dff-116">For information about Windows Image Acquisition (WIA) properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="31dff-117">Para aplicativos Microsoft Visual Basic, adicione uma referência a "biblioteca de tipos do Windows Image Acquisition 1, 1".</span><span class="sxs-lookup"><span data-stu-id="31dff-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="31dff-118">Estas constantes definidas nesse arquivo são válidas para este método:</span><span class="sxs-lookup"><span data-stu-id="31dff-118">This following constants defined in that file are valid for this method:</span></span>

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a><span data-ttu-id="31dff-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31dff-119">Examples</span></span>

<span data-ttu-id="31dff-120">O exemplo a seguir demonstra o uso do método **GetPropById** para recuperar um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="31dff-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="31dff-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31dff-121">Requirements</span></span>



| <span data-ttu-id="31dff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31dff-122">Requirement</span></span> | <span data-ttu-id="31dff-123">Valor</span><span class="sxs-lookup"><span data-stu-id="31dff-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dff-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31dff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31dff-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31dff-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31dff-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31dff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31dff-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31dff-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="31dff-128">DLL</span><span class="sxs-lookup"><span data-stu-id="31dff-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31dff-129"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="31dff-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




