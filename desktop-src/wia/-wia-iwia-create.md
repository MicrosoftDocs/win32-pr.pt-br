---
description: O método Create do objeto WIA faz uma conexão com o dispositivo de aquisição de imagem do Windows (WIA) especificado e retorna um objeto item que representa o dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Método WIA. Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505893"
---
# <a name="wiacreate-method"></a><span data-ttu-id="b21bf-103">Método WIA. Create</span><span class="sxs-lookup"><span data-stu-id="b21bf-103">Wia.Create method</span></span>

<span data-ttu-id="b21bf-104">O método **Create** do objeto [**WIA**](-wia-wia.md) faz uma conexão com o dispositivo de aquisição de imagem do Windows (WIA) especificado e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b21bf-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b21bf-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="b21bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b21bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b21bf-107">*Dispositivo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b21bf-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21bf-108">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="b21bf-108">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="b21bf-109">Especifica o dispositivo WIA ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="b21bf-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b21bf-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b21bf-110">Return value</span></span>

<span data-ttu-id="b21bf-111">Tipo: _ *IWiaDispatchItem*\*</span><span class="sxs-lookup"><span data-stu-id="b21bf-111">Type: _ *IWiaDispatchItem*\*</span></span>

<span data-ttu-id="b21bf-112">Se for bem-sucedido, esse método retornará um objeto [**Item**](-wia-item.md) que representa um dispositivo de hardware WIA (um item raiz).</span><span class="sxs-lookup"><span data-stu-id="b21bf-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="b21bf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b21bf-113">Remarks</span></span>

<span data-ttu-id="b21bf-114">O parâmetro de *dispositivo* especifica um objeto [**DeviceInfo**](-wia-deviceinfo.md) passando o próprio objeto, seu índice de um objeto de coleção ou o valor de sua propriedade de [**ID**](-wia-iwiadeviceinfo-id.md) .</span><span class="sxs-lookup"><span data-stu-id="b21bf-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="b21bf-115">Não passe **nada** para exibir uma caixa de diálogo que permita que um usuário selecione um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b21bf-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="b21bf-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b21bf-116">Examples</span></span>

<span data-ttu-id="b21bf-117">Os exemplos de VBScript a seguir demonstram o uso do método **Create** .</span><span class="sxs-lookup"><span data-stu-id="b21bf-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="b21bf-118">O primeiro exemplo passa um objeto [**DeviceInfo**](-wia-deviceinfo.md) para o método **Create** .</span><span class="sxs-lookup"><span data-stu-id="b21bf-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="b21bf-119">Observe que a passagem da propriedade [**ID**](-wia-iwiadeviceinfo-id.md) do objeto causa exatamente o mesmo comportamento.</span><span class="sxs-lookup"><span data-stu-id="b21bf-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



<span data-ttu-id="b21bf-120">No próximo exemplo, o aplicativo de chamada passa o índice do objeto [**DeviceInfo**](-wia-deviceinfo.md) na coleção para o método **Create** .</span><span class="sxs-lookup"><span data-stu-id="b21bf-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



<span data-ttu-id="b21bf-121">O exemplo a seguir não transmite **nada** para o método **Create** para exibir uma caixa de diálogo que permite que um usuário selecione um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b21bf-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="b21bf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b21bf-122">Requirements</span></span>



| <span data-ttu-id="b21bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b21bf-123">Requirement</span></span> | <span data-ttu-id="b21bf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b21bf-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b21bf-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b21bf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b21bf-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b21bf-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b21bf-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b21bf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b21bf-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b21bf-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b21bf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b21bf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b21bf-130"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b21bf-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




