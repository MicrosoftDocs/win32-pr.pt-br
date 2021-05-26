---
title: Versões de controle comum
description: Este tópico lista as versões disponíveis da biblioteca de Controle Comum (ComCtl32.dll), descreve como identificar a versão que seu aplicativo está usando e explica como direcionar seu aplicativo para uma versão específica.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1131466bd4d3afcaae3a241a6f7854fd5a49450
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423956"
---
# <a name="common-control-versions"></a>Versões de controle comum

Este tópico lista as versões disponíveis da biblioteca de Controle Comum (ComCtl32.dll), descreve como identificar a versão que seu aplicativo está usando e explica como direcionar seu aplicativo para uma versão específica.

Este tópico inclui as seções a seguir.

-   [Números de versões de DLL de controle comum](#common-control-dll-versions-numbers)
-   [Tamanhos de estrutura para versões de controle comuns diferentes](#structure-sizes-for-different-common-control-versions)
-   [Usando DllGetVersion para determinar o número de versão](#using-dllgetversion-to-determine-the-version-number)
-   [Versões do projeto](#project-versions)
-   [Tópicos relacionados](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>Números de versões de DLL de controle comum

O suporte para controles comuns é fornecido pelo ComCtl32.dll, que inclui todas as versões de 32 bits e 64 bits do Windows. Cada versão sucessiva da DLL dá suporte aos recursos e à API de versões anteriores e adiciona novos recursos.

Como várias versões do ComCtl32.dll foram distribuídas com Internet Explorer, a versão que está ativa às vezes é diferente da versão que foi enviada com o sistema operacional. Portanto, seu aplicativo deve determinar diretamente qual versão do ComCtl32.dll está presente.

Na documentação de referência de controles comuns, muitos elementos de programação especificam um número mínimo de versão de DLL com suporte. Esse número de versão indica que o elemento de programação é implementado nessa versão e nas versões subsequentes da DLL, a menos que especificado de outra forma. Se nenhum número de versão for especificado, o elemento de programação será implementado em todas as versões existentes da DLL.

A tabela a seguir descreve as diferentes versões de DLL e como elas foram distribuídas em SOs com suporte.



ComCtl32.dll

Versão

Plataforma de distribuição

5.81

Microsoft Internet Explorer 5, 1, Microsoft Internet Explorer 5,5 e Microsoft Internet Explorer 6

5,82

Windows Server 2003, Windows Vista, Windows Server 2008 e Windows 7

6,0

Windows Server 2003

6.10

Windows Vista, Windows Server 2008 e Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>Tamanhos de estrutura para diferentes versões de controle comuns

Os aprimoramentos contínuos para controles comuns resultaram na necessidade de estender muitas das estruturas. Por esse motivo, o tamanho das estruturas foi alterado entre diferentes versões de commctrl. h. Como a maioria das estruturas de controle comuns assume um tamanho de estrutura como um dos parâmetros, uma mensagem ou função pode falhar se o tamanho não for reconhecido. Para corrigir isso, as constantes de tamanho da estrutura foram definidas para auxiliar na destinação à versão diferente do ComCtl32.dll. A lista a seguir define as constantes de tamanho da estrutura.



|    Constante de tamanho da estrutura                           |     Definição                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| Tamanho de HDITEM \_ v1 \_              | O tamanho da estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) na versão 4,0.                           |
| Tamanho da IMAGELISTDRAWPARAMS \_ v3 \_ | O tamanho da estrutura [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) na versão 5,9. |
| Tamanho de LVCOLUMN \_ v1 \_            | O tamanho da estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) na versão 4,0.                       |
| \_Tamanho LVGROUP V5 \_             | O tamanho da estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) na versão 6,0.                         |
| Tamanho de LVHITTESTINFO \_ v1 \_       | O tamanho da estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) na versão 4.0.             |
| LVITEM \_ V1 \_ SIZE              | O tamanho da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) na versão 4.0.                           |
| LVITEM \_ V5 \_ SIZE              | O tamanho da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) na versão 6.0.                           |
| TAMANHO LVTILEINFO \_ V5 \_          | O tamanho da estrutura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) na versão 6.0.                   |
| TAMANHO DO MCHITTESTINFO \_ V1 \_       | O tamanho da [**estrutura MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) na versão 4.0.             |
| NMLVCUSTOMDRAW \_ TAMANHO V3 \_      | O tamanho da estrutura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) na versão 4.7.           |
| TAMANHO DE NMTTDISPINFO \_ V1 \_        | O tamanho da [**estrutura NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) na versão 4.0.               |
| NMTVCUSTOMDRAW \_ TAMANHO V3 \_      | O tamanho da estrutura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) na versão 4.7.           |
| TAMANHO DE PROPSHEETHEADER \_ V1 \_     | O tamanho da estrutura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) na versão 4.0.         |
| TAMANHO DE PROPSHEETPAGE \_ V1 \_       | O tamanho da estrutura [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) na versão 4.0.             |
| TAMANHO REBARBANDINFO \_ V3 \_       | O tamanho da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) na versão 4,7.             |
| \_Tamanho do V6 REBARBANDINFO \_       | O tamanho da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) na versão 6,0.             |
| Tamanho de TTTOOLINFO \_ v1 \_          | O tamanho da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) na versão 4,0.                       |
| Tamanho de TTTOOLINFO \_ v2 \_          | O tamanho da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) na versão 4,7.                       |
| Tamanho da TTTOOLINFO \_ v3 \_          | O tamanho da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) na versão 6,0.                       |
| Tamanho de TVINSERTSTRUCT \_ v1 \_      | O tamanho da estrutura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) na versão 4,0.           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Usando DllGetVersion para determinar o número de versão

A função [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) pode ser chamada por um aplicativo para determinar qual versão de dll está presente no sistema.

[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) retorna uma estrutura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . Além das informações fornecidas por meio do [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), o **DLLVERSIONINFO2** também fornece o número do hotfix que identifica o Service Pack mais recente instalado, que fornece uma maneira mais robusta de comparar os números de versão. Como o primeiro membro de **DLLVERSIONINFO2** é uma estrutura **DLLVERSIONINFO** , a estrutura posterior é compatível com versões anteriores.


A função de exemplo a seguir `GetVersion` carrega uma DLL especificada e tenta chamar sua função [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) . Se for bem-sucedido, ele usará uma macro para empacotar os números de versão principal e secundária da estrutura [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) em um **DWORD** que é retornado para o aplicativo de chamada. Se a DLL não exportar **DllGetVersion**, a função retornará zero. Você pode modificar a função para lidar com a possibilidade de que **DllGetVersion** retorne uma estrutura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . Nesse caso, use as informações no membro **ullVersion** dessa estrutura **DLLVERSIONINFO2** para comparar versões, números de build e service pack versões. A [**macro MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) simplifica a tarefa de comparar esses valores com aqueles em **ullVersion.**

> [!Note]  
> Usar [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorretamente pode representar riscos de segurança. Consulte a **documentação do LoadLibrary** para obter informações sobre como carregar DLLs corretamente com versões diferentes do Windows.

 


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```



O exemplo de código a seguir mostra como você pode `GetVersion` usar para testar se ComCtl32.dll é a versão 6.0 ou posterior.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a>Versões do projeto

Para garantir que seu aplicativo seja compatível com diferentes versões direcionadas de um arquivo .dll, as macros de versão estão presentes nos arquivos de header. Essas macros são usadas para definir, excluir ou redefinir determinadas definições para versões diferentes da DLL. Consulte [Usando os Headers do Windows](/windows/desktop/WinProg/using-the-windows-headers) para ver uma descrição detalhada dessas macros.

Por exemplo, o nome da macro **\_ WIN32 \_ IE** normalmente é encontrado em títulos mais antigos. Você é responsável por definir a macro como um número hexadecimal. Esse número de versão define a versão de destino do aplicativo que está usando a DLL. A tabela a seguir mostra os números de versão disponíveis e o efeito que cada um tem em seu aplicativo.



| Versão | Descrição                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | O aplicativo é compatível com ComCtl32.dll versão 4.70 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 4.70. |
| 0x0400  | O aplicativo é compatível com ComCtl32.dll versão 4.71 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 4.71. |
| 0x0401  | O aplicativo é compatível com ComCtl32.dll versão 4.72 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 4.72. |
| 0x0500  | O aplicativo é compatível com ComCtl32.dll versão 5,80 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 5,80. |
| 0x0501  | O aplicativo é compatível com ComCtl32.dll versão 5,81 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 5,81. |
| 0x0600  | O aplicativo é compatível com ComCtl32.dll versão 6,0 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 6,0.   |



 

Se você não definir a macro **\_ \_ IE do Win32** em seu projeto, ela será definida automaticamente como 0x0500. Para definir um valor diferente, você pode adicionar o seguinte às diretivas do compilador em seu arquivo Make; Substitua o número de versão desejado por 0x0400.


```C++
/D _WIN32_IE=0x0400
```



Outro método é adicionar uma linha semelhante à seguinte em seu código-fonte antes de incluir os arquivos de cabeçalho do Shell. Substitua o número de versão desejado por 0x0400.


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles comuns](common-controls-intro.md)
</dt> </dl>

 

 