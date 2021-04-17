---
description: O método Create do objeto DeviceInfo faz uma conexão com o dispositivo de aquisição de imagens do Windows (WIA) especificado pelo objeto DeviceInfo e retorna um objeto item que representa o dispositivo.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: Método DeviceInfo. Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790413"
---
# <a name="deviceinfocreate-method"></a><span data-ttu-id="8aea5-103">Método DeviceInfo. Create</span><span class="sxs-lookup"><span data-stu-id="8aea5-103">DeviceInfo.Create method</span></span>

<span data-ttu-id="8aea5-104">O método **Create** do objeto [**DeviceInfo**](-wia-deviceinfo.md) faz uma conexão com o dispositivo de aquisição de imagens do Windows (WIA) especificado pelo objeto **DeviceInfo** e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8aea5-104">The **Create** method of the [**DeviceInfo**](-wia-deviceinfo.md) object makes a connection to the Windows Image Acquisition (WIA) device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aea5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8aea5-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a><span data-ttu-id="8aea5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8aea5-106">Parameters</span></span>

<span data-ttu-id="8aea5-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8aea5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8aea5-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8aea5-108">Return value</span></span>

<span data-ttu-id="8aea5-109">Tipo: **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="8aea5-109">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="8aea5-110">Esse método retorna o objeto [**Item**](-wia-item.md) que representa o dispositivo criado.</span><span class="sxs-lookup"><span data-stu-id="8aea5-110">This method returns the [**Item**](-wia-item.md) object that represents the device that is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aea5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8aea5-111">Remarks</span></span>

<span data-ttu-id="8aea5-112">Use o método **Create** para criar uma conexão com um dispositivo de hardware WIA depois de enumerar a coleção de [**dispositivos**](-wia-iwia-devices.md) .</span><span class="sxs-lookup"><span data-stu-id="8aea5-112">Use the **Create** method to create a connection to a WIA hardware device after enumerating the [**Devices**](-wia-iwia-devices.md) collection.</span></span> <span data-ttu-id="8aea5-113">O método retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo (um item raiz).</span><span class="sxs-lookup"><span data-stu-id="8aea5-113">The method returns an [**Item**](-wia-item.md) object that represents the device (a root item).</span></span>

## <a name="examples"></a><span data-ttu-id="8aea5-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8aea5-114">Examples</span></span>

<span data-ttu-id="8aea5-115">O exemplo a seguir demonstra o uso do método **Create** .</span><span class="sxs-lookup"><span data-stu-id="8aea5-115">The following example demonstrates the use of the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="8aea5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aea5-116">Requirements</span></span>



| <span data-ttu-id="8aea5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aea5-117">Requirement</span></span> | <span data-ttu-id="8aea5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8aea5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aea5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8aea5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8aea5-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8aea5-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8aea5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8aea5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8aea5-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8aea5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8aea5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8aea5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8aea5-124"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8aea5-124"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




