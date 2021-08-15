---
title: Entrada bruta
description: Esta seção descreve como o sistema fornece entrada bruta para seu aplicativo e como um aplicativo recebe e processa essa entrada.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows Interface do usuário, entrada do usuário
- Windows Interface do usuário, entrada bruta
- entrada do usuário, entrada bruta
- capturando entrada do usuário, entrada bruta
- entrada bruta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e26d67f2b014ce22c2d01cb4738cca4e041c59e417a216f0d75ffef6e6e4b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482752"
---
# <a name="raw-input"></a>Entrada bruta

Esta seção descreve como o sistema fornece entrada bruta para seu aplicativo e como um aplicativo recebe e processa essa entrada. Às vezes, a entrada bruta é chamada de entrada genérica.

### <a name="in-this-section"></a>Nesta seção



| Nome                                           | Descrição                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Sobre a entrada bruta](about-raw-input.md)         | Discute a entrada de usuários de dispositivos como joysticks, telas de toque e microfones.<br/> |
| [Usando a entrada bruta](using-raw-input.md)         | Fornece código de exemplo para tarefas relacionadas à entrada bruta.<br/>                                |
| [Referência de entrada bruta](raw-input-reference.md) | Contém a referência de API.<br/>                                                          |



 

### <a name="functions"></a>Funções



| Nome                                                                 | Descrição                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | Chama o procedimento de entrada bruto padrão para fornecer o processamento padrão para todas as mensagens de entrada não processadas que um aplicativo não processa. Essa função garante que cada mensagem seja processada. [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) é chamado com os mesmos parâmetros recebidos pelo procedimento de janela. <br/> |
| [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | Executa uma leitura em buffer dos dados de entrada brutos.<br/>                                                                                                                                                                                                                                                              |
| [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | Obtém a entrada bruta do dispositivo especificado.<br/>                                                                                                                                                                                                                                                                |
| [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | Obtém informações sobre o dispositivo de entrada bruto.<br/>                                                                                                                                                                                                                                                                 |
| [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | Enumera os dispositivos de entrada brutos anexados ao sistema. <br/>                                                                                                                                                                                                                                                    |
| [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | Obtém as informações sobre os dispositivos de entrada brutos para o aplicativo atual.<br/>                                                                                                                                                                                                                                |
| [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | Registra os dispositivos que fornecem os dados de entrada brutos.<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>Macros



| Nome                                                            | Descrição                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**OBTER \_ \_ wParam do código rawinput \_**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | Obtém o código de entrada do *wParam* na [**\_ entrada do WM**](wm-input.md).<br/>                              |
| [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | Obtém o local da próxima estrutura em uma matriz de estruturas [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) . <br/> |



 

### <a name="notifications"></a>Notificações



| Nome                                                        | Descrição                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**entrada do WM \_**](wm-input.md)                               | Enviado para a janela que está obtendo entrada bruta. <br/>            |
| [**\_alteração do \_ dispositivo de entrada do WM \_**](wm-input-device-change.md) | Enviado para a janela que está registrada para receber entrada bruta. <br/> |



 

### <a name="structures"></a>Estruturas



| Nome                                                            | Descrição                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RAWHID**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | Descreve o formato da entrada bruta de um dispositivos de interface humana (HID). <br/> |
| [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | Contém a entrada bruta de um dispositivo. <br/>                                      |
| [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | Define informações para os dispositivos de entrada brutos. <br/>                             |
| [**RAWINPUTDEVICELIST**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | Contém informações sobre um dispositivo de entrada bruto.<br/>                              |
| [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | Contém as informações de cabeçalho que fazem parte dos dados de entrada brutos. <br/>        |
| [**RAWKEYBOARD**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | Contém informações sobre o estado do teclado. <br/>                      |
| [**RAWMOUSE**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | Contém informações sobre o estado do mouse. <br/>                         |
| [**\_informações do dispositivo RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | Define os dados de entrada brutos provenientes de qualquer dispositivo. <br/>                         |
| [**informações de dispositivo de RID \_ \_ \_ HID**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | Define os dados brutos de entrada provenientes do HID especificado. <br/>                  |
| [**\_teclado de \_ informações do dispositivo RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | Define os dados brutos de entrada provenientes do teclado especificado. <br/>             |
| [**\_mouse de \_ informações \_ do dispositivo RID**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | Define os dados brutos de entrada provenientes do mouse especificado.<br/>                 |



 

 

