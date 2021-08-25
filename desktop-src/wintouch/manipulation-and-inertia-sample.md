---
title: Amostra de manipulação e inércia
description: O exemplo de Manipulação e Inércia mostra como adicionar o Windows Touch a aplicativos nativos baseados em Windows que usam a API Windows Touch.
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows Toque, exemplos de código
- Windows Toque, código de exemplo
- Windows Toque, manipulações
- Windows Toque, inércia
- Windows Exemplo de toque, manipulação e inércia
- Amostra de manipulação e inércia
- Windows Touch,_IManipulationEventSink interface
- Windows Touch, interface IManipulationProcessor
- Windows Touch, interface IInertiaProcessor
- manipulações, código de exemplo
- manipulações, exemplos de código
- manipulações, _IManipulationEventSink interface
- manipulations,interface IManipulationProcessor
- inércia, código de exemplo
- inércia, exemplos de código
- inertia, interface IInertiaProcessor
- _IManipulationEventSink interface
- Interface IManipulationProcessor, exemplos de código
- Interface IManipulationProcessor, código de exemplo
- Interface IInertiaProcessor, exemplos de código
- Interface IInertiaProcessor, código de exemplo
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 8b6471362d30b6efc9dfa0c4f07df70f014c8cb72866c92bbb04c9eb33463410
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840586"
---
# <a name="manipulation-and-inertia-sample"></a>Amostra de manipulação e inércia

O exemplo de Manipulação e Inércia mostra como adicionar o Windows Touch a aplicativos nativos baseados em Windows que usam a API Windows Touch. O exemplo implementa os recursos básicos da API para habilitar a tradução, a rotação e o dimensionamento para objetos e a aplicação de propriedades de inércia a eles. O exemplo também mostra como dar suporte básico ao mouse para seus aplicativos Windows Touch. A imagem a seguir mostra a aparência do exemplo quando ele é executado.

![captura de tela que mostra duas caixas com gradientes na amostra de manipulação e inércia](images/manip-inertia-sample.png)

As caixas com gradientes podem ser manipuladas independentemente por um usuário quando ele executar o aplicativo de um computador que dá suporte ao Windows Touch.

## <a name="register-the-touch-window"></a>Registrar a janela de toque

Antes de receber a entrada por toque, primeiro você deve notificar o sistema de que seu aplicativo é um aplicativo Windows Touch chamando a seguinte função:

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a>Implementar a _IManipulationEventSink interface

O [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) de eventos contém três funções: [**ManipulationStarted,**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted.**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) Essas funções de retorno de chamada são usadas pela interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e pela interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para retornar os valores calculados pelos processadores depois de invocarem as funções [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)e [**ProcessMoveWithTime.**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) O exemplo de código a seguir mostra um exemplo de implementação **de uma _IManipulationEvents** interface.

```C++
#include "cmanipulationeventsink.h"
#include <math.h>

CManipulationEventSink::CManipulationEventSink(HWND hWnd, CDrawingObject *dObj, int iTimerId, BOOL inertia) {
    // Manipulation & Inertia Processors
    m_manip = NULL;
    m_inert = NULL;

    // Connection points for COM.
    m_pConPointContainer = NULL;
    m_pConnPoint = NULL;

    // Reference to an object associated with this event sink.
    m_dObj = dObj;

    // Handle to the window used for computing boundaries.
    m_hWnd = hWnd;

    // The unique timer id for this manipulation event sink.
    m_iTimerId = iTimerId;

    m_bInertia = inertia;

    m_cRefCount = 1;
}


CManipulationEventSink::~CManipulationEventSink()
{

}


HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted(
    FLOAT x,
    FLOAT y)
{
    KillTimer(m_hWnd, m_iTimerId);

    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    FLOAT x,
    FLOAT y,
    FLOAT translationDeltaX,
    FLOAT translationDeltaY,
    FLOAT scaleDelta,
    FLOAT expansionDelta,
    FLOAT rotationDelta,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    FLOAT pivot = 0.0f;

    // Apply transformation based on rotationDelta (in radians).
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta.
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta.
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    if(!m_bInertia)
    {
        // Set values for one-finger rotations.
        FLOAT fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->GetWidth()/2, 2)
                           + pow(m_dObj->GetHeight()/2, 2)))*0.4f;
        FLOAT fPivotPtX    = m_dObj->GetCenterX();
        FLOAT fPivotPtY    = m_dObj->GetCenterY();

        m_manip->put_PivotPointX(fPivotPtX);
        m_manip->put_PivotPointY(fPivotPtY);
        m_manip->put_PivotRadius(fPivotRadius);
    }
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted(
    FLOAT x,
    FLOAT y,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    if(!m_bInertia)
    {
        SetupInertia();

        // Kick off timer that handles inertia.
        SetTimer(m_hWnd, m_iTimerId, DESIRED_MILLISECONDS, NULL);
    }
    else
    {
        // Stop timer that handles inertia.
        KillTimer(m_hWnd, m_iTimerId);
    }

    return S_OK;
}
```

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a>Criar objetos COM e configurar as interfaces IManipulationProcessor e IInertiaProcessor

A API fornece uma implementação das interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) [**e IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) Você deve criar uma instância do e referenciar os objetos COM do sink de eventos [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) que foi implementado anteriormente.

## <a name="handle-wm_touch-messages"></a>Manipular WM_TOUCH mensagens

Os dados de entrada devem ser extraídos das mensagens [**WM_TOUCH**](wm-touchdown.md) e, em seguida, posteriormente devem ser processados para alimentar o processador de manipulação correto.

```C++
switch (msg)
{
    case WM_TOUCH:

      iNumContacts = LOWORD(wParam);
      hInput       = (HTOUCHINPUT)lParam;
      pInputs      = new TOUCHINPUT[iNumContacts];

      // Get each touch input info and feed each
      // tagTOUCHINPUT into the process input handler.

      if(pInputs != NULL)
      {
          if(GetTouchInputInfo(hInput, iNumContacts,
               pInputs, sizeof(TOUCHINPUT)))
          {
              for(int i = 0; i < iNumContacts; i++)
              {
                  // Bring touch input info into client coordinates.
                  ptInputs.x = pInputs[i].x/100;
                  ptInputs.y = pInputs[i].y/100;
                  ScreenToClient(g_hWnd, &ptInputs);

                  pInputs[i].x = ptInputs.x;
                  pInputs[i].y = ptInputs.y;

                  g_ctDriver->ProcessInputEvent(pInputs[i]);
              }
          }
      }

      delete [] pInputs;
      break;
}
```

> [!Note]  
> Para usar a função [**ScreenToClient,**](/windows/desktop/api/winuser/nf-winuser-screentoclient) você deve ter suporte de DPI alto em seu aplicativo. Para obter mais informações sobre como dar suporte a alto DPI, visite a [seção DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) alto do MSDN.

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a>Passar estruturas TOUCHINPUT para o processador apropriado

Depois que os dados são extraídos das mensagens WM_TOUCH usando [**a**](wm-touchdown.md) função [**GetTouchInputInfo,**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) alimente os dados no processador de manipulação invocando as funções [**ProcessUpWithTime,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime) [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)ou [**ProcessMoveWithTime,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) dependendo do **dwFlag definido** na estrutura [**TOUCHINPUT.**](/windows/win32/api/winuser/ns-winuser-touchinput)

> [!Note]  
> Ao dar suporte a várias manipulações, um novo processador de manipulação deverá ser criado se **o dwID** definido na estrutura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) deve ser usado para enviar os dados para o objeto [**IManipulationProcessor correto.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)

```C++
CoreObject* coCurrent = m_coHead;

while(coCurrent!=NULL && !bFoundObj)
{
    if(dwEvent & TOUCHEVENTF_DOWN)
    {
        DownEvent(coCurrent, inData, &bFoundObj);
    }
    else if(dwEvent & TOUCHEVENTF_MOVE)
    {
        MoveEvent(coCurrent, inData);
    }
    else if(dwEvent & TOUCHEVENTF_UP)
    {
        UpEvent(coCurrent, inData);
    }
    coCurrent = coCurrent->coNext;
}

VOID CComTouchDriver::DownEvent(CoreObject* coRef, tagTOUCHINPUT inData, BOOL* bFound) {
    DWORD dwPCursor = inData.dwID;
    DWORD dwPTime   = inData.dwTime;
    int x           = inData.x;
    int y           = inData.y;

    // Check that the user has touched within an object's region and fed to the object's manipulation processor.

    if(coRef->doDrawing->InRegion(x, y) &&
        !HasCursor(coRef, dwPCursor))
    {
        ...

        // Feed values to the Manipulation Processor.
        coRef->manipulationProc->ProcessDownWithTime(dwPCursor, (FLOAT)x, (FLOAT)y, dwPTime);

        ...
    }
}
```

## <a name="set-up-inertia-within-manipulationcompleted"></a>Configurar inércia em ManipulationCompleted

Depois que o método [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) for invocado, o objeto [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) deverá definir os valores para o objeto [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) vinculado ao **IManipulationProcessor** para invocar a inércia. O exemplo de código a seguir mostra como configurar o objeto **IInertiaProcessor** do método **IManipulationProcessor** **ManipulationCompleted.**

```C++
    int iVWidth       = GetSystemMetrics(SM_CXVIRTUALSCREEN);
    int iVHeight      = GetSystemMetrics(SM_CYVIRTUALSCREEN);

    RECT rc;
    GetClientRect(m_hWnd, &rc);
    FLOAT lCWidth     = (FLOAT)rc.right;
    FLOAT lCHeight    = (FLOAT)rc.bottom;

    // Set properties for inertia events.

    // Deceleration for tranlations in pixel / msec^2.
    m_inert->put_DesiredDeceleration(0.001f);

    // Deceleration for rotations in radians / msec^2.
    m_inert->put_DesiredAngularDeceleration(0.00001f);

    // Calculate borders and elastic margin to be set.
    // They are relative to the width and height of the object.

    FLOAT fHOffset = m_dObj->GetWidth()  * 0.5f;
    FLOAT fVOffset = m_dObj->GetHeight() * 0.5f;

    // Elastic margin is in pixels - note that it offsets the boundary.

    FLOAT fHElasticMargin = 25.0f;
    FLOAT fVElasticMargin = 25.0f;

    FLOAT fBoundaryLeft   = fHOffset + fHElasticMargin;
    FLOAT fBoundaryTop    = fVOffset + fVElasticMargin;
    FLOAT fBoundaryRight  = lCWidth - fHOffset - fHElasticMargin;
    FLOAT fBoundaryBottom = lCHeight - fVOffset - fVElasticMargin;

    // Set borders and elastic margin.

    m_inert->put_BoundaryLeft(fBoundaryLeft);
    m_inert->put_BoundaryTop(fBoundaryTop);
    m_inert->put_BoundaryRight(fBoundaryRight);
    m_inert->put_BoundaryBottom(fBoundaryBottom);

    m_inert->put_ElasticMarginLeft(fHElasticMargin);
    m_inert->put_ElasticMarginTop(fVElasticMargin);
    m_inert->put_ElasticMarginRight(fHElasticMargin);
    m_inert->put_ElasticMarginBottom(fVElasticMargin);

    // Set initial origins.

    m_inert->put_InitialOriginX(m_dObj->GetCenterX());
    m_inert->put_InitialOriginY(m_dObj->GetCenterY());

    FLOAT fVX;
    FLOAT fVY;
    FLOAT fVR;

    m_manip->GetVelocityX(&fVX);
    m_manip->GetVelocityY(&fVY);
    m_manip->GetAngularVelocity(&fVR);

    // Set initial velocities for inertia processor.

    m_inert->put_InitialVelocityX(fVX);
    m_inert->put_InitialVelocityY(fVY);
    m_inert->put_InitialAngularVelocity(fVR);
```

## <a name="clean-up-your-com-objects"></a>Limpar seus objetos COM

Quando o aplicativo for fechado, você deverá limpar seus objetos COM. O código a seguir mostra como você pode liberar os recursos que foram alocados no exemplo.

```C++
CComTouchDriver::~CComTouchDriver(VOID) {
    CoreObject* coCurrent = m_coHead;

    // Clean up COM objects.

    while(coCurrent!=NULL)
    {
        coCurrent->inertiaEventSink->Release();
        coCurrent->manipulationEventSink->Release();
        coCurrent->inertiaProc->Release();
        coCurrent->manipulationProc->Release();
        coCurrent = coCurrent->coNext;
    }
}
```

## <a name="related-topics"></a>Tópicos relacionados

[Aplicativo de manipulação de vários](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp) [toques, amostra de manipulação e inércia,](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp) [Windows de toque](windows-touch-samples.md)