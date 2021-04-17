---
description: Este programa verifica a presença e a configuração dos componentes principais do PC MicrosoftTablet e do touch Technology.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Exemplo de informações sobre a plataforma do Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d815f21233b1edcc90d456df68b3736c170a5fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764064"
---
# <a name="tablet-pc-platform-info-sample"></a><span data-ttu-id="cc7ba-103">Exemplo de informações sobre a plataforma do Tablet PC</span><span class="sxs-lookup"><span data-stu-id="cc7ba-103">Tablet PC Platform Info Sample</span></span>

<span data-ttu-id="cc7ba-104">Este programa verifica a presença e a configuração dos componentes principais do PC MicrosoftTablet e do touch Technology.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-104">This program checks the presence and configuration of the MicrosoftTablet PC and Touch Technology core components.</span></span> <span data-ttu-id="cc7ba-105">Ele determina se os componentes do Tablet PC estão habilitados no sistema operacional, listando nomes e informações de versão para controles principais e o reconhecedor de fala e manuscrito padrão.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-105">It determines whether Tablet PC components are enabled in the operating system, listing names and version information for core controls and the default handwriting and speech recognizer.</span></span>

<span data-ttu-id="cc7ba-106">O aplicativo usa a API do Windows GetSystemMetrics, passando o Tablet do SM \_ , para determinar se o aplicativo está sendo executado em um Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-106">The application uses the GetSystemMetrics Windows API, passing in SM\_TABLETPC, to determine whether the application running on a Tablet PC.</span></span> <span data-ttu-id="cc7ba-107">O SM \_ Tablet é definido em winuser. h.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-107">SM\_TABLETPC is defined in WinUser.h.</span></span>

<span data-ttu-id="cc7ba-108">De interesse específico é a maneira como o aplicativo usa a coleção reconhecedores para fornecer informações sobre o reconhecedor padrão.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-108">Of particular interest is the way the application uses the Recognizers collection to provide information about the default recognizer.</span></span> <span data-ttu-id="cc7ba-109">Antes de tentar usar a coleção de reconhecedores e o objeto reconhecedor, o aplicativo testa a criação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-109">Before attempting to use the Recognizers collection and Recognizer object, the application tests for their successful creation.</span></span>

## <a name="components"></a><span data-ttu-id="cc7ba-110">Componentes</span><span class="sxs-lookup"><span data-stu-id="cc7ba-110">Components</span></span>

<span data-ttu-id="cc7ba-111">Usando o módulo de mesclagem redistribuível, determinadas partes da API da plataforma do Tablet PC podem ser instaladas em versões não-Tablet do vista e do Windows XP Professional.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-111">Using the re-distributable merge module, certain parts of the Tablet PC Platform API may be installed on non-Tablet versions of Vista and Windows XP Professional .</span></span> <span data-ttu-id="cc7ba-112">A chamada GetSystemMetrics indica apenas que o Windows XP Tablet PC Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-112">The GetSystemMetrics call only indicates that Windows XP Tablet PC Edition is installed.</span></span> <span data-ttu-id="cc7ba-113">Um aplicativo sempre deve determinar se um determinado componente está disponível.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-113">An application should always determine if a given component is available.</span></span> <span data-ttu-id="cc7ba-114">A maneira apropriada de determinar se um componente da API está instalado é tentar criar uma instância de um objeto ou controle e verificar se ela existe antes de tentar usá-la, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-114">The proper way to determine if a component of the API is installed is to attempt to create an instance of an object or control and check that it exists before attempting to use it, as shown in the following example.</span></span>


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



<span data-ttu-id="cc7ba-115">O aplicativo descobre sobre os componentes de fala instalados examinando a chave do registro apropriada:</span><span class="sxs-lookup"><span data-stu-id="cc7ba-115">The application finds out about the installed speech components by looking in the appropriate registry key:</span></span>


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



<span data-ttu-id="cc7ba-116">A chave é lida usando RegQueryValueExW.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-116">The key is read using RegQueryValueExW.</span></span>

<span data-ttu-id="cc7ba-117">Por fim, o exemplo descobre quais controles estão instalados.</span><span class="sxs-lookup"><span data-stu-id="cc7ba-117">Finally, the sample finds out which controls are installed.</span></span>


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



