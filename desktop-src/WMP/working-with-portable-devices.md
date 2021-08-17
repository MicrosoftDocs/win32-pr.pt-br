---
title: Trabalhando com dispositivos portáteis
description: Trabalhando com dispositivos portáteis
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player, dispositivos portáteis
- modelo de objeto Windows Media Player, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Windows Media Player ActiveX controle, dispositivos portáteis
- controle de ActiveX, dispositivos portáteis
- Windows Media Player controle de ActiveX móvel, dispositivos portáteis
- Windows Media Player Dispositivos móveis e portáteis
- dispositivos portáteis, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cbff16b293ac4ab438c1b018608497d2a61cdfa6fb727332d5b50a27de313c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745502"
---
# <a name="working-with-portable-devices"></a>Trabalhando com dispositivos portáteis

esta seção descreve como usar um controle de ActiveX de Windows Media Player remoto para trabalhar com dispositivos portáteis.

Os exemplos de código nesta seção usam classes Active Template Library (ATL), como **CComPtr**.

## <a name="included-headers"></a>Cabeçalhos incluídos

Para usar o código nesta seção, inclua os seguintes cabeçalhos:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a>Ponteiro IWMPPlayer

O ponteiro **IWMPPlayer** é armazenado em uma variável de membro.


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>Os dispositivos são armazenados em uma matriz

O código de exemplo acessa a seguinte variável de membro, a ser declarada no cabeçalho do projeto:


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



A contagem de dispositivos é armazenada em uma variável de membro.


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>Recuperando um ponteiro de dispositivo

Um ponteiro para um dispositivo específico é recuperado por meio de seu índice de matriz usando um código semelhante ao seguinte:


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Observe que o índice mostrado nos exemplos anteriores não é o índice de parceria para o dispositivo. É o índice para o dispositivo na matriz personalizada de dispositivos.

## <a name="cleaning-up"></a>Limpeza

Os exemplos usam a seguinte função para liberar a memória na matriz de dispositivo e para liberar os ponteiros de interface:


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a>Os dispositivos são exibidos em uma caixa de listagem

A função GetSelectedDeviceIndex retorna o índice do dispositivo selecionado pelo usuário em uma caixa de listagem usando o seguinte código:


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a>O estado da interface do usuário é gerenciado por uma única função

A função SetUIState gerencia a interface do usuário.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



Os detalhes dessa função não são relevantes para as discussões nesta seção, mas lembre-se de que essa função executa tarefas como habilitar ou desabilitar controles e alterar o texto de exibição na interface do usuário.

A enumeração UIState foi definida da seguinte maneira:


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



O parâmetro *bConnected* especifica se a interface do usuário deve ser configurada para um dispositivo conectado (true significa que o dispositivo está conectado). Os parâmetros *NewState* e *bConnected* transmitem as informações necessárias para que a função faça seu trabalho.

As seções a seguir fornecem explicações sobre o código de exemplo:

-   [Enumerando dispositivos](enumerating-devices.md)
-   [Recuperando atributos do dispositivo](retrieving-device-attributes.md)
-   [Mostrando o progresso da sincronização](showing-synchronization-progress.md)
-   [Gerenciando listas de reprodução de sincronização](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de controle do Player**](player-control-guide.md)
</dt> </dl>

 

 




