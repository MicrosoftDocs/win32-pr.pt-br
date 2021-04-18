---
description: Como reproduzir arquivos que contêm mídia protegida por DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Como reproduzir arquivos de mídia protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105760633"
---
# <a name="how-to-play-protected-media-files"></a><span data-ttu-id="7fc58-103">Como reproduzir arquivos de mídia protegidos</span><span class="sxs-lookup"><span data-stu-id="7fc58-103">How to Play Protected Media Files</span></span>

<span data-ttu-id="7fc58-104">Um arquivo de mídia protegido é qualquer arquivo de mídia que tenha regras associadas para usar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-104">A protected media file is any media file that has associated rules for using the content.</span></span> <span data-ttu-id="7fc58-105">Em alguns casos, um arquivo de mídia protegido é criptografado usando alguma forma de criptografia DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="7fc58-105">In some cases, a protected media file is encrypted using some form of digital rights management (DRM) encryption.</span></span> <span data-ttu-id="7fc58-106">Para reproduzir um arquivo de mídia protegido, a reprodução deve ocorrer dentro do caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="7fc58-106">To play a protected media file, playback must occur inside the protected media path (PMP).</span></span> <span data-ttu-id="7fc58-107">Além disso, o usuário pode precisar adquirir direitos para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-107">In addition, the user might have to acquire rights to the content.</span></span>

<span data-ttu-id="7fc58-108">O termo aquisição de direitos refere-se a qualquer ação que o aplicativo deve executar antes que o usuário possa reproduzir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-108">The term rights acquisition refers to any action that the application must perform before the user can play the content.</span></span> <span data-ttu-id="7fc58-109">O exemplo mais comum é obter uma licença de DRM, mas Media Foundation define um mecanismo genérico que pode dar suporte a outros tipos de aquisição de direitos.</span><span class="sxs-lookup"><span data-stu-id="7fc58-109">The most common example is obtaining a DRM license, but Media Foundation defines a generic mechanism that can support other types of rights acquisition.</span></span> <span data-ttu-id="7fc58-110">A interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) define esse mecanismo genérico.</span><span class="sxs-lookup"><span data-stu-id="7fc58-110">The [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface defines this generic mechanism.</span></span>

<span data-ttu-id="7fc58-111">A aquisição de direitos deve ser feita fora do PMP, a partir do processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-111">Rights acquisition must be done outside of the PMP, from the application process.</span></span> <span data-ttu-id="7fc58-112">A sessão de mídia notifica o aplicativo por meio da interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , que é implementada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-112">The Media Session notifies the application through the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface, which is implemented by the application.</span></span> <span data-ttu-id="7fc58-113">A sessão de mídia usa a interface **IMFContentProtectionManager** para encaminhar um objeto de habilitador de conteúdo para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-113">The Media Session uses the **IMFContentProtectionManager** interface to forward a content enabler object to the application.</span></span> <span data-ttu-id="7fc58-114">Os ativadores de conteúdo implementam a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="7fc58-114">Content enablers implement the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="7fc58-115">O aplicativo usa essa interface para adquirir os direitos necessários.</span><span class="sxs-lookup"><span data-stu-id="7fc58-115">The application uses this interface to acquire the necessary rights.</span></span>

<span data-ttu-id="7fc58-116">Um ativador de conteúdo pode dar suporte à aquisição automática de direitos, caso em que o ativador de conteúdo implementa todo o processo, e o aplicativo simplesmente monitora o status.</span><span class="sxs-lookup"><span data-stu-id="7fc58-116">A content enabler might support automatic rights acquisition, in which case the content enabler implements the entire process, and the application simply monitors the status.</span></span> <span data-ttu-id="7fc58-117">Caso contrário, o aplicativo deve usar a aquisição de direitos não silenciosa, que é um processo em que o aplicativo envia dados HTTP POST para uma URL fornecida pelo habilitador de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-117">Otherwise, the application must use non-silent rights acquisition, which is a process where the application sends HTTP POST data to a URL provided by the content enabler.</span></span>

<span data-ttu-id="7fc58-118">Para reproduzir mídia protegida, um aplicativo segue as mesmas etapas fornecidas no tópico [como reproduzir arquivos de mídia com o Media Foundation](how-to-play-unprotected-media-files.md), com as seguintes etapas adicionais:</span><span class="sxs-lookup"><span data-stu-id="7fc58-118">To play protected media, an application follows the same steps given in the topic [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), with the following additional steps:</span></span>

1.  <span data-ttu-id="7fc58-119">Consulte se a origem da mídia contém conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="7fc58-119">Query whether the media source contains protected content.</span></span> <span data-ttu-id="7fc58-120">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="7fc58-120">(Optional.)</span></span>
2.  <span data-ttu-id="7fc58-121">Crie a sessão de mídia no processo do PMP, em vez do processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-121">Create the Media Session in the PMP process, instead of the application process.</span></span>
3.  <span data-ttu-id="7fc58-122">Execute a aquisição de direitos, se notificado para fazer isso pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="7fc58-122">Perform rights acquisition, if notified to do so by the Media Session.</span></span> <span data-ttu-id="7fc58-123">Esta operação é executada de forma assíncrona pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-123">This operation is performed asynchronously by the application.</span></span>
4.  <span data-ttu-id="7fc58-124">Conclua a operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7fc58-124">Complete the asynchronous operation.</span></span>

## <a name="query-for-protected-content"></a><span data-ttu-id="7fc58-125">Consulta de conteúdo protegido</span><span class="sxs-lookup"><span data-stu-id="7fc58-125">Query for Protected Content</span></span>

<span data-ttu-id="7fc58-126">Para consultar se uma fonte de mídia contém conteúdo protegido, chame a função [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) no descritor de apresentação da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="7fc58-126">To query whether a media source contains protected content, call the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function on the media source's presentation descriptor.</span></span> <span data-ttu-id="7fc58-127">Se a função retornar S \_ OK, você deverá usar o PMP para reproduzir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-127">If the function returns S\_OK, you must use the PMP to play the content.</span></span> <span data-ttu-id="7fc58-128">Se a função retornar S \_ false, a PMP não será necessária e você poderá criar a sessão de mídia no processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-128">If the function returns S\_FALSE, the PMP is not required, and you can create the Media Session in the application process.</span></span> <span data-ttu-id="7fc58-129">Como alternativa, você pode usar o PMP para reproduzir os dois tipos de conteúdo, protegidos e desprotegidos.</span><span class="sxs-lookup"><span data-stu-id="7fc58-129">Alternatively, you can use the PMP to play both types of content, protected and unprotected.</span></span> <span data-ttu-id="7fc58-130">Se você fizer isso, não precisará chamar **MFRequireProtectedEnvironment**.</span><span class="sxs-lookup"><span data-stu-id="7fc58-130">If you do that, you do not need to call **MFRequireProtectedEnvironment**.</span></span>

<span data-ttu-id="7fc58-131">Para obter mais informações sobre descritores de apresentação, consulte [descritores de apresentação](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="7fc58-131">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

## <a name="create-the-pmp-media-session"></a><span data-ttu-id="7fc58-132">Criar a sessão de mídia do PMP</span><span class="sxs-lookup"><span data-stu-id="7fc58-132">Create the PMP Media Session</span></span>

<span data-ttu-id="7fc58-133">Para criar a sessão de mídia no PMP, chame [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="7fc58-133">To create the Media Session in the PMP, call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="7fc58-134">Essa função é semelhante a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), mas em vez de criar a sessão de mídia no processo do aplicativo, ela cria a sessão de mídia no processo do PMP.</span><span class="sxs-lookup"><span data-stu-id="7fc58-134">This function is similar to [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), but instead of creating the Media Session in the application's process, it creates the Media Session in the PMP process.</span></span> <span data-ttu-id="7fc58-135">O aplicativo recebe um ponteiro para um objeto proxy para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="7fc58-135">The application receives a pointer to a proxy object for the Media Session.</span></span> <span data-ttu-id="7fc58-136">O aplicativo chama métodos [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) no objeto proxy, assim como faria na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="7fc58-136">The application calls [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods on the proxy object, just as it would on the Media Session.</span></span> <span data-ttu-id="7fc58-137">O objeto proxy encaminha as chamadas para a sessão de mídia entre o limite do processo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-137">The proxy object forwards the calls to the Media Session across the process boundary.</span></span>

<span data-ttu-id="7fc58-138">Crie a sessão de mídia do PMP da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7fc58-138">Create the PMP Media Session as follows:</span></span>

1.  <span data-ttu-id="7fc58-139">Crie um novo repositório de atributos chamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="7fc58-139">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="7fc58-140">Defina o [**atributo \_ \_ Gerenciador de \_ proteção \_ de conteúdo da sessão MF**](mf-session-content-protection-manager-attribute.md) no repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="7fc58-140">Set the [**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**](mf-session-content-protection-manager-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="7fc58-141">O valor desse atributo é um ponteiro para a implementação do seu aplicativo de [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span><span class="sxs-lookup"><span data-stu-id="7fc58-141">The value of this attribute is a pointer to your application's implementation of [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span></span> <span data-ttu-id="7fc58-142">Chame [**IMFAttributes:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) para definir o atributo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-142">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the attribute.</span></span>
3.  <span data-ttu-id="7fc58-143">Chame [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para criar a sessão de mídia no processo do PMP.</span><span class="sxs-lookup"><span data-stu-id="7fc58-143">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session in the PMP process.</span></span> <span data-ttu-id="7fc58-144">O parâmetro *pConfiguration* é um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) do repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="7fc58-144">The *pConfiguration* parameter is a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the attribute store.</span></span>


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



<span data-ttu-id="7fc58-145">Em seguida, crie uma topologia de reprodução e a enfileirará na sessão de mídia, conforme descrito em [criando topologias de reprodução](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="7fc58-145">Next, create a playback topology and queue it on the Media Session, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

## <a name="perform-rights-acquisition"></a><span data-ttu-id="7fc58-146">Executar aquisição de direitos</span><span class="sxs-lookup"><span data-stu-id="7fc58-146">Perform Rights Acquisition</span></span>

<span data-ttu-id="7fc58-147">Se a reprodução exigir a aquisição de direitos, a sessão de mídia chamará [**IMFContentProtectionManager:: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="7fc58-147">If playback requires rights acquisition, the Media Session calls [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="7fc58-148">O parâmetro *pEnablerActivate* desse método é um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="7fc58-148">The *pEnablerActivate* parameter of this method is a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="7fc58-149">Use essa interface para criar o objeto de habilitação de conteúdo, que expõe a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="7fc58-149">Use this interface to create the content enabler object, which exposes the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="7fc58-150">Em seguida, use o habilitador de conteúdo para executar a etapa de aquisição de direitos.</span><span class="sxs-lookup"><span data-stu-id="7fc58-150">Then use the content enabler to perform the rights acquisition step.</span></span>

<span data-ttu-id="7fc58-151">Para criar o ativador de conteúdo, chame [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span><span class="sxs-lookup"><span data-stu-id="7fc58-151">To create the content enabler, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span></span>


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



<span data-ttu-id="7fc58-152">Consulte o ponteiro [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) retornado para a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="7fc58-152">Query the returned [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pointer for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="7fc58-153">Use esta interface para obter eventos do objeto de habilitador de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-153">Use this interface to get events from the content enabler object.</span></span> <span data-ttu-id="7fc58-154">Para obter mais informações sobre eventos, consulte [geradores de eventos de mídia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="7fc58-154">For more information about events, see [Media Event Generators](media-event-generators.md).</span></span>

<span data-ttu-id="7fc58-155">Para descobrir se o ativador de conteúdo dá suporte à aquisição automática, chame [**IMFContentEnabler:: IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span><span class="sxs-lookup"><span data-stu-id="7fc58-155">To find out whether the content enabler supports automatic acquisition, call [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span></span> <span data-ttu-id="7fc58-156">Se esse método retornar o valor **true**, o aplicativo deverá usar a aquisição automática.</span><span class="sxs-lookup"><span data-stu-id="7fc58-156">If this method returns the value **TRUE**, the application should use automatic acquisition.</span></span> <span data-ttu-id="7fc58-157">Caso contrário, use a aquisição não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="7fc58-157">Otherwise, use non-silent acquisition.</span></span>

<span data-ttu-id="7fc58-158">O método [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) é assíncrono.</span><span class="sxs-lookup"><span data-stu-id="7fc58-158">The [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method is asynchronous.</span></span> <span data-ttu-id="7fc58-159">O aplicativo deve executar a etapa de aquisição no thread do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-159">The application should perform the acquisition step on the application's thread.</span></span> <span data-ttu-id="7fc58-160">Uma abordagem é postar uma mensagem de janela privada na janela principal do aplicativo, notificando o thread do aplicativo para executar a aquisição.</span><span class="sxs-lookup"><span data-stu-id="7fc58-160">One approach is to post a private window message to the application's main window, notifying the application thread to perform the acquisition.</span></span> <span data-ttu-id="7fc58-161">Enquanto a operação está pendente, o aplicativo deve armazenar o ponteiro de retorno de chamada e o objeto de estado que ele recebeu nos parâmetros *pCallback* e *punkState* de **BeginEnableContent**.</span><span class="sxs-lookup"><span data-stu-id="7fc58-161">While the operation is pending, the application must store the callback pointer and the state object that it received in the *pCallback* and *punkState* parameters of **BeginEnableContent**.</span></span> <span data-ttu-id="7fc58-162">Eles serão usados para concluir a operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7fc58-162">These will be used to complete the asynchronous operation.</span></span>

### <a name="automatic-acquisition"></a><span data-ttu-id="7fc58-163">Aquisição automática</span><span class="sxs-lookup"><span data-stu-id="7fc58-163">Automatic Acquisition</span></span>

<span data-ttu-id="7fc58-164">Para executar a aquisição automática, chame [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span><span class="sxs-lookup"><span data-stu-id="7fc58-164">To perform automatic acquisition, call [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span></span> <span data-ttu-id="7fc58-165">Esse método é assíncrono.</span><span class="sxs-lookup"><span data-stu-id="7fc58-165">This method is asynchronous.</span></span> <span data-ttu-id="7fc58-166">Quando a operação é concluída, o ativador de conteúdo envia um evento [MEEnablerCompleted](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc58-166">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span> <span data-ttu-id="7fc58-167">O código de status do evento indica se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7fc58-167">The event's status code indicates whether the operation was successful.</span></span> <span data-ttu-id="7fc58-168">Se o código de status do evento MEEnablerCompleted for a \_ licença NS e \_ DRM \_ \_ não adquirida, o aplicativo deverá tentar usar a aquisição não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="7fc58-168">If the status code from the MEEnablerCompleted event is NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should try using non-silent acquisition.</span></span>

<span data-ttu-id="7fc58-169">Enquanto a operação de aquisição está em andamento, o objeto habilitador pode enviar o evento [MEEnablerProgress](meenablerprogress.md) para indicar o progresso da operação.</span><span class="sxs-lookup"><span data-stu-id="7fc58-169">While the acquisition operation is in progress, the enabler object might send the [MEEnablerProgress](meenablerprogress.md) event to indicate the progress of the operation.</span></span> <span data-ttu-id="7fc58-170">Para cancelar a operação, chame [**IMFContentEnabler:: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span><span class="sxs-lookup"><span data-stu-id="7fc58-170">To cancel the operation, call [**IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span></span>

### <a name="non-silent-acquisition"></a><span data-ttu-id="7fc58-171">Aquisição não silenciosa</span><span class="sxs-lookup"><span data-stu-id="7fc58-171">Non-Silent Acquisition</span></span>

<span data-ttu-id="7fc58-172">Se o método [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) retornar **false** ou o método [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) falhar com o código de erro licença do NS \_ E \_ DRM \_ \_ não adquirido, o aplicativo deverá executar uma aquisição não silenciosa, conforme descrito nas etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="7fc58-172">If the [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) method returns **FALSE** or the [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method fails with the error code NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should perform non-silent acquisition as described in the following steps:</span></span>

1.  <span data-ttu-id="7fc58-173">Chame [**IMFContentEnabler:: GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) para obter a URL para a aquisição de direitos.</span><span class="sxs-lookup"><span data-stu-id="7fc58-173">Call [**IMFContentEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) to get the URL for the rights acquisition.</span></span> <span data-ttu-id="7fc58-174">Esse método também retorna um sinalizador que indica se a URL é confiável.</span><span class="sxs-lookup"><span data-stu-id="7fc58-174">This method also returns a flag indicating whether the URL is trusted.</span></span>
2.  <span data-ttu-id="7fc58-175">Chame [**IMFContentEnabler:: GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) para obter os dados http post.</span><span class="sxs-lookup"><span data-stu-id="7fc58-175">Call [**IMFContentEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) to get the HTTP POST data.</span></span>
3.  <span data-ttu-id="7fc58-176">Chame [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span><span class="sxs-lookup"><span data-stu-id="7fc58-176">Call [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span></span> <span data-ttu-id="7fc58-177">Esse método faz com que o habilitador de conteúdo monitore o progresso da ação de aquisição de direitos.</span><span class="sxs-lookup"><span data-stu-id="7fc58-177">This method causes the content enabler to monitor the progress of the rights acquisition action.</span></span>

4.  <span data-ttu-id="7fc58-178">Envie os dados para a URL de aquisição de direitos usando uma ação HTTP POST.</span><span class="sxs-lookup"><span data-stu-id="7fc58-178">Submit the data to the rights acquisition URL by using an HTTP POST action.</span></span> <span data-ttu-id="7fc58-179">Você pode usar o controle do Internet Explorer ou as APIs do Windows Internet (WinINet).</span><span class="sxs-lookup"><span data-stu-id="7fc58-179">You can use the Internet Explorer control or the Windows Internet (WinINet) APIs.</span></span>

<span data-ttu-id="7fc58-180">O código a seguir mostra as etapas 1 a 3.</span><span class="sxs-lookup"><span data-stu-id="7fc58-180">The following code shows steps 1–3.</span></span> <span data-ttu-id="7fc58-181">A etapa 4 depende dos requisitos específicos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc58-181">Step 4 depends on your application's particular requirements.</span></span>


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



<span data-ttu-id="7fc58-182">Quando a operação é concluída, o ativador de conteúdo envia um evento [MEEnablerCompleted](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc58-182">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span>

## <a name="complete-the-asynchronous-operation"></a><span data-ttu-id="7fc58-183">Concluir a operação assíncrona</span><span class="sxs-lookup"><span data-stu-id="7fc58-183">Complete the Asynchronous Operation</span></span>

<span data-ttu-id="7fc58-184">Quando a aquisição de direitos é concluída, com êxito ou não, o aplicativo deve notificar a sessão de mídia, invocando o ponteiro de retorno de chamada fornecido no método [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="7fc58-184">When the rights acquisition is completed, successfully or otherwise, the application must notify the Media Session, by invoking the callback pointer given in the [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

1.  <span data-ttu-id="7fc58-185">Crie um objeto de resultado assíncrono chamando [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span><span class="sxs-lookup"><span data-stu-id="7fc58-185">Create an asynchronous result object by calling [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span></span>
2.  <span data-ttu-id="7fc58-186">Invoque o retorno de chamada da sessão de mídia chamando [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="7fc58-186">Invoke the Media Session's callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>
3.  <span data-ttu-id="7fc58-187">A sessão de mídia chamará [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span><span class="sxs-lookup"><span data-stu-id="7fc58-187">The Media Session will call [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span></span> <span data-ttu-id="7fc58-188">Na implementação desse método, libere os ponteiros ou recursos que você alocou dentro de [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="7fc58-188">In your implementation of this method, release any pointers or resources that you allocated inside [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="7fc58-189">Retornar um **HRESULT** que indica o êxito geral da operação.</span><span class="sxs-lookup"><span data-stu-id="7fc58-189">Return an **HRESULT** that indicates the overall success of the operation.</span></span> <span data-ttu-id="7fc58-190">Se a aquisição de direitos tiver falhado ou o usuário tiver cancelado antes de ser concluído, retorne um código de erro.</span><span class="sxs-lookup"><span data-stu-id="7fc58-190">If the rights acquisition failed or the user canceled before it was completed, return an error code.</span></span>

<span data-ttu-id="7fc58-191">O código a seguir mostra como criar o resultado assíncrono e invocar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7fc58-191">The following code shows how to create the asynchronous result and invoke the callback.</span></span>


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a><span data-ttu-id="7fc58-192">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fc58-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fc58-193">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="7fc58-193">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="7fc58-194">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="7fc58-194">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



