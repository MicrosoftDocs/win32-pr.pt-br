---
title: Interface ISoftKbd (Softkbdc. h)
description: A interface ISoftKbd é usada por aplicativos e serviços de texto para implementar um teclado virtual.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Estrutura de serviços de texto da interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, descrita
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761367"
---
# <a name="isoftkbd-interface"></a><span data-ttu-id="e5953-105">Interface ISoftKbd</span><span class="sxs-lookup"><span data-stu-id="e5953-105">ISoftKbd interface</span></span>

<span data-ttu-id="e5953-106">A interface **ISoftKbd** é usada por aplicativos e serviços de texto para implementar um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5953-106">The **ISoftKbd** interface is used by applications and text services to implement a soft keyboard.</span></span>

## <a name="members"></a><span data-ttu-id="e5953-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e5953-107">Members</span></span>

<span data-ttu-id="e5953-108">A interface **ISoftKbd** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e5953-108">The **ISoftKbd** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e5953-109">**ISoftKbd** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e5953-109">**ISoftKbd** also has these types of members:</span></span>

-   [<span data-ttu-id="e5953-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e5953-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e5953-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e5953-111">Methods</span></span>

<span data-ttu-id="e5953-112">A interface **ISoftKbd** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e5953-112">The **ISoftKbd** interface has these methods.</span></span>



| <span data-ttu-id="e5953-113">Método</span><span class="sxs-lookup"><span data-stu-id="e5953-113">Method</span></span>                                                                                        | <span data-ttu-id="e5953-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5953-114">Description</span></span>                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5953-115">**AdviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="e5953-115">**AdviseSoftKeyboardEventSink**</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)                   | <span data-ttu-id="e5953-116">Instala um coletor de eventos de teclado flexível para lidar com notificações OnKeySelection do teclado soft.</span><span class="sxs-lookup"><span data-stu-id="e5953-116">Installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span><br/> |
| [<span data-ttu-id="e5953-117">**CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="e5953-117">**CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md) | <span data-ttu-id="e5953-118">Cria um layout de teclado flexível a partir do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="e5953-118">Creates a soft keyboard layout from the specified resource.</span></span><br/>                                        |
| [<span data-ttu-id="e5953-119">**CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="e5953-119">**CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | <span data-ttu-id="e5953-120">Cria um layout de teclado flexível a partir do arquivo XML especificado.</span><span class="sxs-lookup"><span data-stu-id="e5953-120">Creates a soft keyboard layout from the specified XML file.</span></span><br/>                                        |
| [<span data-ttu-id="e5953-121">**CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="e5953-121">**CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)                         | <span data-ttu-id="e5953-122">Cria uma janela de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="e5953-122">Creates a soft keyboard window.</span></span><br/>                                                                    |
| [<span data-ttu-id="e5953-123">**DestroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="e5953-123">**DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)                       | <span data-ttu-id="e5953-124">Destrói uma janela de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="e5953-124">Destroys a soft keyboard window.</span></span><br/>                                                                   |
| [<span data-ttu-id="e5953-125">**EnumSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="e5953-125">**EnumSoftKeyboard**</span></span>](isoftkbd-enumsoftkeyboard.md)                                         | <span data-ttu-id="e5953-126">Enumera os teclados suaves possíveis que dão suporte ao idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="e5953-126">Enumerates the possible soft keyboards that support the specified language.</span></span><br/>                        |
| [<span data-ttu-id="e5953-127">**GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="e5953-127">**GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)                               | <span data-ttu-id="e5953-128">Recupera a cor do teclado flexível correspondente ao tipo de cor fornecido.</span><span class="sxs-lookup"><span data-stu-id="e5953-128">Retrieves the soft keyboard color corresponding to the supplied color type.</span></span><br/>                        |
| [<span data-ttu-id="e5953-129">**GetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="e5953-129">**GetSoftKeyboardPosSize**</span></span>](isoftkbd-getsoftkeyboardpossize.md)                             | <span data-ttu-id="e5953-130">Recupera a posição inicial e o tamanho de um teclado suave.</span><span class="sxs-lookup"><span data-stu-id="e5953-130">Retrieves the starting position and size of a soft keyboard.</span></span><br/>                                       |
| [<span data-ttu-id="e5953-131">**GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="e5953-131">**GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)                           | <span data-ttu-id="e5953-132">Recupera a fonte de texto usada por um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5953-132">Retrieves the text font used by a soft keyboard.</span></span><br/>                                                   |
| [<span data-ttu-id="e5953-133">**GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="e5953-133">**GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)                           | <span data-ttu-id="e5953-134">Recupera o modo de tipo para um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5953-134">Retrieves the type mode for a soft keyboard.</span></span><br/>                                                       |
| [<span data-ttu-id="e5953-135">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="e5953-135">**Initialize**</span></span>](isoftkbd-initialize.md)                                                     | <span data-ttu-id="e5953-136">Inicializa todos os campos necessários para um teclado virtual e gera layouts de teclado flexível padrão.</span><span class="sxs-lookup"><span data-stu-id="e5953-136">Initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span><br/> |
| [<span data-ttu-id="e5953-137">**SelectSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="e5953-137">**SelectSoftKeyboard**</span></span>](isoftkbd-selectsoftkeyboard.md)                                     | <span data-ttu-id="e5953-138">Seleciona o teclado virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="e5953-138">Selects the specified soft keyboard.</span></span><br/>                                                               |
| [<span data-ttu-id="e5953-139">**SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="e5953-139">**SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)                                 | <span data-ttu-id="e5953-140">Define o texto do rótulo do layout de um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5953-140">Sets the label text from the layout for a soft keyboard.</span></span><br/>                                           |
| [<span data-ttu-id="e5953-141">**SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="e5953-141">**SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)           | <span data-ttu-id="e5953-142">Define uma combinação de rótulo e texto usado para descrever um teclado suave.</span><span class="sxs-lookup"><span data-stu-id="e5953-142">Sets a combination of label and text used to describe a soft keyboard.</span></span><br/>                             |
| [<span data-ttu-id="e5953-143">**SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="e5953-143">**SetSoftKeyboardColors**</span></span>](isoftkbd-setsoftkeyboardcolors.md)                               | <span data-ttu-id="e5953-144">Define a cor do teclado flexível correspondente ao tipo de cor fornecido.</span><span class="sxs-lookup"><span data-stu-id="e5953-144">Sets the soft keyboard color corresponding to the supplied color type.</span></span><br/>                             |
| [<span data-ttu-id="e5953-145">**SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="e5953-145">**SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)                             | <span data-ttu-id="e5953-146">Define a posição inicial e o tamanho de um teclado suave.</span><span class="sxs-lookup"><span data-stu-id="e5953-146">Sets the starting position and size of a soft keyboard.</span></span><br/>                                            |
| [<span data-ttu-id="e5953-147">**SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="e5953-147">**SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)                           | <span data-ttu-id="e5953-148">Define a fonte de texto usada por um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5953-148">Sets the text font used by a soft keyboard.</span></span><br/>                                                        |
| [<span data-ttu-id="e5953-149">**SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="e5953-149">**SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)                           | <span data-ttu-id="e5953-150">Define o modo de tipo para um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5953-150">Sets the type mode for a soft keyboard.</span></span><br/>                                                            |
| [<span data-ttu-id="e5953-151">**ShowKeysForKeyScanMode**</span><span class="sxs-lookup"><span data-stu-id="e5953-151">**ShowKeysForKeyScanMode**</span></span>](isoftkbd-showkeysforkeyscanmode.md)                             | <span data-ttu-id="e5953-152">Exibe as chaves usadas para o modo de verificação de chave para um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5953-152">Displays the keys used for the key scan mode for a soft keyboard.</span></span><br/>                                  |
| [<span data-ttu-id="e5953-153">**ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="e5953-153">**ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)                                         | <span data-ttu-id="e5953-154">Exibe um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5953-154">Displays a soft keyboard.</span></span><br/>                                                                          |
| [<span data-ttu-id="e5953-155">**UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="e5953-155">**UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)               | <span data-ttu-id="e5953-156">Remove um coletor de eventos de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="e5953-156">Removes a soft keyboard event sink.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="e5953-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5953-157">Requirements</span></span>



| <span data-ttu-id="e5953-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5953-158">Requirement</span></span> | <span data-ttu-id="e5953-159">Valor</span><span class="sxs-lookup"><span data-stu-id="e5953-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5953-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5953-160">Minimum supported client</span></span><br/> | <span data-ttu-id="e5953-161">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5953-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e5953-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5953-162">Minimum supported server</span></span><br/> | <span data-ttu-id="e5953-163">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5953-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e5953-164">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e5953-164">Redistributable</span></span><br/>          | <span data-ttu-id="e5953-165">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e5953-165">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="e5953-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5953-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5953-167"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5953-167"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="e5953-168">INSERI</span><span class="sxs-lookup"><span data-stu-id="e5953-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5953-169"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5953-169"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5953-170">DLL</span><span class="sxs-lookup"><span data-stu-id="e5953-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5953-171"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5953-171"><dt>Softkbd.dll</dt></span></span> </dl> |



 

