---
description: Esta seção explica como recuperar a marcação MathML do controle de entrada matemática usando o Active Template Library (ATL) e o Component Object Model (COM).
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Recebendo entrada do controle de entrada de matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830c8f57bb7b27c305928cf68b658dcc37ede5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793340"
---
# <a name="receiving-input-from-the-math-input-control"></a>Recebendo entrada do controle de entrada de matemática

Esta seção explica como recuperar a marcação MathML do controle de entrada matemática usando o Active Template Library (ATL) e o Component Object Model (COM).

Para recuperar a equação matemática reconhecida do controle de entrada de matemática, você pode substituir o comportamento que acontece quando o botão de inserção é pressionado. Para fazer isso, você precisará configurar um manipulador de eventos que implementa os vários eventos com suporte na interface [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) . A configuração do manipulador de eventos envolve a execução das seguintes etapas para os eventos aos quais você deseja dar suporte (inserir, nesse caso).

-   [Criar uma classe de modelo que contém coletores de eventos](#create-a-template-class-that-contains-event-sinks)
-   [Configurar os manipuladores de eventos](#set-up-the-event-handlers)
-   [Herdar a classe do manipulador de eventos em sua classe principal](#inherit-the-event-handler-class-in-your-main-class)
-   [Inicialize sua classe para herdar o (s) coletor (es) de eventos](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>Criar uma classe de modelo que contém coletores de eventos

Ao implementar um coletor de eventos que usa o controle de entrada de matemática, você deve primeiro especificar uma ID de coletor. Em seguida, você deve criar uma classe de modelo herdada do evento, do manipulador de controle de eventos e das interfaces de evento de controle de entrada matemática. O código a seguir mostra como definir uma ID de coletor e criar uma classe de modelo, CMathInputControlEventHandler, que herda das interfaces necessárias. Essa classe de modelo também é configurada para ter um ponteiro de interface desconhecido privado que será usado para passar o controle de entrada de matemática para ele na inicialização e o \_ membro m ulAdviseCount para contar o número de chamadas para Advise/Unadvise.


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> O membro **m \_ pMain** deve ser diferente em sua implementação se você não estiver usando uma caixa de diálogo.

 

Agora que você tem a classe de modelo básica, deve fornecer uma declaração de encaminhamento para os manipuladores de eventos que serão substituídos e, em seguida, configurar um mapa do coletor para os eventos que você estará lidando. O código a seguir mostra como configurar manipuladores de eventos para o método [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , chamado quando um usuário clica no botão Insert no controle de entrada Math e o método [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , chamado quando um usuário clica no botão Cancel no controle de entrada Math.


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



Como você estará trabalhando com o controle de entrada de matemática, será útil definir uma referência interna para a interface relevante. A função do utilitário a seguir é criada na classe de exemplo para definir essa referência.


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>Configurar os manipuladores de eventos

Depois de configurar os coletores de eventos, será necessário criar suas implementações dos coletores de eventos. Em ambos os métodos no exemplo de código a seguir, os coletores de eventos recuperam um identificador para a interface de controle de entrada matemática. Na função [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , o resultado do reconhecimento é exibido como MathML e o controle é oculto. Na função [**fechar**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , o controle de entrada de matemática está oculto.


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a>Herdar a classe do manipulador de eventos em sua classe principal

Depois de implementar a classe de modelo, você precisará herdá-la na classe em que você configurará seu controle de entrada matemática. Para os fins deste guia, essa classe é uma caixa de diálogo, CMIC \_ test \_ EVENTSDlg. No cabeçalho da caixa de diálogo, os cabeçalhos de requisito devem ser incluídos e a classe de modelo que você criou deve ser herdada. A classe que você está herdando e os manipuladores de eventos devem ter declarações de encaminhamento para que o modelo possa ser implementado. O exemplo de código a seguir mostra como isso é feito.


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> O tipo de modelo, **CMIC \_ test \_ EventsDlg**, será diferente, a menos que você tenha nomeado sua classe da mesma forma que o exemplo.

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>Inicialize sua classe para herdar o (s) coletor (es) de eventos

Depois de configurar sua classe para herdar da classe de modelo, você estará pronto para configurá-la para manipular eventos. Isso consistirá na inicialização da classe para ter um identificador para o controle de entrada matemática e para a classe de chamada. Além disso, o controle de entrada de matemática para manipular eventos de deve ser enviado para o método DispEventAdvise que a classe de exemplo CMathInputControlEventHandler herda. O código a seguir é chamado do método OnInitDialog na classe de exemplo para executar essas ações.


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> O tipo de modelo, CMIC \_ test \_ EventsDlg neste exemplo, será diferente, a menos que você tenha nomeado sua classe da mesma forma que o exemplo.

 

 

 
