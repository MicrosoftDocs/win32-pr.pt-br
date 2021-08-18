---
title: Aproveitando o movimento do High-Definition mouse
description: Este artigo se concentra na melhor maneira de otimizar o desempenho da entrada do mouse de alta definição em um jogo como um shooter de primeira pessoa.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7a6efe6916ad8605e3cdc056ffd716ac5113b66c022b0a95fd8a78b1a62e30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042386"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Aproveitando o movimento do High-Definition mouse

Um mouse de computador padrão retorna dados a 400 pontos por polegada (DPI), enquanto que um mouse de alta definição gera dados em 800 DPI ou mais. Isso torna a entrada de um mouse de alta definição muito mais precisa do que a de um mouse padrão. No entanto, os dados de alta definição não podem ser obtidos por meio das mensagens MOUSEMOVE padrão do WM \_ . Em geral, os jogos se beneficiarão de dispositivos com o mouse de alta definição, mas os jogos que obtêm dados do mouse usando apenas \_ o WM MOUSEMOVE não conseguirão acessar a resolução completa e não filtrada do mouse.

Várias empresas são dispositivos de mouse de alta definição de fabricação, como Microsoft e Logitech. Com o aumento da popularidade dos dispositivos de mouse de alta resolução, é importante que os desenvolvedores entendam como usar as informações geradas por esses dispositivos de maneira ideal. Este artigo se concentra na melhor maneira de otimizar o desempenho da entrada do mouse de alta definição em um jogo como um shooter de primeira pessoa.

## <a name="retrieving-mouse-movement-data"></a>Recuperando dados de movimento do mouse

Aqui estão os três métodos principais para recuperar os dados do mouse:

-   [admousemove do WM \_](/windows)
-   [entrada do WM \_](/windows)
-   [DirectInput](#directinput)

Há vantagens e desvantagens em cada método, dependendo de como os dados serão usados.

### <a name="wm_mousemove"></a>admousemove do WM \_

O método mais simples de ler dados de movimento do mouse é por meio de mensagens do WM \_ MOUSEMOVE. Veja a seguir um exemplo de como ler dados de movimento do mouse da \_ mensagem MOUSEMOVE do WM:

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

A principal desvantagem dos dados do WM \_ MOUSEMOVE é que ele é limitado à resolução da tela. Isso significa que se você mover um pouco o mouse, mas não o suficiente para fazer com que o ponteiro se mova para o próximo pixel —, nenhuma \_ mensagem MOUSEMOVE do WM será gerada. Portanto, o uso desse método para ler o movimento do mouse nega os benefícios da entrada de alta definição.

\_no entanto, a vantagem do WM MOUSEMOVE é que Windows aplica a aceleração do ponteiro (também conhecida como ballistics) aos dados brutos do mouse, o que faz com que o ponteiro do mouse se comporte como os clientes esperam. Isso torna \_ o WM MOUSEMOVE a opção preferida para controle de ponteiro (sobre \_ entrada ou DIRECTINPUT do WM), pois resulta em um comportamento mais natural para os usuários. Embora \_ o WM MOUSEMOVE seja ideal para mover ponteiros do mouse, não é tão bom para mover uma câmera de primeira pessoa, pois a precisão de alta definição será perdida.

Para obter mais informações sobre o WM \_ MouseMove, consulte [**WM \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove).

### <a name="wm_input"></a>entrada do WM \_

O segundo método de obtenção de dados do mouse é ler \_ mensagens de entrada do WM. O processamento de \_ mensagens de entrada do WM é mais complicado do que processar \_ mensagens MOUSEMOVE do WM, mas \_ as mensagens de entrada do WM são lidas diretamente da pilha dispositivos de interface humana (HID) e refletem os resultados de alta definição.

Para ler os dados de movimento do mouse da mensagem de entrada do WM \_ , o dispositivo deve primeiro ser registrado; o código a seguir fornece um exemplo disso:

```cpp
// you can #include <hidusage.h> for these defines
#ifndef HID_USAGE_PAGE_GENERIC
#define HID_USAGE_PAGE_GENERIC         ((USHORT) 0x01)
#endif
#ifndef HID_USAGE_GENERIC_MOUSE
#define HID_USAGE_GENERIC_MOUSE        ((USHORT) 0x02)
#endif

RAWINPUTDEVICE Rid[1];
Rid[0].usUsagePage = HID_USAGE_PAGE_GENERIC; 
Rid[0].usUsage = HID_USAGE_GENERIC_MOUSE; 
Rid[0].dwFlags = RIDEV_INPUTSINK;   
Rid[0].hwndTarget = hWnd;
RegisterRawInputDevices(Rid, 1, sizeof(Rid[0]));
```

O código a seguir manipula \_ as mensagens de entrada do WM no manipulador que WinProc do aplicativo:

```cpp
case WM_INPUT: 
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEMOUSE) 
    {
        int xPosRelative = raw->data.mouse.lLastX;
        int yPosRelative = raw->data.mouse.lLastY;
    } 
    break;
}
```

A vantagem de usar a \_ entrada do WM é que seu jogo recebe dados brutos do mouse no nível mais baixo possível.

A desvantagem é que a entrada do WM \_ não tem nenhum Ballistics aplicado a seus dados, portanto, se você quiser impulsionar um cursor com esses dados, será necessário um esforço extra para que o cursor se comporte da mesma forma que no Windows. para obter mais informações sobre como aplicar o ponteiro ballistics, consulte [ponteiro ballistics para Windows XP](https://www.microsoft.com/whdc/archive/pointer-bal.mspx).

Para obter mais informações sobre a entrada do WM \_ , consulte [sobre a entrada bruta](/windows/desktop/inputdev/about-raw-input).

### <a name="directinput"></a>DirectInput

O [DirectInput](/windows-hardware/drivers/hid/directinput) é um conjunto de chamadas de API que abstrai os dispositivos de entrada no sistema. Internamente, o DirectInput cria um segundo thread para ler os \_ dados de entrada do WM e usar as APIs do DirectInput adicionará mais sobrecarga do que simplesmente ler diretamente a entrada do WM \_ . O DirectInput só é útil para ler dados de joysticks do DirectInput; no entanto, se você só precisar dar suporte ao controlador Xbox 360 para Windows, use [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) em vez disso. Em geral, o uso do DirectInput não oferece nenhuma vantagem ao ler dados de dispositivos de mouse ou de teclado, e o uso do DirectInput nesses cenários não é recomendado.

Compare a complexidade de usar o [DirectInput](/windows-hardware/drivers/hid/directinput), mostrado no código a seguir, para os métodos descritos anteriormente. O seguinte conjunto de chamadas é necessário para criar um mouse do DirectInput:

```cpp
LPDIRECTINPUT8 pDI;
LPDIRECTINPUTDEVICE8 pMouse;

hr = DirectInput8Create(GetModuleHandle(NULL), DIRECTINPUT_VERSION, IID_IDirectInput8, (VOID**)&pDI, NULL);
if(FAILED(hr))
    return hr;

hr = pDI->CreateDevice(GUID_SysMouse, &pMouse, NULL);
if(FAILED(hr))
    return hr;

hr = pMouse->SetDataFormat(&c_dfDIMouse2);
if(FAILED(hr))
    return hr;

hr = pMouse->SetCooperativeLevel(hWnd, DISCL_NONEXCLUSIVE | DISCL_FOREGROUND);
if(FAILED(hr))
    return hr;

if(!bImmediate)
{
    DIPROPDWORD dipdw;
    dipdw.diph.dwSize       = sizeof(DIPROPDWORD);
    dipdw.diph.dwHeaderSize = sizeof(DIPROPHEADER);
    dipdw.diph.dwObj        = 0;
    dipdw.diph.dwHow        = DIPH_DEVICE;
    dipdw.dwData            = 16; // Arbitrary buffer size

    if(FAILED(hr = pMouse->SetProperty(DIPROP_BUFFERSIZE, &dipdw.diph)))
        return hr;
}

pMouse->Acquire();
```

E, em seguida, o dispositivo de mouse do DirectInput pode ser lido em cada quadro:

```cpp
DIMOUSESTATE2 dims2; 
ZeroMemory(&dims2, sizeof(dims2));

hr = pMouse->GetDeviceState(sizeof(DIMOUSESTATE2), &dims2);
if(FAILED(hr)) 
{
    hr = pMouse->Acquire();
    while(hr == DIERR_INPUTLOST) 
        hr = pMouse->Acquire();

    return S_OK; 
}

int xPosRelative = dims2.lX;
int yPosRelative = dims2.lY;
```

## <a name="summary"></a>Resumo

De modo geral, o melhor método para receber dados de movimentação de mouse de alta definição é a entrada do WM \_ . Se os usuários estiverem apenas movendo um ponteiro do mouse, considere usar o WM \_ MOUSEMOVE para evitar a necessidade de executar o ponteiro Ballistics. Essas duas mensagens de janela funcionarão bem mesmo se o mouse não for um mouse de alta definição. ao dar suporte à alta definição, Windows jogos podem oferecer controle mais preciso aos usuários.