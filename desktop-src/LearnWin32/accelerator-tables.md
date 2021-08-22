---
title: Tabelas do acelerador
description: Tabelas do acelerador
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504749b6fad794f5f587e035f0dbc81662aa8b5faaf9b9eb13de365dd9a8d312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146439"
---
# <a name="accelerator-tables"></a>Tabelas do acelerador

Os aplicativos geralmente definem atalhos de teclado, como CTRL + O para o comando File Open. Você pode implementar atalhos de teclado manipulando mensagens do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) individuais, mas as tabelas de aceleração fornecem uma solução melhor que:

-   Requer menos codificação.
-   Consolida todos os seus atalhos em um arquivo de dados.
-   Dá suporte à localização em outros idiomas.
-   Permite que atalhos e comandos de menu usem a mesma lógica do aplicativo.

Uma *tabela de acelerador* é um recurso de dados que mapeia combinações de teclado, como CTRL + O, para comandos de aplicativo. Antes de veremos como usar uma tabela de acelerador, precisaremos de uma rápida introdução aos recursos. Um *recurso* é um blob de dados que é compilado em um binário de aplicativo (exe ou dll). Os recursos armazenam dados que são necessários para o aplicativo, como menus, cursores, ícones, imagens, cadeias de caracteres de texto ou qualquer dado de aplicativo personalizado. O aplicativo carrega os dados do recurso do binário em tempo de execução. Para incluir recursos em um binário, faça o seguinte:

1.  Crie um arquivo de definição de recurso (. rc). Esse arquivo define os tipos de recursos e seus identificadores. O arquivo de definição de recurso pode incluir referências a outros arquivos. Por exemplo, um recurso de ícone é declarado no arquivo. rc, mas a imagem de ícone é armazenada em um arquivo separado.
2.  Use o compilador de recursos do Microsoft Windows (RC) para compilar o arquivo de definição de recurso em um arquivo de recurso compilado (. res). o compilador RC é fornecido com Visual Studio e também o SDK do Windows.
3.  Vincule o arquivo de recurso compilado ao arquivo binário.

Essas etapas são aproximadamente equivalentes ao processo de compilação/vínculo para arquivos de código. Visual Studio fornece um conjunto de editores de recursos que facilitam a criação e a modificação de recursos. (Essas ferramentas não estão disponíveis nas edições Express do Visual Studio.) Mas um arquivo. rc é simplesmente um arquivo de texto, e a sintaxe é documentada no MSDN, portanto, é possível criar um arquivo. rc usando qualquer editor de texto. Para obter mais informações, consulte [About Resource files](/windows/desktop/menurc/about-resource-files).

## <a name="defining-an-accelerator-table"></a>Definindo uma tabela de acelerador

Uma tabela de acelerador é uma tabela de atalhos de teclado. Cada atalho é definido por:

-   Um identificador numérico. Esse número identifica o comando do aplicativo que será invocado pelo atalho.
-   O caractere ASCII ou o código de chave virtual do atalho.
-   Chaves modificadoras opcionais: ALT, SHIFT ou CTRL.

A própria tabela do acelerador tem um identificador numérico, que identifica a tabela na lista de recursos do aplicativo. Vamos criar uma tabela de acelerador para um simples programa de desenho. Este programa terá dois modos, modo de desenho e modo de seleção. No modo de desenho, o usuário pode desenhar formas. No modo de seleção, o usuário pode selecionar formas. Para este programa, gostaríamos de definir os seguintes atalhos de teclado.



| Atalho | Comando                   |
|----------|---------------------------|
| CTRL+M   | Alternar entre os modos.     |
| F1       | Alterne para o modo de desenho.      |
| F2       | Alternar para o modo de seleção. |



 

Primeiro, defina identificadores numéricos para a tabela e para os comandos do aplicativo. Esses valores são arbitrários. Você pode atribuir constantes simbólicas para os identificadores definindo-os em um arquivo de cabeçalho. Por exemplo:


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



Neste exemplo, o valor `IDR_ACCEL1` identifica a tabela de acelerador e as três constantes a seguir definem os comandos do aplicativo. Por convenção, um arquivo de cabeçalho que define constantes de recurso é geralmente denominado Resource. h. A próxima listagem mostra o arquivo de definição de recurso.


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



Os atalhos do acelerador são definidos entre chaves. Cada atalho contém as entradas a seguir.

-   O código de chave virtual ou o caractere ASCII que invoca o atalho.
-   O comando do aplicativo. Observe que as constantes simbólicas são usadas no exemplo. O arquivo de definição de recurso inclui Resource. h, em que essas constantes são definidas.
-   A palavra-chave **VIRTKEY** significa que a primeira entrada é um código de chave virtual. A outra opção é usar caracteres ASCII.
-   Modificadores opcionais: ALT, CONTROL ou SHIFT.

Se você usar caracteres ASCII para atalhos, um caractere minúsculo será um atalho diferente de um caractere maiúsculo. (Por exemplo, digitar ' a ' pode invocar um comando diferente do que digitar ' A '.) Isso pode confundir os usuários, portanto, geralmente é melhor usar códigos de chave virtual, em vez de caracteres ASCII, para atalhos.

## <a name="loading-the-accelerator-table"></a>Carregando a tabela de acelerador

O recurso para a tabela de acelerador deve ser carregado antes que o programa possa usá-lo. Para carregar uma tabela de acelerador, chame a função [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



Chame essa função antes de inserir o loop de mensagem. O primeiro parâmetro é o identificador para o módulo. (Esse parâmetro é passado para sua função [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) . Para obter detalhes, consulte [WinMain: o ponto de entrada do aplicativo](winmain--the-application-entry-point.md).) O segundo parâmetro é o identificador de recurso. A função retorna um identificador para o recurso. Lembre-se de que um identificador é um tipo opaco que se refere a um objeto gerenciado pelo sistema. Se a função falhar, ela retornará **NULL**.

Você pode liberar uma tabela de acelerador chamando [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable). No entanto, o sistema libera automaticamente a tabela quando o programa é encerrado, portanto, você só precisa chamar essa função se estiver substituindo uma tabela por outra. Há um exemplo interessante disso no tópico [criando aceleradores editáveis do usuário](/windows/desktop/menurc/using-keyboard-accelerators).

## <a name="translating-key-strokes-into-commands"></a>Convertendo traços de chave em comandos

Uma tabela de acelerador funciona convertendo os traços de chave em mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . O parâmetro *wParam* do **\_ comando do WM** contém o identificador numérico do comando. Por exemplo, usando a tabela mostrada anteriormente, o pressionamento de tecla CTRL + M é convertido em uma mensagem de **\_ comando do WM** com o valor `ID_TOGGLE_MODE` . Para fazer isso acontecer, altere o loop de mensagem para o seguinte:


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



Esse código adiciona uma chamada para a função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) dentro do loop de mensagem. A função **TranslateAccelerator** examina cada mensagem de janela, procurando mensagens de chave para baixo. Se o usuário pressionar uma das combinações de teclas listadas na tabela do acelerador, **TranslateAccelerator** enviará uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para a janela. A função envia **o \_ comando do WM** invocando diretamente o procedimento de janela. Quando **TranslateAccelerator** converte com êxito um traço de chave, a função retorna um valor diferente de zero, o que significa que você deve ignorar o processamento normal da mensagem. Caso contrário, **TranslateAccelerator** retornará zero. Nesse caso, passe a mensagem de janela para [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), como de costume.

Veja como o programa de desenho pode manipular a mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) :


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



Esse código pressupõe que `SetMode` é uma função definida pelo aplicativo para alternar entre os dois modos. Os detalhes de como você trataria cada comando obviamente dependem do seu programa.

## <a name="next"></a>Avançar

[Definindo a imagem do cursor](setting-the-cursor-image.md)

 

 
