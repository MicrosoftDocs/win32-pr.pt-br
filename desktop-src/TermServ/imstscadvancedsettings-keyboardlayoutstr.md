---
title: Propriedade IMsTscAdvancedSettings KeyBoardLayoutStr
description: Especifica o nome do identificador de localidade de entrada ativo (anteriormente chamado de layout de teclado) a ser usado para a conexão.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade KeyBoardLayoutStr
- Propriedade KeyBoardLayoutStr Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, propriedade KeyBoardLayoutStr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644650"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a><span data-ttu-id="c02b2-106">Propriedade IMsTscAdvancedSettings:: KeyBoardLayoutStr</span><span class="sxs-lookup"><span data-stu-id="c02b2-106">IMsTscAdvancedSettings::KeyBoardLayoutStr property</span></span>

<span data-ttu-id="c02b2-107">Especifica o nome do identificador de localidade de entrada ativo (anteriormente chamado de layout de teclado) a ser usado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="c02b2-107">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span>

<span data-ttu-id="c02b2-108">Se essa propriedade não for definida, o controle usará o layout padrão retornado pela função [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .</span><span class="sxs-lookup"><span data-stu-id="c02b2-108">If this property is not set, the control uses the default layout returned by the [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) function.</span></span>

<span data-ttu-id="c02b2-109">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="c02b2-109">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c02b2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c02b2-110">Syntax</span></span>


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a><span data-ttu-id="c02b2-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c02b2-111">Property value</span></span>

<span data-ttu-id="c02b2-112">O nome do identificador de localidade de entrada ativo.</span><span class="sxs-lookup"><span data-stu-id="c02b2-112">The name of the active input locale identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c02b2-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c02b2-113">Error codes</span></span>

<span data-ttu-id="c02b2-114">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c02b2-114">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c02b2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c02b2-115">Remarks</span></span>

<span data-ttu-id="c02b2-116">A propriedade é um número hexadecimal de oito dígitos na forma de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c02b2-116">The property is an eight digit hexadecimal number in string form.</span></span> <span data-ttu-id="c02b2-117">Os quatro dígitos inferiores representam o identificador de idioma, e os quatro dígitos superiores representam a variação de teclado dentro desse idioma.</span><span class="sxs-lookup"><span data-stu-id="c02b2-117">The lower four digits represent the language identifier, and the upper four digits represent the keyboard variation within that language.</span></span> <span data-ttu-id="c02b2-118">Portanto, por exemplo, "00000409" representaria o teclado padrão em inglês dos EUA porque "0409" é o identificador de idioma inglês dos EUA.</span><span class="sxs-lookup"><span data-stu-id="c02b2-118">So, for example, "00000409" would represent the default US English keyboard because "0409" is the US English language identifier.</span></span> <span data-ttu-id="c02b2-119">A variação Dvorak do teclado em inglês dos EUA tem um identificador de "00010409".</span><span class="sxs-lookup"><span data-stu-id="c02b2-119">The Dvorak variation of the US English keyboard has an identifier of "00010409".</span></span> <span data-ttu-id="c02b2-120">Você pode encontrar os layouts de teclado disponíveis, listados por seus identificadores de layout de teclado, no registro em</span><span class="sxs-lookup"><span data-stu-id="c02b2-120">You can find the available keyboard layouts, listed by their keyboard layout identifiers, in the registry under</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

<span data-ttu-id="c02b2-121">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c02b2-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c02b2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c02b2-122">Requirements</span></span>



| <span data-ttu-id="c02b2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c02b2-123">Requirement</span></span> | <span data-ttu-id="c02b2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c02b2-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c02b2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c02b2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c02b2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c02b2-126">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="c02b2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c02b2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c02b2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c02b2-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c02b2-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c02b2-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="c02b2-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c02b2-130"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c02b2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c02b2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c02b2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c02b2-132"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c02b2-133">IID</span><span class="sxs-lookup"><span data-stu-id="c02b2-133">IID</span></span><br/>                      | <span data-ttu-id="c02b2-134">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="c02b2-134">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c02b2-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c02b2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c02b2-136">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c02b2-136">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

