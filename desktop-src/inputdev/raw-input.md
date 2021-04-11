---
title: Entrada bruta
description: Esta seção descreve como o sistema fornece entrada bruta para seu aplicativo e como um aplicativo recebe e processa essa entrada.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Interface do usuário do Windows, entrada do usuário
- Interface do usuário do Windows, entrada bruta
- entrada do usuário, entrada bruta
- capturando entrada do usuário, entrada bruta
- entrada bruta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365942"
---
# <a name="raw-input"></a><span data-ttu-id="f7cac-108">Entrada bruta</span><span class="sxs-lookup"><span data-stu-id="f7cac-108">Raw Input</span></span>

<span data-ttu-id="f7cac-109">Esta seção descreve como o sistema fornece entrada bruta para seu aplicativo e como um aplicativo recebe e processa essa entrada.</span><span class="sxs-lookup"><span data-stu-id="f7cac-109">This section describes how the system provides raw input to your application and how an application receives and processes that input.</span></span> <span data-ttu-id="f7cac-110">Às vezes, a entrada bruta é chamada de entrada genérica.</span><span class="sxs-lookup"><span data-stu-id="f7cac-110">Raw input is sometimes referred to as generic input.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="f7cac-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f7cac-111">In This Section</span></span>



| <span data-ttu-id="f7cac-112">Nome</span><span class="sxs-lookup"><span data-stu-id="f7cac-112">Name</span></span>                                           | <span data-ttu-id="f7cac-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7cac-113">Description</span></span>                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7cac-114">Sobre a entrada bruta</span><span class="sxs-lookup"><span data-stu-id="f7cac-114">About Raw Input</span></span>](about-raw-input.md)         | <span data-ttu-id="f7cac-115">Discute a entrada de usuários de dispositivos como joysticks, telas de toque e microfones.</span><span class="sxs-lookup"><span data-stu-id="f7cac-115">Discusses user-input from devices such as joysticks, touch screens, and microphones.</span></span><br/> |
| [<span data-ttu-id="f7cac-116">Usando a entrada bruta</span><span class="sxs-lookup"><span data-stu-id="f7cac-116">Using Raw Input</span></span>](using-raw-input.md)         | <span data-ttu-id="f7cac-117">Fornece código de exemplo para tarefas relacionadas à entrada bruta.</span><span class="sxs-lookup"><span data-stu-id="f7cac-117">Provides sample code for tasks relating to raw input.</span></span><br/>                                |
| [<span data-ttu-id="f7cac-118">Referência de entrada bruta</span><span class="sxs-lookup"><span data-stu-id="f7cac-118">Raw Input Reference</span></span>](raw-input-reference.md) | <span data-ttu-id="f7cac-119">Contém a referência de API.</span><span class="sxs-lookup"><span data-stu-id="f7cac-119">Contains the API reference.</span></span><br/>                                                          |



 

### <a name="functions"></a><span data-ttu-id="f7cac-120">Funções</span><span class="sxs-lookup"><span data-stu-id="f7cac-120">Functions</span></span>



| <span data-ttu-id="f7cac-121">Nome</span><span class="sxs-lookup"><span data-stu-id="f7cac-121">Name</span></span>                                                                 | <span data-ttu-id="f7cac-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7cac-122">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7cac-123">**DefRawInputProc**</span><span class="sxs-lookup"><span data-stu-id="f7cac-123">**DefRawInputProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | <span data-ttu-id="f7cac-124">Chama o procedimento de entrada bruto padrão para fornecer o processamento padrão para todas as mensagens de entrada não processadas que um aplicativo não processa.</span><span class="sxs-lookup"><span data-stu-id="f7cac-124">Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.</span></span> <span data-ttu-id="f7cac-125">Essa função garante que cada mensagem seja processada.</span><span class="sxs-lookup"><span data-stu-id="f7cac-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="f7cac-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) é chamado com os mesmos parâmetros recebidos pelo procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="f7cac-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) is called with the same parameters received by the window procedure.</span></span> <br/> |
| [<span data-ttu-id="f7cac-127">**GetRawInputBuffer**</span><span class="sxs-lookup"><span data-stu-id="f7cac-127">**GetRawInputBuffer**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | <span data-ttu-id="f7cac-128">Executa uma leitura em buffer dos dados de entrada brutos.</span><span class="sxs-lookup"><span data-stu-id="f7cac-128">Performs a buffered read of the raw input data.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f7cac-129">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="f7cac-129">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | <span data-ttu-id="f7cac-130">Obtém a entrada bruta do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f7cac-130">Gets the raw input from the specified device.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="f7cac-131">**GetRawInputDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="f7cac-131">**GetRawInputDeviceInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | <span data-ttu-id="f7cac-132">Obtém informações sobre o dispositivo de entrada bruto.</span><span class="sxs-lookup"><span data-stu-id="f7cac-132">Gets information about the raw input device.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f7cac-133">**GetRawInputDeviceList**</span><span class="sxs-lookup"><span data-stu-id="f7cac-133">**GetRawInputDeviceList**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | <span data-ttu-id="f7cac-134">Enumera os dispositivos de entrada brutos anexados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="f7cac-134">Enumerates the raw input devices attached to the system.</span></span> <br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f7cac-135">**GetRegisteredRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="f7cac-135">**GetRegisteredRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | <span data-ttu-id="f7cac-136">Obtém as informações sobre os dispositivos de entrada brutos para o aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="f7cac-136">Gets the information about the raw input devices for the current application.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="f7cac-137">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="f7cac-137">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | <span data-ttu-id="f7cac-138">Registra os dispositivos que fornecem os dados de entrada brutos.</span><span class="sxs-lookup"><span data-stu-id="f7cac-138">Registers the devices that supply the raw input data.</span></span><br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a><span data-ttu-id="f7cac-139">Macros</span><span class="sxs-lookup"><span data-stu-id="f7cac-139">Macros</span></span>



| <span data-ttu-id="f7cac-140">Nome</span><span class="sxs-lookup"><span data-stu-id="f7cac-140">Name</span></span>                                                            | <span data-ttu-id="f7cac-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7cac-141">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7cac-142">**OBTER \_ \_ wParam do código rawinput \_**</span><span class="sxs-lookup"><span data-stu-id="f7cac-142">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | <span data-ttu-id="f7cac-143">Obtém o código de entrada do *wParam* na [**\_ entrada do WM**](wm-input.md).</span><span class="sxs-lookup"><span data-stu-id="f7cac-143">Gets the input code from *wParam* in [**WM\_INPUT**](wm-input.md).</span></span><br/>                              |
| [<span data-ttu-id="f7cac-144">**NEXTRAWINPUTBLOCK**</span><span class="sxs-lookup"><span data-stu-id="f7cac-144">**NEXTRAWINPUTBLOCK**</span></span>](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | <span data-ttu-id="f7cac-145">Obtém o local da próxima estrutura em uma matriz de estruturas [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) .</span><span class="sxs-lookup"><span data-stu-id="f7cac-145">Gets the location of the next structure in an array of [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structures.</span></span> <br/> |



 

### <a name="notifications"></a><span data-ttu-id="f7cac-146">Notificações</span><span class="sxs-lookup"><span data-stu-id="f7cac-146">Notifications</span></span>



| <span data-ttu-id="f7cac-147">Nome</span><span class="sxs-lookup"><span data-stu-id="f7cac-147">Name</span></span>                                                        | <span data-ttu-id="f7cac-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7cac-148">Description</span></span>                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="f7cac-149">**entrada do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f7cac-149">**WM\_INPUT**</span></span>](wm-input.md)                               | <span data-ttu-id="f7cac-150">Enviado para a janela que está obtendo entrada bruta.</span><span class="sxs-lookup"><span data-stu-id="f7cac-150">Sent to the window that is getting raw input.</span></span> <br/>            |
| [<span data-ttu-id="f7cac-151">**\_alteração do \_ dispositivo de entrada do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f7cac-151">**WM\_INPUT\_DEVICE\_CHANGE**</span></span>](wm-input-device-change.md) | <span data-ttu-id="f7cac-152">Enviado para a janela que está registrada para receber entrada bruta.</span><span class="sxs-lookup"><span data-stu-id="f7cac-152">Sent to the window that registered to receive raw input.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="f7cac-153">Estruturas</span><span class="sxs-lookup"><span data-stu-id="f7cac-153">Structures</span></span>



| <span data-ttu-id="f7cac-154">Nome</span><span class="sxs-lookup"><span data-stu-id="f7cac-154">Name</span></span>                                                            | <span data-ttu-id="f7cac-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7cac-155">Description</span></span>                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7cac-156">**RAWHID**</span><span class="sxs-lookup"><span data-stu-id="f7cac-156">**RAWHID**</span></span>](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | <span data-ttu-id="f7cac-157">Descreve o formato da entrada bruta de um dispositivos de interface humana (HID).</span><span class="sxs-lookup"><span data-stu-id="f7cac-157">Describes the format of the raw input from a Human Interface Device (HID).</span></span> <br/> |
| [<span data-ttu-id="f7cac-158">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="f7cac-158">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | <span data-ttu-id="f7cac-159">Contém a entrada bruta de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7cac-159">Contains the raw input from a device.</span></span> <br/>                                      |
| [<span data-ttu-id="f7cac-160">**RAWINPUTDEVICE**</span><span class="sxs-lookup"><span data-stu-id="f7cac-160">**RAWINPUTDEVICE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | <span data-ttu-id="f7cac-161">Define informações para os dispositivos de entrada brutos.</span><span class="sxs-lookup"><span data-stu-id="f7cac-161">Defines information for the raw input devices.</span></span> <br/>                             |
| [<span data-ttu-id="f7cac-162">**RAWINPUTDEVICELIST**</span><span class="sxs-lookup"><span data-stu-id="f7cac-162">**RAWINPUTDEVICELIST**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | <span data-ttu-id="f7cac-163">Contém informações sobre um dispositivo de entrada bruto.</span><span class="sxs-lookup"><span data-stu-id="f7cac-163">Contains information about a raw input device.</span></span><br/>                              |
| [<span data-ttu-id="f7cac-164">**RAWINPUTHEADER**</span><span class="sxs-lookup"><span data-stu-id="f7cac-164">**RAWINPUTHEADER**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | <span data-ttu-id="f7cac-165">Contém as informações de cabeçalho que fazem parte dos dados de entrada brutos.</span><span class="sxs-lookup"><span data-stu-id="f7cac-165">Contains the header information that is part of the raw input data.</span></span> <br/>        |
| [<span data-ttu-id="f7cac-166">**RAWKEYBOARD**</span><span class="sxs-lookup"><span data-stu-id="f7cac-166">**RAWKEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | <span data-ttu-id="f7cac-167">Contém informações sobre o estado do teclado.</span><span class="sxs-lookup"><span data-stu-id="f7cac-167">Contains information about the state of the keyboard.</span></span> <br/>                      |
| [<span data-ttu-id="f7cac-168">**RAWMOUSE**</span><span class="sxs-lookup"><span data-stu-id="f7cac-168">**RAWMOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | <span data-ttu-id="f7cac-169">Contém informações sobre o estado do mouse.</span><span class="sxs-lookup"><span data-stu-id="f7cac-169">Contains information about the state of the mouse.</span></span> <br/>                         |
| [<span data-ttu-id="f7cac-170">**\_informações do dispositivo RID \_**</span><span class="sxs-lookup"><span data-stu-id="f7cac-170">**RID\_DEVICE\_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | <span data-ttu-id="f7cac-171">Define os dados de entrada brutos provenientes de qualquer dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7cac-171">Defines the raw input data coming from any device.</span></span> <br/>                         |
| [<span data-ttu-id="f7cac-172">**informações de dispositivo de RID \_ \_ \_ HID**</span><span class="sxs-lookup"><span data-stu-id="f7cac-172">**RID\_DEVICE\_INFO\_HID**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | <span data-ttu-id="f7cac-173">Define os dados brutos de entrada provenientes do HID especificado.</span><span class="sxs-lookup"><span data-stu-id="f7cac-173">Defines the raw input data coming from the specified HID.</span></span> <br/>                  |
| [<span data-ttu-id="f7cac-174">**\_teclado de \_ informações do dispositivo RID \_**</span><span class="sxs-lookup"><span data-stu-id="f7cac-174">**RID\_DEVICE\_INFO\_KEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | <span data-ttu-id="f7cac-175">Define os dados brutos de entrada provenientes do teclado especificado.</span><span class="sxs-lookup"><span data-stu-id="f7cac-175">Defines the raw input data coming from the specified keyboard.</span></span> <br/>             |
| [<span data-ttu-id="f7cac-176">**\_mouse de \_ informações \_ do dispositivo RID**</span><span class="sxs-lookup"><span data-stu-id="f7cac-176">**RID\_DEVICE\_INFO\_MOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | <span data-ttu-id="f7cac-177">Define os dados brutos de entrada provenientes do mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="f7cac-177">Defines the raw input data coming from the specified mouse.</span></span><br/>                 |



 

 

