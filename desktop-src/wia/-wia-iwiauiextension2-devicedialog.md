---
description: Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: 'IWiaUIExtension2: método eviceDialog de:D (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164526"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="c6ec1-103">IWiaUIExtension2: método eviceDialog de:D</span><span class="sxs-lookup"><span data-stu-id="c6ec1-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="c6ec1-104">Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ec1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6ec1-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="c6ec1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6ec1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6ec1-107">*pDeviceDialogData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6ec1-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ec1-108">Tipo: \**PDEVICEDIALOGDATA2 \** _</span><span class="sxs-lookup"><span data-stu-id="c6ec1-108">Type: \**PDEVICEDIALOGDATA2\** _</span></span>

<span data-ttu-id="c6ec1-109">Aponta para uma estrutura [_ *DEVICEDIALOGDATA2* \*](-wia-devicedialogdata2.md) que contém todos os dados necessários para implementar a caixa de diálogo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-109">Points to a [_ *DEVICEDIALOGDATA2*\*](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6ec1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6ec1-110">Return value</span></span>

<span data-ttu-id="c6ec1-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c6ec1-111">Type: **HRESULT**</span></span>

<span data-ttu-id="c6ec1-112">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c6ec1-113">Se o usuário cancelar a caixa de diálogo, o método retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="c6ec1-114">Se o método falhar, ele retornará um código de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="c6ec1-115">A tabela a seguir mostra alguns dos possíveis códigos de status de retorno.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="c6ec1-116">Código do erro</span><span class="sxs-lookup"><span data-stu-id="c6ec1-116">Error code</span></span>    | <span data-ttu-id="c6ec1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6ec1-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="c6ec1-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c6ec1-118">E\_INVALIDARG</span></span> | <span data-ttu-id="c6ec1-119">O parâmetro pDeviceDialogData é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="c6ec1-120">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c6ec1-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="c6ec1-121">O método não está implementado.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="c6ec1-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6ec1-122">Remarks</span></span>

<span data-ttu-id="c6ec1-123">Se você implementar a interface [**IWiaUIExtension2**](-wia-iwiauiextension2.md) e não quiser substituir a interface do usuário do sistema, esse método ainda deverá ser implementado, mas não deverá fazer nada mais do que Return E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ec1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6ec1-124">Requirements</span></span>



| <span data-ttu-id="c6ec1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ec1-125">Requirement</span></span> | <span data-ttu-id="c6ec1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c6ec1-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ec1-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6ec1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ec1-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6ec1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c6ec1-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6ec1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ec1-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6ec1-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c6ec1-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6ec1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6ec1-132"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6ec1-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




