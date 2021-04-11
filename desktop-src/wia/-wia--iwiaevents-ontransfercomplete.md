---
description: Evento que ocorre quando uma transferência de dados é concluída com êxito.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento WIA. OnTransferComplete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169547"
---
# <a name="wiaontransfercomplete-event"></a><span data-ttu-id="ac3cc-103">Evento WIA. OnTransferComplete</span><span class="sxs-lookup"><span data-stu-id="ac3cc-103">Wia.OnTransferComplete event</span></span>

<span data-ttu-id="ac3cc-104">Evento que ocorre quando uma transferência de dados é concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="ac3cc-104">Event that occurs when a data transfer is completed successfully.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac3cc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac3cc-105">Syntax</span></span>


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="ac3cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac3cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac3cc-107">*Item*</span><span class="sxs-lookup"><span data-stu-id="ac3cc-107">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="ac3cc-108">O objeto [**Item**](-wia-item.md) transferido.</span><span class="sxs-lookup"><span data-stu-id="ac3cc-108">The [**Item**](-wia-item.md) object transferred.</span></span>

</dd> <dt>

<span data-ttu-id="ac3cc-109">*Caminho*</span><span class="sxs-lookup"><span data-stu-id="ac3cc-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="ac3cc-110">O caminho e o nome do arquivo da imagem transferida.</span><span class="sxs-lookup"><span data-stu-id="ac3cc-110">The path and file name of the transferred image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac3cc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac3cc-111">Return value</span></span>

<span data-ttu-id="ac3cc-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ac3cc-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac3cc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac3cc-113">Remarks</span></span>

<span data-ttu-id="ac3cc-114">O WIA notifica o script ou o aplicativo quando uma transferência de dados, imagem ou som é concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="ac3cc-114">WIA notifies the script or application when a data transfer, image or sound, completes successfully.</span></span> <span data-ttu-id="ac3cc-115">Implemente a sub-rotina **objWia** \_ **OnTransferComplete ()** para permitir que seu script ou aplicativo responda à conclusão da transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="ac3cc-115">Implement the **objWia**\_**OnTransferComplete()** subroutine to allow your script or application to respond to the completion of the data transfer.</span></span>

<span data-ttu-id="ac3cc-116">Por exemplo, talvez você queira que um script exiba uma imagem depois que ela for transferida.</span><span class="sxs-lookup"><span data-stu-id="ac3cc-116">For example, you might want a script to display an image after it is transferred.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac3cc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac3cc-117">Requirements</span></span>



| <span data-ttu-id="ac3cc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac3cc-118">Requirement</span></span> | <span data-ttu-id="ac3cc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3cc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3cc-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac3cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac3cc-121">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ac3cc-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac3cc-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac3cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac3cc-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ac3cc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ac3cc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ac3cc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac3cc-125"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ac3cc-125"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




