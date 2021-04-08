---
description: O método TakePicture do objeto item faz com que um dispositivo de câmera digital pegue uma imagem e retorna um objeto item que representa a imagem resultante. Esse método se aplica somente a dispositivos de câmera digital.
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: Método item. TakePicture (Wiavideo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921800"
---
# <a name="itemtakepicture-method"></a><span data-ttu-id="a703a-104">Método item. TakePicture</span><span class="sxs-lookup"><span data-stu-id="a703a-104">Item.TakePicture method</span></span>

<span data-ttu-id="a703a-105">O método **TakePicture** do objeto [**Item**](-wia-item.md) faz com que um dispositivo de câmera digital pegue uma imagem e retorna um objeto **Item** que representa a imagem resultante.</span><span class="sxs-lookup"><span data-stu-id="a703a-105">The **TakePicture** method of the [**Item**](-wia-item.md) object causes a digital camera device to take a picture and returns an **Item** object that represents the resulting image.</span></span> <span data-ttu-id="a703a-106">Esse método se aplica somente a dispositivos de câmera digital.</span><span class="sxs-lookup"><span data-stu-id="a703a-106">This method applies only to digital camera devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a703a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a703a-107">Syntax</span></span>


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a><span data-ttu-id="a703a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a703a-108">Parameters</span></span>

<span data-ttu-id="a703a-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a703a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a703a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a703a-110">Return value</span></span>

<span data-ttu-id="a703a-111">Tipo: **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="a703a-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="a703a-112">Um objeto [**Item**](-wia-item.md) que representa a imagem que esse método cria.</span><span class="sxs-lookup"><span data-stu-id="a703a-112">An [**Item**](-wia-item.md) object that represents the image that this method creates.</span></span>

## <a name="requirements"></a><span data-ttu-id="a703a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a703a-113">Requirements</span></span>



| <span data-ttu-id="a703a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a703a-114">Requirement</span></span> | <span data-ttu-id="a703a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a703a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a703a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a703a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a703a-117">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a703a-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a703a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a703a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a703a-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a703a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a703a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a703a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a703a-121"><dt>Wiavideo. h</dt></span><span class="sxs-lookup"><span data-stu-id="a703a-121"><dt>Wiavideo.h</dt></span></span> </dl>                         |
| <span data-ttu-id="a703a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a703a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a703a-123"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a703a-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




