---
title: Usando ícones
description: Esta seção fornece exemplos de código que mostram como executar tarefas relacionadas a ícones.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- recursos, ícones
- ícones, criando
- ícones, exibindo
- ícones, compartilhamento de recursos
- criando ícones
- exibindo ícones
- compartilhamento de recursos de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40db7a5828c80dc27780ac54e4110e37a80f44938c9475904ce32089be50d84f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472594"
---
# <a name="using-icons"></a>Usando ícones

Os tópicos a seguir descrevem como executar determinadas tarefas relacionadas a ícones:

-   [Criando um ícone](#creating-an-icon)
-   [Exibindo um ícone](#displaying-an-icon)
-   [Compartilhamento de recursos do ícone](#sharing-icon-resources)

## <a name="creating-an-icon"></a>Criando um ícone

Para usar um ícone, seu aplicativo deve obter um handle para o ícone. O exemplo a seguir mostra como criar dois controles de ícone diferentes: um para o ícone de pergunta padrão e outro para um ícone personalizado incluído como um recurso no arquivo de definição de recursos do aplicativo.


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



Um aplicativo deve implementar ícones personalizados como recursos e deve usar a função [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) ou [**LoadImage,**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) em vez de criar os ícones em tempo de execução. Essa abordagem evita a dependência do dispositivo, simplifica a localização e permite que os aplicativos compartilhem bitmaps de ícone. No entanto, o exemplo a seguir usa [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) para criar um ícone personalizado em tempo de executar, com base em bitmasks de bitmap; ele está incluído para ilustrar como o sistema interpreta bitmasks de bitmap do ícone.


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



Para criar o ícone, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) aplica a tabela de verdade a seguir às máscaras de bits AND e XOR.



| E bitmask | Máscara de bits XOR | Exibir        |
|-------------|-------------|----------------|
| 0           | 0           | Preto          |
| 0           | 1           | Branca          |
| 1           | 0           | Tela         |
| 1           | 1           | Tela inversa |



 

Antes de fechar, seu aplicativo deve usar [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) para destruir qualquer ícone criado usando [**CreateIconIndirect.**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) Não é necessário destruir ícones criados por outras funções.

## <a name="displaying-an-icon"></a>Exibindo um ícone

Seu aplicativo pode carregar e criar ícones a exibir na área de cliente ou janelas filho do aplicativo. O exemplo a seguir demonstra como desenhar um ícone na área de cliente da janela cujo dc (contexto do dispositivo) é identificado pelo *parâmetro hdc.*


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



O sistema exibe automaticamente os ícones de classe de uma janela. Seu aplicativo pode atribuir ícones de classe ao registrar uma classe de janela. Seu aplicativo pode substituir um ícone de classe usando a [**função SetClassLong.**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) Essa função altera as configurações de janela padrão para todas as janelas de uma determinada classe. O exemplo a seguir substitui um ícone de classe pelo ícone cujo identificador de recurso é 480.


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLongPtr(hwnd,          // window handle 
    GCLP_HICON,              // changes icon 
    (LONG_PTR) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



Para obter mais informações sobre classes de janela, consulte [Classes de janela](/windows/desktop/winmsg/window-classes).

## <a name="sharing-icon-resources"></a>Compartilhamento de recursos do ícone

O código a seguir usa as funções [**CreateIconFromResourceEx,**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)e [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex)e várias das funções de recurso, para criar uma alça de ícone com base nos dados de ícone de outro arquivo executável. Em seguida, ele exibe o ícone em uma janela.

**Aviso de segurança:** Usar [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorretamente pode comprometer a segurança do seu aplicativo carregando a DLL incorreta. Consulte a **documentação do LoadLibrary** para obter informações sobre como carregar DLLs corretamente com diferentes versões do Windows.


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
