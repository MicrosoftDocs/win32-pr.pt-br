---
description: Usado por aplicativos para exibir uma caixa de diálogo de dispositivo para o usuário.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Função DeviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790552"
---
# <a name="devicedialog-function"></a><span data-ttu-id="bfe8f-103">Função DeviceDialog</span><span class="sxs-lookup"><span data-stu-id="bfe8f-103">DeviceDialog function</span></span>

<span data-ttu-id="bfe8f-104">Usado por aplicativos para exibir uma caixa de diálogo de dispositivo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-104">Used by applications to display a device dialog box to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfe8f-105">Syntax</span></span>


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="bfe8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfe8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfe8f-107">*pDeviceDialogData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bfe8f-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfe8f-108">Tipo: **PDEVICEDIALOGDATA**</span><span class="sxs-lookup"><span data-stu-id="bfe8f-108">Type: **PDEVICEDIALOGDATA**</span></span>

<span data-ttu-id="bfe8f-109">O [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) a ser usado para criar a caixa de diálogo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-109">The [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) to use to create the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfe8f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bfe8f-110">Return value</span></span>

<span data-ttu-id="bfe8f-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bfe8f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="bfe8f-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bfe8f-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bfe8f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe8f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfe8f-114">Requirements</span></span>



| <span data-ttu-id="bfe8f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfe8f-115">Requirement</span></span> | <span data-ttu-id="bfe8f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe8f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe8f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfe8f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe8f-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bfe8f-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bfe8f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfe8f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe8f-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bfe8f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bfe8f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bfe8f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe8f-122"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfe8f-122"><dt>Wiadevd.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfe8f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfe8f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bfe8f-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfe8f-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfe8f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfe8f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe8f-126">**DEVICEDIALOGDATA**</span><span class="sxs-lookup"><span data-stu-id="bfe8f-126">**DEVICEDIALOGDATA**</span></span>](-wia-devicedialogdata.md)
</dt> </dl>

 

 




