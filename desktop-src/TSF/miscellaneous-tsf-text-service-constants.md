---
title: Constantes de serviço de texto de TSF diversas (Ctffunc. h)
description: Os valores a seguir são usados com os serviços de texto.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ebd7d22f9cfbd59f95ee3dcfe68229536503b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782922"
---
# <a name="miscellaneous-tsf-text-service-constants"></a><span data-ttu-id="4e885-103">Constantes de serviço de texto de TSF diversas</span><span class="sxs-lookup"><span data-stu-id="4e885-103">Miscellaneous TSF Text Service Constants</span></span>

<span data-ttu-id="4e885-104">Os valores a seguir são usados com os serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="4e885-104">The following values are used with text services.</span></span>



| <span data-ttu-id="4e885-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="4e885-105">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="4e885-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e885-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <span data-ttu-id="4e885-107"><dt>**TF \_ MENUREADY**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4e885-107"><dt>**TF\_MENUREADY**</dt> <dt>0x00000001</dt></span></span> </dl>                                                | <span data-ttu-id="4e885-108">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="4e885-108">Not currently used.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <span data-ttu-id="4e885-109"><dt>**TF \_ PROPUI \_ status \_ SAVETOFILE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4e885-109"><dt>**TF\_PROPUI\_STATUS\_SAVETOFILE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4e885-110">A propriedade pode ser serializada.</span><span class="sxs-lookup"><span data-stu-id="4e885-110">The property can be serialized.</span></span> <span data-ttu-id="4e885-111">Se esse valor não estiver presente, a propriedade não poderá ser serializada.</span><span class="sxs-lookup"><span data-stu-id="4e885-111">If this value is not present, the property cannot be serialized.</span></span> <span data-ttu-id="4e885-112">Esse valor é usado com [ITfFnPropertyUIStatus:: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) e [ITfFnPropertyUIStatus:: SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span><span class="sxs-lookup"><span data-stu-id="4e885-112">This value is used with [ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) and [ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4e885-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e885-113">Requirements</span></span>



| <span data-ttu-id="4e885-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e885-114">Requirement</span></span> | <span data-ttu-id="4e885-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4e885-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e885-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e885-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4e885-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e885-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4e885-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e885-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4e885-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e885-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4e885-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4e885-120">Redistributable</span></span><br/>          | <span data-ttu-id="4e885-121">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4e885-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="4e885-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e885-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e885-123"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e885-123"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e885-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="4e885-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e885-125"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e885-125"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e885-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e885-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e885-127">ITfFnPropertyUIStatus:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="4e885-127">ITfFnPropertyUIStatus::GetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[<span data-ttu-id="4e885-128">ITfFnPropertyUIStatus:: SetStatus</span><span class="sxs-lookup"><span data-stu-id="4e885-128">ITfFnPropertyUIStatus::SetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





