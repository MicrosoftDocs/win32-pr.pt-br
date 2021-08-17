---
description: Esta seção descreve como determinar a versão das DLLs de Shell em que seu aplicativo está em execução e como direcionar seu aplicativo para uma versão específica.
title: 'Versões de DLL do Shell e Shlwapi '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6d74371478b30037e75b1c168dc235735ba6bd219fa461245262ff55a508ae5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967827"
---
# <a name="shell-and-shlwapi-dll-versions"></a>Versões de DLL do Shell e Shlwapi 

Esta seção descreve como determinar a versão das DLLs de Shell em que seu aplicativo está em execução e como direcionar seu aplicativo para uma versão específica.

-   [Números de versão da DLL](#dll-version-numbers)
-   [Usando DllGetVersion para determinar o número de versão](#using-dllgetversion-to-determine-the-version-number)
    -   [Usando DllGetVersion](#using-dllgetversion)
-   [Project Versões](#project-versions)

## <a name="dll-version-numbers"></a>Números de versão da DLL

Todos, exceto alguns dos elementos de programação discutidos na documentação do Shell, estão contidos em duas DLLs: Shell32.dll e Shlwapi.dll. Devido a aprimoramentos contínuos, versões diferentes dessas DLLs implementam recursos diferentes. Em toda a documentação de referência do Shell, cada elemento de programação especifica um número de versão da DLL com suporte mínimo. Esse número de versão indica que o elemento de programação é implementado nessa versão e nas versões subsequentes da DLL, a menos que especificado de outra forma. Se nenhum número de versão for especificado, o elemento de programação será implementado em todas as versões existentes da DLL.

antes de Windows XP, novas versões Shell32.dll e Shlwapi.dll às vezes eram fornecidas com novas versões do Windows Internet Explorer. a partir do Windows XP, essas DLLs não eram mais fornecidas como arquivos redistribuíveis fora das novas versões do Windows em si. a tabela a seguir descreve as diferentes versões de DLL e como elas foram distribuídas de volta para o microsoft Internet Explorer 3,0, o Windows 95 e o microsoft Windows NT 4,0.

Shell32.dll versão 4,0 é encontrada nas versões originais do Windows 95 e do Microsoft Windows NT 4,0. O shell não foi atualizado com a versão 3,0 do Internet Explorer, portanto Shell32.dll não tem uma versão 4,70. Shell32.dll versões 4,71 e 4,72 foram enviadas com as versões correspondentes do Internet Explorer, mas elas não foram necessariamente instaladas (consulte a observação 1). para versões posteriores ao Microsoft Internet Explorer 4, 1 e Windows 98, os números de versão para Shell32.dll e Shlwapi.dll divergência. Em geral, você deve assumir que as DLLs têm números de versão diferentes e testar cada uma separadamente.

#### <a name="shell32dll"></a>Shell32.dll

| Versão | Plataforma de distribuição                                                       |
|---------|-----------------------------------------------------------------------------|
| 4,0     | Windows 95 e Microsoft Windows NT 4,0                                     |
| 4,71    | Microsoft Internet Explorer 4,0. Consulte a observação 1.                                |
| 4.72    | Internet Explorer 4, 1 e Windows 98. Consulte a observação 1.                          |
| 5.0     | Windows 2000 e Windows Millennium Edition (Windows Me). Consulte a observação 2.       |
| 6,0     | Windows XP                                                                  |
| 6.0.1   | Windows Vista                                                               |
| 6.1     | Windows 7                                                                   |

#### <a name="shlwapidll"></a>Shlwapi.dll

| Versão | Plataforma de distribuição                                                       |
|---------|-----------------------------------------------------------------------------|
| 4,0     | Windows 95 e Microsoft Windows NT 4,0                                     |
| 4,71    | Internet Explorer 4,0. Consulte a observação 1.                                          |
| 4.72    | Internet Explorer 4, 1 e Windows 98. Consulte a observação 1.                          |
| 4.7     | Internet Explorer 3. x                                                       |
| 5.0     | ES do Microsoft Internet Explorer 5 e Windows 98. Consulte a observação 2.                |
| 5.5     | Microsoft Internet Explorer 5,5 e Windows Millennium Edition (Windows Me) |
| 6,0     | Windows XP e Windows Vista                                                |



**Observação 1:** Todos os sistemas com o Internet Explorer 4,0 ou 4, 1 tinham a versão associada do Shlwapi.dll (4,71 ou 4,72, respectivamente). no entanto, para sistemas anteriores à Windows 98, o Internet Explorer 4,0 e 4, 1 podem ser instalados com ou sem o que era conhecido como *Shell integrado*. Se o Internet Explorer foi instalado com o Shell integrado, a versão associada do Shell32.dll (4,71 ou 4,72) também foi instalada. Se o Internet Explorer foi instalado sem o Shell integrado, Shell32.dll permaneceu como a versão 4,0. Em outras palavras, a presença da versão 4,71 ou 4,72 de Shlwapi.dll em um sistema não garante que Shell32.dll tenha o mesmo número de versão. todos os sistemas Windows 98 têm a versão 4,72 do Shell32.dll.

**Observação 2:** a versão 5,0 do Shlwapi.dll foi distribuída com o internet explorer 5 e foi encontrada em todos os sistemas nos quais o internet explorer 5 foi instalado, com exceção de Windows 2000. a versão 5,0 do Shell32.dll foi distribuída nativamente com Windows 2000 e Windows Millennium Edition (Windows Me), junto com a versão 5,0 do Shlwapi.dll.

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Usando DllGetVersion para determinar o número de versão

A partir da versão 4,71, as DLLs do Shell, entre outras, começaram a exportar [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Essa função pode ser chamada por um aplicativo para determinar qual versão de DLL está presente no sistema.

> [!Note]  
> As DLLs não necessariamente exportam [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Sempre teste-o antes de tentar usá-lo.

para Windows versões anteriores a Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) retorna uma estrutura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) que contém os números de versão principal e secundária, o número da compilação e uma ID de plataforma. para os sistemas Windows 2000 e posteriores, **DllGetVersion** pode retornar uma estrutura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) . Além das informações fornecidas por meio do **DLLVERSIONINFO**, o **DLLVERSIONINFO2** também fornece o número do hotfix que identifica o Service Pack mais recente instalado, que fornece uma maneira mais robusta de comparar os números de versão. Como o primeiro membro de **DLLVERSIONINFO2** é uma estrutura **DLLVERSIONINFO** , a estrutura posterior é compatível com versões anteriores.

### <a name="using-dllgetversion"></a>Usando DllGetVersion

A função de exemplo a seguir `GetVersion` carrega uma DLL especificada e tenta chamar sua função [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) . Se for bem-sucedido, ele usará uma macro para empacotar os números de versão principal e secundária da estrutura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) em um **DWORD** que é retornado para o aplicativo de chamada. Se a DLL não exportar **DllGetVersion**, a função retornará zero. com os sistemas Windows 2000 e posteriores, você pode modificar a função para lidar com a possibilidade de que **DllGetVersion** retorne uma estrutura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) . Nesse caso, use as informações contidas no membro **ullVersion** da estrutura **DLLVERSIONINFO2** para comparar versões, números de compilação e Service Pack versões. A macro [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) simplifica a tarefa de comparar esses valores com aqueles em **ullVersion**.

> [!Note]  
> Usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorretamente pode representar riscos de segurança. Consulte a documentação **LoadLibrary** para obter informações sobre como carregar corretamente DLLs com versões diferentes do Windows.


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

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

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


O exemplo de código a seguir ilustra como você pode usar o `GetVersion` para testar se Shell32.dll é a versão 6,0 ou posterior.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a>Project Versões

Para garantir que seu aplicativo seja compatível com versões de destino diferentes de um arquivo de .dll, as macros de versão estão presentes nos arquivos de cabeçalho. Essas macros são usadas para definir, excluir ou redefinir determinadas definições para diferentes versões da DLL. consulte [usando os cabeçalhos de Windows](../winprog/using-the-windows-headers.md) para obter uma descrição detalhada dessas macros.

Por exemplo, o nome da macro **\_ Win32 \_ IE** normalmente é encontrado em cabeçalhos mais antigos. Você é responsável por definir a macro como um número hexadecimal. Esse número de versão define a versão de destino do aplicativo que está usando a DLL. A tabela a seguir mostra os números de versão disponíveis e o efeito que cada um tem em seu aplicativo.


| Versão | Descrição                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0200  | O aplicativo é compatível com Shell32.dll versão 4, 0 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 4, 0.                                              |
| 0x0300  | O aplicativo é compatível com Shell32.dll versão 4,70 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 4,70.                                              |
| 0x0400  | O aplicativo é compatível com Shell32.dll versão 4,71 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 4,71.                                              |
| 0x0401  | O aplicativo é compatível com Shell32.dll versão 4,72 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 4,72.                                              |
| 0x0500  | O aplicativo é compatível com Shell32.dll e Shlwapi.dll versão 5,0 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 5,0 de Shell32.dll e Shlwapi.dll. |
| 0x0501  | O aplicativo é compatível com Shell32.dll e Shlwapi.dll versão 5,0 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 5,0 de Shell32.dll e Shlwapi.dll. |
| 0x0600  | O aplicativo é compatível com Shell32.dll e Shlwapi.dll versão 6,0 e posterior. O aplicativo não pode implementar recursos que foram adicionados após a versão 6,0 de Shell32.dll e Shlwapi.dll. |


Se você não definir a macro **\_ \_ IE do Win32** em seu projeto, ela será definida automaticamente como 0x0500. Para definir um valor diferente, você pode adicionar o seguinte às diretivas do compilador em seu arquivo Make; Substitua o número de versão desejado por 0x0400.

```
/D _WIN32_IE=0x0400
```

Outro método é adicionar uma linha semelhante à seguinte em seu código-fonte antes de incluir os arquivos de cabeçalho do Shell. Substitua o número de versão desejado por 0x0400.

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
