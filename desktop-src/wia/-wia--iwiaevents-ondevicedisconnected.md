---
description: Evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem do Windows) está desconectado.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento WIA. OnDeviceDisconnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169548"
---
# <a name="wiaondevicedisconnected-event"></a><span data-ttu-id="c6e4d-103">Evento WIA. OnDeviceDisconnected</span><span class="sxs-lookup"><span data-stu-id="c6e4d-103">Wia.OnDeviceDisconnected event</span></span>

<span data-ttu-id="c6e4d-104">Evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem do Windows) está desconectado.</span><span class="sxs-lookup"><span data-stu-id="c6e4d-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is disconnected.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e4d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6e4d-105">Syntax</span></span>


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="c6e4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6e4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6e4d-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="c6e4d-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="c6e4d-108">Uma cadeia de caracteres que contém a ID do dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="c6e4d-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6e4d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6e4d-109">Return value</span></span>

<span data-ttu-id="c6e4d-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c6e4d-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e4d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6e4d-111">Remarks</span></span>

<span data-ttu-id="c6e4d-112">O WIA notifica o script ou o aplicativo sempre que um dispositivo de hardware é desconectado do computador.</span><span class="sxs-lookup"><span data-stu-id="c6e4d-112">WIA notifies the script or application whenever a hardware device is disconnected from the computer.</span></span> <span data-ttu-id="c6e4d-113">Implemente a sub-rotina **objWia** \_ **OnDeviceDisconnected ()** para permitir que o script ou o aplicativo respondam à desconexão do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6e4d-113">Implement the **objWia**\_**OnDeviceDisconnected()** subroutine to allow the script or application to respond to the device disconnection.</span></span>

<span data-ttu-id="c6e4d-114">Por exemplo, talvez você queira que um script atualize a coleção de [**dispositivos**](-wia-iwia-devices.md) quando um dispositivo for removido do computador.</span><span class="sxs-lookup"><span data-stu-id="c6e4d-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a device is removed from the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e4d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6e4d-115">Requirements</span></span>



| <span data-ttu-id="c6e4d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6e4d-116">Requirement</span></span> | <span data-ttu-id="c6e4d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c6e4d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e4d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6e4d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e4d-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c6e4d-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6e4d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6e4d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e4d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c6e4d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c6e4d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c6e4d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6e4d-123"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c6e4d-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




