---
title: UI_PKEY_ColorType
description: Identifica a \_ Propriedade ColorType da interface do usuário PKEY \_ .
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294248"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="11145-103">Cortype da interface do usuário \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="11145-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="11145-104">Identifica a \_ Propriedade ColorType da interface do usuário PKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="11145-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="11145-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="11145-105">Remarks</span></span>

<span data-ttu-id="11145-106">O ColorType da interface do usuário \_ PKEY \_ é usado por um aplicativo para consultar a configuração de cores do controle [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="11145-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="11145-107">O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="11145-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11145-108">SWATCHCOLORTYPE da interface do usuário \_ \_</span><span class="sxs-lookup"><span data-stu-id="11145-108">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="11145-109">O aplicativo deve tratar a configuração de cor como transparente.</span><span class="sxs-lookup"><span data-stu-id="11145-109">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="11145-110">Normalmente usado em conjunto com a configuração cor **sem cor** .</span><span class="sxs-lookup"><span data-stu-id="11145-110">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="11145-111">interface do usuário \_ SWATCHCOLORTYPE \_ automática</span><span class="sxs-lookup"><span data-stu-id="11145-111">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="11145-112">O aplicativo deve consultar [GetSysColor (Color \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="11145-112">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="11145-113">Normalmente usado em conjunto com a configuração de cor **automática** .</span><span class="sxs-lookup"><span data-stu-id="11145-113">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="11145-114">interface do usuário \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="11145-114">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="11145-115">O aplicativo deve consultar a [ \_ \_ cor de PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-color.md) para a configuração de cor.</span><span class="sxs-lookup"><span data-stu-id="11145-115">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="11145-116">\_O ColorType de PKEY de interface do usuário \_ é passado para o método de retorno de chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando uma amostra de cor é selecionada em um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="11145-116">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="11145-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11145-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11145-118">Propriedades do seletor de cores</span><span class="sxs-lookup"><span data-stu-id="11145-118">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 