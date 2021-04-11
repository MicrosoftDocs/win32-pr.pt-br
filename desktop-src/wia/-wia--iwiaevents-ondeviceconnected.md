---
description: Evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem do Windows) está conectado.
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Evento WIA. OnDeviceConnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169549"
---
# <a name="wiaondeviceconnected-event"></a><span data-ttu-id="2040d-103">Evento WIA. OnDeviceConnected</span><span class="sxs-lookup"><span data-stu-id="2040d-103">Wia.OnDeviceConnected event</span></span>

<span data-ttu-id="2040d-104">Evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem do Windows) está conectado.</span><span class="sxs-lookup"><span data-stu-id="2040d-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="2040d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2040d-105">Syntax</span></span>


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="2040d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2040d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2040d-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="2040d-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="2040d-108">Uma cadeia de caracteres que contém a ID do dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="2040d-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2040d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2040d-109">Return value</span></span>

<span data-ttu-id="2040d-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2040d-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2040d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2040d-111">Remarks</span></span>

<span data-ttu-id="2040d-112">O WIA notifica o script ou o aplicativo sempre que um novo dispositivo de hardware estiver conectado ao computador.</span><span class="sxs-lookup"><span data-stu-id="2040d-112">WIA notifies the script or application whenever a new hardware device is connected to the computer.</span></span> <span data-ttu-id="2040d-113">Implemente a sub-rotina **objWia** \_ **OnDeviceConnected ()** para permitir que o script ou o aplicativo respondam à conexão do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2040d-113">Implement the **objWia**\_**OnDeviceConnected()** subroutine to allow the script or application to respond to the device connection.</span></span>

<span data-ttu-id="2040d-114">Por exemplo, talvez você queira que um script atualize a coleção de [**dispositivos**](-wia-iwia-devices.md) quando um novo dispositivo for instalado.</span><span class="sxs-lookup"><span data-stu-id="2040d-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a new device is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2040d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2040d-115">Requirements</span></span>



| <span data-ttu-id="2040d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2040d-116">Requirement</span></span> | <span data-ttu-id="2040d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2040d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2040d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2040d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2040d-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2040d-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2040d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2040d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2040d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2040d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2040d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2040d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2040d-123"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2040d-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




