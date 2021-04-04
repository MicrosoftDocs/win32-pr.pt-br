---
title: WM/ASFSecurityObjectsSize
description: O atributo WM/ASFSecurityObjectsSize contém o tamanho, em bytes, dos objetos relacionados ao DRM no cabeçalho do arquivo ASF.
ms.assetid: 40ea619a-1042-4d1b-a855-d80c93202765
keywords:
- Formato de mídia do Windows do WM/ASFSecurityObjectsSize
topic_type:
- apiref
api_name:
- WM/ASFSecurityObjectsSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de28f2169e5ac854163854ac95959d941100aaae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007090"
---
# <a name="wmasfsecurityobjectssize"></a><span data-ttu-id="8d18e-104">WM/ASFSecurityObjectsSize</span><span class="sxs-lookup"><span data-stu-id="8d18e-104">WM/ASFSecurityObjectsSize</span></span>

<span data-ttu-id="8d18e-105">O atributo **WM/ASFSecurityObjectsSize** contém o tamanho, em bytes, dos objetos relacionados ao DRM no cabeçalho do arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="8d18e-105">The **WM/ASFSecurityObjectsSize** attribute contains the size, in bytes, of the DRM-related objects in the header of the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8d18e-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="8d18e-106">Global Constant</span></span>

<span data-ttu-id="8d18e-107">g \_ wszWMASFSecurityObjectsSize</span><span class="sxs-lookup"><span data-stu-id="8d18e-107">g\_wszWMASFSecurityObjectsSize</span></span>

## <a name="data-type"></a><span data-ttu-id="8d18e-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="8d18e-108">Data Type</span></span>

<span data-ttu-id="8d18e-109">**WMT \_ tipo \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="8d18e-109">**WMT\_TYPE\_QWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="8d18e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d18e-110">Remarks</span></span>

<span data-ttu-id="8d18e-111">Esse atributo é somente leitura e se aplica a todo o arquivo (fluxo 0).</span><span class="sxs-lookup"><span data-stu-id="8d18e-111">This attribute is read-only, and applies to the entire file (stream 0).</span></span>

<span data-ttu-id="8d18e-112">Você só pode recuperar esse atributo usando os métodos da interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) do objeto editor de metadados.</span><span class="sxs-lookup"><span data-stu-id="8d18e-112">You can only retrieve this attribute by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface from the metadata editor object.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d18e-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d18e-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d18e-114">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="8d18e-114">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




