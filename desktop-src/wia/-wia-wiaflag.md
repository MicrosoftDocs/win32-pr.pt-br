---
description: 'Sinalizadores usados pelos métodos IWiaDevMgr:: GetImageDlg, IWiaDevMgr2:: GetImageDlg, IWiaItem::D eviceDlg e IWiaItem2::D eviceDlg para controlar a operação da caixa de diálogo.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: WiaFlag (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756497"
---
# <a name="wiaflag"></a><span data-ttu-id="e5b88-103">WiaFlag</span><span class="sxs-lookup"><span data-stu-id="e5b88-103">WiaFlag</span></span>

<span data-ttu-id="e5b88-104">Sinalizadores usados pelos métodos [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)e [**IWiaItem2::D evicedlg**](-wia-iwiaitem2-devicedlg.md) para controlar a operação da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e5b88-104">Flags used by the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg), and [**IWiaItem2::DeviceDlg**](-wia-iwiaitem2-devicedlg.md) methods to control the dialog box operation.</span></span>



| <span data-ttu-id="e5b88-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e5b88-105">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="e5b88-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5b88-106">Description</span></span>                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <span data-ttu-id="e5b88-107"><dt>**\_ \_ imagem única da caixa de diálogo do dispositivo WIA \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b88-107"><dt>**WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE**</dt></span></span> </dl>     | <span data-ttu-id="e5b88-108">Restringir a seleção de imagem a uma única imagem na caixa de diálogo aquisição de imagem de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5b88-108">Restrict image selection to a single image in the device image acquisition dialog box.</span></span><br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <span data-ttu-id="e5b88-109"><dt>**\_caixa de \_ diálogo do dispositivo WIA \_ usar \_ \_ interface do usuário comum**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b88-109"><dt>**WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI**</dt></span></span> </dl> | <span data-ttu-id="e5b88-110">Use a interface do usuário do sistema, se disponível, em vez da interface do usuário fornecida pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="e5b88-110">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="e5b88-111">Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada.</span><span class="sxs-lookup"><span data-stu-id="e5b88-111">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="e5b88-112">Se nenhuma interface do usuário estiver disponível, a função retornará E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e5b88-112">If neither UI is available, the function returns E\_NOTIMPL.</span></span><br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <span data-ttu-id="e5b88-113"><dt>**WIA \_ selecionar \_ dispositivo \_ padrão**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b88-113"><dt>**WIA\_SELECT\_DEVICE\_NODEFAULT**</dt></span></span> </dl>               | <span data-ttu-id="e5b88-114">Force o método [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) ou [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) para exibir a caixa de diálogo **selecionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="e5b88-114">Force the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) or [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method to display the **Select Device** dialog box.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e5b88-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5b88-115">Requirements</span></span>



| <span data-ttu-id="e5b88-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b88-116">Requirement</span></span> | <span data-ttu-id="e5b88-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e5b88-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b88-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5b88-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b88-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e5b88-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e5b88-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5b88-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b88-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5b88-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e5b88-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5b88-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5b88-123"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b88-123"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




