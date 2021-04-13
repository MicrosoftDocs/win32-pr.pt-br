---
description: Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: 'IWiaUIExtension: método eviceDialog de:D (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 7d42d0c7f8cca510a9c8f78de7bf589f8e1d2d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501787"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="f2e65-103">IWiaUIExtension: método eviceDialog de:D</span><span class="sxs-lookup"><span data-stu-id="f2e65-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="f2e65-104">Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e65-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e65-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2e65-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="f2e65-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2e65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e65-107">*pDeviceDialogData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2e65-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e65-108">Tipo: \**PDEVICEDIALOGDATA \** _</span><span class="sxs-lookup"><span data-stu-id="f2e65-108">Type: \**PDEVICEDIALOGDATA\** _</span></span>

<span data-ttu-id="f2e65-109">Aponta para uma estrutura [_ *DEVICEDIALOGDATA* \*](-wia-devicedialogdata.md) que contém todos os dados necessários para implementar a caixa de diálogo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2e65-109">Points to a [_ *DEVICEDIALOGDATA*\*](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e65-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2e65-110">Return value</span></span>

<span data-ttu-id="f2e65-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f2e65-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f2e65-112">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2e65-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="f2e65-113">Se o usuário cancelar a caixa de diálogo, o método retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="f2e65-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="f2e65-114">Se o método não for implementado, ele retornará E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f2e65-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="f2e65-115">Se o método falhar, ele retornará um código de erro COM padrão.</span><span class="sxs-lookup"><span data-stu-id="f2e65-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e65-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2e65-116">Remarks</span></span>

<span data-ttu-id="f2e65-117">Se você implementar a interface [**IWiaUIExtension**](-wia-iwiauiextension.md) e não quiser substituir a interface do usuário do sistema, esse método ainda deverá ser implementado, mas não deverá fazer nada mais do que Return E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f2e65-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e65-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2e65-118">Requirements</span></span>



| <span data-ttu-id="f2e65-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e65-119">Requirement</span></span> | <span data-ttu-id="f2e65-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f2e65-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e65-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2e65-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e65-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2e65-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f2e65-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2e65-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e65-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2e65-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f2e65-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2e65-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e65-126"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e65-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




