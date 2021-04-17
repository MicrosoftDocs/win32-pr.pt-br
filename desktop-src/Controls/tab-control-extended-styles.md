---
title: Estilos estendidos de controle de guia (CommCtrl. h)
description: O controle guia agora dá suporte a estilos estendidos. Esses estilos são manipulados usando as mensagens TCM Extended \_ e TCM \_ setextendedattribute e não devem ser confundidos com estilos de janela estendidos que são passados para CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748714"
---
# <a name="tab-control-extended-styles"></a><span data-ttu-id="f20d4-104">Estilos estendidos de controle de guia</span><span class="sxs-lookup"><span data-stu-id="f20d4-104">Tab Control Extended Styles</span></span>

<span data-ttu-id="f20d4-105">O controle guia agora dá suporte a estilos estendidos.</span><span class="sxs-lookup"><span data-stu-id="f20d4-105">The tab control now supports extended styles.</span></span> <span data-ttu-id="f20d4-106">Esses estilos são manipulados usando as mensagens TCM Extended e [**TCM \_ setextendedattribute**](tcm-setextendedstyle.md) e não devem ser confundidos com estilos de janela estendidos que são passados para [**\_**](tcm-getextendedstyle.md) [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="f20d4-106">These styles are manipulated using the [**TCM\_GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) and [**TCM\_SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) messages and should not be confused with extended window styles that are passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>



| <span data-ttu-id="f20d4-107">Constante</span><span class="sxs-lookup"><span data-stu-id="f20d4-107">Constant</span></span>                                                                                                                                                                               | <span data-ttu-id="f20d4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f20d4-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <span data-ttu-id="f20d4-109"><dt>**TCS \_ ex \_ FLATSEPARATORS**</dt></span><span class="sxs-lookup"><span data-stu-id="f20d4-109"><dt>**TCS\_EX\_FLATSEPARATORS**</dt></span></span> </dl> | <span data-ttu-id="f20d4-110">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="f20d4-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="f20d4-111">O controle guia desenhará separadores entre os itens da guia.</span><span class="sxs-lookup"><span data-stu-id="f20d4-111">The tab control will draw separators between the tab items.</span></span> <span data-ttu-id="f20d4-112">Esse estilo estendido só afeta os controles de guia que têm os [**\_ botões de TCS**](tab-control-styles.md) e os estilos de [**\_ FLATBUTTONS de TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f20d4-112">This extended style only affects tab controls that have the [**TCS\_BUTTONS**](tab-control-styles.md) and [**TCS\_FLATBUTTONS**](tab-control-styles.md) styles.</span></span> <span data-ttu-id="f20d4-113">Por padrão, a criação do controle guia com o estilo de **\_ FLATBUTTONS de TCS** define esse estilo estendido.</span><span class="sxs-lookup"><span data-stu-id="f20d4-113">By default, creating the tab control with the **TCS\_FLATBUTTONS** style sets this extended style.</span></span> <span data-ttu-id="f20d4-114">Se você não precisar de separadores, deverá remover esse estilo estendido depois de criar o controle.</span><span class="sxs-lookup"><span data-stu-id="f20d4-114">If you do not require separators, you should remove this extended style after creating the control.</span></span><br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <span data-ttu-id="f20d4-115"><dt>**TCS \_ ex \_ REGISTERDROP**</dt></span><span class="sxs-lookup"><span data-stu-id="f20d4-115"><dt>**TCS\_EX\_REGISTERDROP**</dt></span></span> </dl>       | <span data-ttu-id="f20d4-116">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="f20d4-116">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="f20d4-117">O controle guia gera códigos de notificação do [TCN \_ GetObject](tcn-getobject.md) para solicitar um objeto de destino drop quando um objeto é arrastado sobre os itens da guia no controle.</span><span class="sxs-lookup"><span data-stu-id="f20d4-117">The tab control generates [TCN\_GETOBJECT](tcn-getobject.md) notification codes to request a drop target object when an object is dragged over the tab items in the control.</span></span> <span data-ttu-id="f20d4-118">O aplicativo deve chamar [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de definir esse estilo.</span><span class="sxs-lookup"><span data-stu-id="f20d4-118">The application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before setting this style.</span></span> <br/>                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="f20d4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f20d4-119">Requirements</span></span>



| <span data-ttu-id="f20d4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f20d4-120">Requirement</span></span> | <span data-ttu-id="f20d4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f20d4-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f20d4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f20d4-122">Header</span></span><br/> | <dl> <span data-ttu-id="f20d4-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f20d4-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

