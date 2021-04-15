---
title: Manipulação e exemplo de inércia
description: O exemplo de manipulação e inércia mostra como adicionar suporte ao Windows Touch a aplicativos nativos baseados no Windows que usam a API de toque do Windows.
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows Touch, exemplos de código
- Windows Touch, código de exemplo
- Windows Touch, manipulações
- Windows Touch, inércia
- Exemplo de toque, manipulação e inércia do Windows
- Manipulação e exemplo de inércia
- Windows Touch, interface _IManipulationEventSink
- Windows Touch, interface IManipulationProcessor
- Windows Touch, interface IInertiaProcessor
- manipulações, código de exemplo
- manipulações, exemplos de código
- manipulações, _IManipulationEventSink interface
- manipulações, interface IManipulationProcessor
- inércia, código de exemplo
- inércia, exemplos de código
- inércia, interface IInertiaProcessor
- Interface _IManipulationEventSink
- Interface IManipulationProcessor, exemplos de código
- Interface IManipulationProcessor, código de exemplo
- Interface IInertiaProcessor, exemplos de código
- Interface IInertiaProcessor, código de exemplo
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: a17b634fbe79d72e79fc5c9e03ef64a30cb46411
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104554707"
---
# <a name="manipulation-and-inertia-sample"></a><span data-ttu-id="1e02e-124">Manipulação e exemplo de inércia</span><span class="sxs-lookup"><span data-stu-id="1e02e-124">Manipulation and Inertia Sample</span></span>

<span data-ttu-id="1e02e-125">O exemplo de manipulação e inércia mostra como adicionar suporte ao Windows Touch a aplicativos nativos baseados no Windows que usam a API de toque do Windows.</span><span class="sxs-lookup"><span data-stu-id="1e02e-125">The Manipulation and Inertia sample shows how to add Windows Touch support to native Windows-based applications that use the Windows Touch API.</span></span> <span data-ttu-id="1e02e-126">O exemplo implementa os recursos básicos da API para habilitar a conversão, a rotação e o dimensionamento de objetos e a aplicação de propriedades inércia a eles.</span><span class="sxs-lookup"><span data-stu-id="1e02e-126">The sample implements the basic features of the API to enable translation, rotation, and scaling for objects and applying inertia properties to them.</span></span> <span data-ttu-id="1e02e-127">O exemplo também mostra como dar suporte ao mouse básico para Windows Touch Applications.</span><span class="sxs-lookup"><span data-stu-id="1e02e-127">The sample also shows how to give your Windows Touch applications basic mouse support.</span></span> <span data-ttu-id="1e02e-128">A imagem a seguir mostra como a amostra é exibida quando é executada.</span><span class="sxs-lookup"><span data-stu-id="1e02e-128">The following image shows how the sample looks when it runs.</span></span>

![captura de tela que mostra duas caixas com gradientes no exemplo de manipulação e inércia](images/manip-inertia-sample.png)

<span data-ttu-id="1e02e-130">As caixas com gradientes podem ser manipuladas de forma independente por um usuário quando executam o aplicativo de um computador que dá suporte ao Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="1e02e-130">The boxes with gradients can be manipulated independently by a user when they run the application from a computer that supports Windows Touch.</span></span>

## <a name="register-the-touch-window"></a><span data-ttu-id="1e02e-131">Registrar a janela de toque</span><span class="sxs-lookup"><span data-stu-id="1e02e-131">Register the Touch Window</span></span>

<span data-ttu-id="1e02e-132">Antes de receber a entrada por toque, primeiro você deve notificar o sistema de que seu aplicativo é um aplicativo do Windows Touch chamando a seguinte função:</span><span class="sxs-lookup"><span data-stu-id="1e02e-132">Before you can receive touch input, you first must notify the system that your application is a Windows Touch application by calling the following function:</span></span>

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a><span data-ttu-id="1e02e-133">Implementar a interface _IManipulationEventSink</span><span class="sxs-lookup"><span data-stu-id="1e02e-133">Implement the _IManipulationEventSink Interface</span></span>

<span data-ttu-id="1e02e-134">O coletor de eventos [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) contém três funções: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted).</span><span class="sxs-lookup"><span data-stu-id="1e02e-134">The [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) event sink contains three functions: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted).</span></span> <span data-ttu-id="1e02e-135">Essas funções de retorno de chamada são usadas pela interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e pela interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para retornar os valores calculados pelos processadores depois que eles chamam as funções [**processtime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)e [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) .</span><span class="sxs-lookup"><span data-stu-id="1e02e-135">These callback functions are used by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface and [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for returning the values calculated by the processors after they invoke the [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime), and [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) functions.</span></span> <span data-ttu-id="1e02e-136">O exemplo de código a seguir mostra uma implementação de exemplo de uma interface **_IManipulationEvents** .</span><span class="sxs-lookup"><span data-stu-id="1e02e-136">The following code example shows an example implementation of a **_IManipulationEvents** interface.</span></span>

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

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a><span data-ttu-id="1e02e-137">Criar objetos COM e configurar as interfaces IManipulationProcessor e IInertiaProcessor</span><span class="sxs-lookup"><span data-stu-id="1e02e-137">Create COM Objects and Set up the IManipulationProcessor and IInertiaProcessor Interfaces</span></span>

<span data-ttu-id="1e02e-138">A API fornece uma implementação das interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="1e02e-138">The API provides an implementation of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) and [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span> <span data-ttu-id="1e02e-139">Você deve criar uma instância do e fazer referência aos objetos COM do coletor de eventos [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) que foi implementado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1e02e-139">You should create an instance of and reference the COM objects from the [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) event sink that was implemented earlier.</span></span>

## <a name="handle-wm_touch-messages"></a><span data-ttu-id="1e02e-140">Manipular WM_TOUCH mensagens</span><span class="sxs-lookup"><span data-stu-id="1e02e-140">Handle WM_TOUCH Messages</span></span>

<span data-ttu-id="1e02e-141">Os dados de entrada devem ser extraídos do [**WM_TOUCH**](wm-touchdown.md) mensagens e, posteriormente, devem ser processados para alimentar o processador de manipulação correto.</span><span class="sxs-lookup"><span data-stu-id="1e02e-141">The input data must be extracted from the [**WM_TOUCH**](wm-touchdown.md) messages and then later must be processed to feed the correct manipulation processor.</span></span>

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
> <span data-ttu-id="1e02e-142">Para usar a função [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , você deve ter suporte a DPI alto em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1e02e-142">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="1e02e-143">Para obter mais informações sobre como dar suporte a DPI alto, visite a seção [alta dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) do MSDN.</span><span class="sxs-lookup"><span data-stu-id="1e02e-143">For more information about supporting high DPI, visit the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a><span data-ttu-id="1e02e-144">Passe as estruturas TOUCHINPUT para o processador apropriado</span><span class="sxs-lookup"><span data-stu-id="1e02e-144">Pass TOUCHINPUT Structures to the Appropriate Processor</span></span>

<span data-ttu-id="1e02e-145">Depois que os dados são extraídos [**do WM_TOUCH**](wm-touchdown.md) mensagens usando a [**função GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) , alimentar os dados no processador de manipulação invocando as [**funções ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)ou [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) , dependendo do **dwFlag** definido na estrutura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) .</span><span class="sxs-lookup"><span data-stu-id="1e02e-145">After the data is extracted from the [**WM_TOUCH**](wm-touchdown.md) messages by using the [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) function, feed the data into the manipulation processor by invoking [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime), or [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) functions, depending on the **dwFlag** set in the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure.</span></span>

> [!Note]  
> <span data-ttu-id="1e02e-146">Ao dar suporte a várias manipulações, um novo processador de manipulação deve ser criado se o **dwID** definido na estrutura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) deve ser usado para enviar os dados para o objeto [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) correto.</span><span class="sxs-lookup"><span data-stu-id="1e02e-146">When supporting multiple manipulations, a new manipulation processor must be created if the **dwID** defined in the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure must be used to send the data to the correct [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) object.</span></span>

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

## <a name="set-up-inertia-within-manipulationcompleted"></a><span data-ttu-id="1e02e-147">Configurar inércia em ManipulationCompleted</span><span class="sxs-lookup"><span data-stu-id="1e02e-147">Set up Inertia within ManipulationCompleted</span></span>

<span data-ttu-id="1e02e-148">Depois que o método [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) é invocado, o objeto [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) deve definir os valores para o objeto [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) vinculado ao **IManipulationProcessor** para invocar inércia.</span><span class="sxs-lookup"><span data-stu-id="1e02e-148">After the [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) method is invoked, the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) object must set the values for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) object linked to the **IManipulationProcessor** to invoke inertia.</span></span> <span data-ttu-id="1e02e-149">O exemplo de código a seguir mostra como configurar o objeto **IInertiaProcessor** do método **IManipulationProcessor** **ManipulationCompleted**.</span><span class="sxs-lookup"><span data-stu-id="1e02e-149">The following code example shows how to set up the **IInertiaProcessor** object from the **IManipulationProcessor** method **ManipulationCompleted**.</span></span>

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

## <a name="clean-up-your-com-objects"></a><span data-ttu-id="1e02e-150">Limpar seus objetos COM</span><span class="sxs-lookup"><span data-stu-id="1e02e-150">Clean up your COM Objects</span></span>

<span data-ttu-id="1e02e-151">Quando seu aplicativo for fechado, você deverá limpar seus objetos COM.</span><span class="sxs-lookup"><span data-stu-id="1e02e-151">When your application closes, you must clean up your COM objects.</span></span> <span data-ttu-id="1e02e-152">O código a seguir mostra como você pode liberar os recursos que foram alocados no exemplo.</span><span class="sxs-lookup"><span data-stu-id="1e02e-152">The following code shows how you can free the resources that were allocated in the sample.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1e02e-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e02e-153">Related topics</span></span>

<span data-ttu-id="1e02e-154">[Aplicativo de manipulação multitoque](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [manipulação e exemplo de inércia](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [exemplos de toque do Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="1e02e-154">[Multi-touch Manipulation Application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [Manipulation and Inertia Sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>