---
title: Constantes da barra de idiomas diversas (Ctfutb. h)
description: As constantes da barra de idiomas diversas definem determinadas propriedades das barras de idiomas.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369842"
---
# <a name="miscellaneous-language-bar-constants"></a><span data-ttu-id="1356a-103">Constantes da barra de idiomas diversos</span><span class="sxs-lookup"><span data-stu-id="1356a-103">Miscellaneous Language Bar Constants</span></span>

<span data-ttu-id="1356a-104">As constantes da barra de idiomas diversas definem determinadas propriedades das barras de idiomas.</span><span class="sxs-lookup"><span data-stu-id="1356a-104">The miscellaneous language bar constants set certain properties of language bars.</span></span>



| <span data-ttu-id="1356a-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="1356a-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="1356a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1356a-106">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <span data-ttu-id="1356a-107"><dt>**TF \_ DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1356a-107"><dt>**TF\_DTLBI\_USEPROFILEICON**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="1356a-108">O item da barra de idiomas do sistema deve exibir o ícone especificado para o perfil de idioma.</span><span class="sxs-lookup"><span data-stu-id="1356a-108">The system language bar item should display the icon specified for the language profile.</span></span> <span data-ttu-id="1356a-109">Usado nos métodos [ITfSystemDeviceTypeLangBarItem:: Geticonmode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) e [ITfSystemDeviceTypeLangBarItem:: seticonmode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) .</span><span class="sxs-lookup"><span data-stu-id="1356a-109">Used in the [ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) and [ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) methods.</span></span><br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <span data-ttu-id="1356a-110"><dt>**TF \_ INVALIDMENUITEM**</dt> <dt>(UINT) (-1)</dt></span><span class="sxs-lookup"><span data-stu-id="1356a-110"><dt>**TF\_INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt></span></span> </dl>                 | <span data-ttu-id="1356a-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="1356a-111">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <span data-ttu-id="1356a-112"><dt>**TF \_ BIN \_ BMPF \_ vertical**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1356a-112"><dt>**TF\_LBI\_BMPF\_VERTICAL**</dt> <dt>0x00000001</dt></span></span> </dl>         | <span data-ttu-id="1356a-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="1356a-113">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <span data-ttu-id="1356a-114"><dt>**TF \_ BIN \_ desc \_ MAXLEN**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="1356a-114"><dt>**TF\_LBI\_DESC\_MAXLEN**</dt> <dt>32</dt></span></span> </dl>                       | <span data-ttu-id="1356a-115">Comprimento, em caracteres WCHAR, do membro da estrutura [TF \_ LANGBARITEMINFO. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span><span class="sxs-lookup"><span data-stu-id="1356a-115">Length, in WCHAR characters, of structure member [TF\_LANGBARITEMINFO.szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span></span><br/>                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="1356a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1356a-116">Requirements</span></span>



| <span data-ttu-id="1356a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1356a-117">Requirement</span></span> | <span data-ttu-id="1356a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1356a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1356a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1356a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1356a-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1356a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1356a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1356a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1356a-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1356a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1356a-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="1356a-123">Redistributable</span></span><br/>          | <span data-ttu-id="1356a-124">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1356a-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="1356a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1356a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1356a-126"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1356a-126"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1356a-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="1356a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1356a-128"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1356a-128"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1356a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1356a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1356a-130">ITfSystemDeviceTypeLangBarItem:: geticonmode</span><span class="sxs-lookup"><span data-stu-id="1356a-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[<span data-ttu-id="1356a-131">ITfSystemDeviceTypeLangBarItem:: seticonmode</span><span class="sxs-lookup"><span data-stu-id="1356a-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[<span data-ttu-id="1356a-132">TF \_ LANGBARITEMINFO</span><span class="sxs-lookup"><span data-stu-id="1356a-132">TF\_LANGBARITEMINFO</span></span>](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





