---
title: UI_PKEY_ColorType
description: Identifica a \_ Propriedade ColorType da interface do usuário PKEY \_ .
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443887"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="1c55f-103">Cortype da interface do usuário \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="1c55f-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="1c55f-104">Identifica a \_ Propriedade ColorType da interface do usuário PKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="1c55f-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="1c55f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c55f-105">Remarks</span></span>

<span data-ttu-id="1c55f-106">O ColorType da interface do usuário \_ PKEY \_ é usado por um aplicativo para consultar a configuração de cores do controle [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="1c55f-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="1c55f-107">O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="1c55f-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|    <span data-ttu-id="1c55f-108">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1c55f-108">Property</span></span>                            |    <span data-ttu-id="1c55f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c55f-109">Description</span></span>                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c55f-110">SWATCHCOLORTYPE da interface do usuário \_ \_</span><span class="sxs-lookup"><span data-stu-id="1c55f-110">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="1c55f-111">O aplicativo deve tratar a configuração de cor como transparente.</span><span class="sxs-lookup"><span data-stu-id="1c55f-111">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="1c55f-112">Normalmente usado em conjunto com a configuração cor **sem cor** .</span><span class="sxs-lookup"><span data-stu-id="1c55f-112">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="1c55f-113">interface do usuário \_ SWATCHCOLORTYPE \_ automática</span><span class="sxs-lookup"><span data-stu-id="1c55f-113">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="1c55f-114">O aplicativo deve consultar [GetSysColor (Color \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="1c55f-114">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="1c55f-115">Normalmente usado em conjunto com a configuração de cor **automática** .</span><span class="sxs-lookup"><span data-stu-id="1c55f-115">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="1c55f-116">interface do usuário \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="1c55f-116">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="1c55f-117">O aplicativo deve consultar a [ \_ \_ cor de PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-color.md) para a configuração de cor.</span><span class="sxs-lookup"><span data-stu-id="1c55f-117">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="1c55f-118">\_O ColorType de PKEY de interface do usuário \_ é passado para o método de retorno de chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando uma amostra de cor é selecionada em um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="1c55f-118">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c55f-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c55f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c55f-120">Propriedades do seletor de cores</span><span class="sxs-lookup"><span data-stu-id="1c55f-120">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 