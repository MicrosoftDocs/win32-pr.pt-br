---
description: Coleção de objetos DeviceInfo que representa todos os dispositivos instalados no computador.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Propriedade WIA. Devices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b4d98bfe1552156071efde0b46899ad058e75aec
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841308"
---
# <a name="wiadevices-property"></a><span data-ttu-id="3988e-103">Propriedade WIA. Devices</span><span class="sxs-lookup"><span data-stu-id="3988e-103">Wia.Devices property</span></span>

<span data-ttu-id="3988e-104">Coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) que representa todos os dispositivos instalados no computador.</span><span class="sxs-lookup"><span data-stu-id="3988e-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="3988e-105">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3988e-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="3988e-106">Esta coleção é baseada em 0.</span><span class="sxs-lookup"><span data-stu-id="3988e-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="3988e-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3988e-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3988e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3988e-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="3988e-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3988e-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="3988e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3988e-110">Examples</span></span>

<span data-ttu-id="3988e-111">O exemplo a seguir ilustra o uso da coleção **Devices** para enumerar os dispositivos em um sistema.</span><span class="sxs-lookup"><span data-stu-id="3988e-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="3988e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3988e-112">Requirements</span></span>



| <span data-ttu-id="3988e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3988e-113">Requirement</span></span> | <span data-ttu-id="3988e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3988e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3988e-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3988e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3988e-116">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3988e-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3988e-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3988e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3988e-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3988e-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3988e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3988e-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3988e-120"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3988e-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




