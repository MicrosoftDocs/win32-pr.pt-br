---
title: Sobre a entrada bruta
description: Este tópico discute a entrada de usuários de dispositivos como joysticks, telas de toque e microfones.
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- entrada do usuário, entrada bruta
- capturando entrada do usuário, entrada bruta
- entrada bruta
- registrando a entrada bruta
- lendo entrada bruta
- entrada bruta do joystick
- entrada bruta de tela sensível ao toque
- entrada bruta do microfone
- HID (Dispositivo de Interface Humana)
- HID (dispositivos de interface humana)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fed3772406cc85df57b95c4b11dbcfeaf60804e94da5602059ec790e87e0439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884323"
---
# <a name="about-raw-input"></a>Sobre a entrada bruta

Há muitos dispositivos de entrada de usuário ao lado do teclado e do mouse tradicionais. Por exemplo, a entrada do usuário pode vir de um joystick, uma tela sensível ao toque, um microfone ou outros dispositivos que permitem grande flexibilidade na entrada do usuário. Esses dispositivos são coletivamente conhecidos como HIDs (dispositivos de interface humana). A API de entrada bruta fornece uma maneira estável e robusta para que os aplicativos aceitem a entrada bruta de qualquer HID, incluindo o teclado e o mouse.

Esta seção contém os seguintes tópicos:

-   [Modelo de entrada bruto](#raw-input-model)
-   [Registro de entrada bruta](#registration-for-raw-input)
-   [Lendo entrada bruta](#reading-raw-input)

## <a name="raw-input-model"></a>Modelo de entrada bruto

Anteriormente, o teclado e o mouse normalmente geraram dados de entrada. O sistema interpretou os dados provenientes desses dispositivos de forma a eliminar os detalhes específicos do dispositivo das informações brutas. Por exemplo, o teclado gera o código de verificação específico do dispositivo, mas o sistema fornece um aplicativo com o código de chave virtual. Além de ocultar os detalhes da entrada bruta, o Gerenciador de janelas não dava suporte a todos os novos HIDs. Para obter a entrada do HIDs sem suporte, um aplicativo tinha que fazer muitas coisas: abrir o dispositivo, gerenciar o modo compartilhado, ler periodicamente o dispositivo ou configurar a porta de conclusão de e/s e assim por diante. O modelo de entrada bruto e as APIs associadas foram desenvolvidas para permitir o acesso simples à entrada bruta de todos os dispositivos de entrada, incluindo o teclado e o mouse.

o modelo de entrada bruto é diferente do modelo de entrada de Windows original para o teclado e o mouse. No modelo de entrada original, um aplicativo recebe entrada independente de dispositivo na forma de mensagens que são enviadas ou postadas em suas janelas, como [**WM \_ Char**](wm-char.md), [**WM \_ MOUSEMOVE**](wm-mousemove.md)e [**WM \_ APPCOMMAND**](wm-appcommand.md). Por outro lado, para a entrada bruta, um aplicativo deve registrar os dispositivos do qual deseja obter dados. Além disso, o aplicativo obtém a entrada bruta por meio da mensagem de [**\_ entrada do WM**](wm-input.md) .

Há várias vantagens para o modelo de entrada bruto:

-   Um aplicativo não precisa detectar ou abrir o dispositivo de entrada.
-   Um aplicativo obtém os dados diretamente do dispositivo e processa os dados para suas necessidades.
-   Um aplicativo pode distinguir a origem da entrada mesmo que ela seja do mesmo tipo de dispositivo. Por exemplo, dois dispositivos de mouse.
-   Um aplicativo gerencia o tráfego de dados especificando dados de uma coleção de dispositivos ou apenas tipos de dispositivos específicos.
-   Os dispositivos HID podem ser usados à medida que se tornam disponíveis no Marketplace, sem aguardar novos tipos de mensagem ou um sistema operacional atualizado para ter novos comandos no [**WM \_ APPCOMMAND**](wm-appcommand.md).

Observe que o [**WM \_ APPCOMMAND**](wm-appcommand.md) fornece alguns dispositivos HID. No entanto, o **WM \_ APPCOMMAND** é um evento de entrada independente de dispositivo de nível superior, enquanto a [**\_ entrada do WM**](wm-input.md) envia dados brutos de baixo nível que são específicos para um dispositivo.

## <a name="registration-for-raw-input"></a>Registro de entrada bruta

Por padrão, nenhum aplicativo recebe entrada bruta. Para receber a entrada bruta de um dispositivo, um aplicativo deve registrar o dispositivo.

Para registrar dispositivos, um aplicativo primeiro cria uma matriz de estruturas [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) que especificam a [coleção de nível superior](/windows-hardware/drivers/hid/top-level-collections) (TLC) para os dispositivos que ele deseja. O TLC é definido por uma [página de uso](/windows-hardware/drivers/hid/hid-usages#usage-page) (a classe do dispositivo) e uma [ID de uso](/windows-hardware/drivers/hid/hid-usages#usage-id) (o dispositivo dentro da classe). Por exemplo, para obter o teclado TLC, defina UsagePage = 0x01 e Usageid = 0x06. O aplicativo chama [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) para registrar os dispositivos.

Observe que um aplicativo pode registrar um dispositivo que não está anexado no momento ao sistema. quando esse dispositivo estiver anexado, o gerenciador de Windows enviará automaticamente a entrada bruta para o aplicativo. Para obter a lista de dispositivos de entrada brutos no sistema, um aplicativo chama [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist). Usando o *hDevice* dessa chamada, um aplicativo chama [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) para obter as informações do dispositivo.

Por meio do membro **dwFlags** de [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice), um aplicativo pode selecionar os dispositivos a serem escutados e também aqueles que deseja ignorar. Por exemplo, um aplicativo pode solicitar entrada de todos os dispositivos de telefonia, exceto para as máquinas de resposta. Para obter o código de exemplo, consulte [registrando para entrada bruta](using-raw-input.md).

Observe que o mouse e o teclado também são HIDs, portanto, os dados deles podem vir por meio da [**\_ entrada do WM**](wm-input.md) de mensagem HID e de mensagens tradicionais. Um aplicativo pode selecionar um dos métodos pela seleção apropriada de sinalizadores em [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice).

Para obter o status do registro de um aplicativo, chame [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) a qualquer momento.

## <a name="reading-raw-input"></a>Lendo entrada bruta

Um aplicativo recebe entrada bruta de qualquer HID cuja [coleção de nível superior](/windows-hardware/drivers/hid/top-level-collections) (TLC) corresponde a um TLC do registro. Quando um aplicativo recebe entrada bruta, sua fila de mensagens Obtém uma mensagem de [**\_ entrada do WM**](wm-input.md) e o sinalizador de status da fila **QS \_ rawinput** é definido (**QS \_ entrada** também inclui esse sinalizador). Um aplicativo pode receber dados quando estiver em primeiro plano e quando estiver em segundo plano.

Há duas maneiras de ler os dados brutos: o método sem buffer (ou padrão) e o método em buffer. O método sem buffer obtém os dados brutos de uma estrutura [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) por vez e é adequado para muitos HIDS. Aqui, o aplicativo chama [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) para obter a mensagem de [**\_ entrada do WM**](wm-input.md) . Em seguida, o aplicativo chama [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) usando o identificador **rawinput** contido na **\_ entrada do WM**. Para obter um exemplo, consulte [fazendo uma leitura padrão de entrada bruta](using-raw-input.md).

Por outro lado, o método em buffer obtém uma matriz de estruturas [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) de cada vez. Isso é fornecido para dispositivos que podem produzir grandes quantidades de entrada bruta. Nesse método, o aplicativo chama [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) para obter uma matriz de estruturas **rawinput** . Observe que a macro [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) é usada para atravessar uma matriz de estruturas **rawinput** . Para obter um exemplo, consulte [fazendo uma leitura em buffer de entrada bruta](using-raw-input.md).

Para interpretar a entrada bruta, são necessárias informações detalhadas sobre o HIDs. Um aplicativo obtém as informações do dispositivo chamando [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) com o identificador do dispositivo. Esse identificador pode ser proveniente da [**\_ entrada do WM**](wm-input.md) ou do membro **hDevice** de [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader).