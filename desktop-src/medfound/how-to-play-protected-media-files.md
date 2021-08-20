---
description: Como reproduzir arquivos que contêm mídia protegida por DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Como reproduzir arquivos de mídia protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20a2b525f8acc3a602bcaae2630726d01269881beec07ac214f4d0bd02ee1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942336"
---
# <a name="how-to-play-protected-media-files"></a>Como reproduzir arquivos de mídia protegidos

Um arquivo de mídia protegido é qualquer arquivo de mídia que tenha regras associadas para usar o conteúdo. Em alguns casos, um arquivo de mídia protegido é criptografado usando alguma forma de criptografia DRM (gerenciamento de direitos digitais). Para reproduzir um arquivo de mídia protegido, a reprodução deve ocorrer dentro do caminho de mídia protegido (PMP). Além disso, o usuário pode precisar adquirir direitos para o conteúdo.

O termo aquisição de direitos refere-se a qualquer ação que o aplicativo deve executar antes que o usuário possa reproduzir o conteúdo. O exemplo mais comum é obter uma licença de DRM, mas Media Foundation define um mecanismo genérico que pode dar suporte a outros tipos de aquisição de direitos. A interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) define esse mecanismo genérico.

A aquisição de direitos deve ser feita fora do PMP, a partir do processo do aplicativo. A sessão de mídia notifica o aplicativo por meio da interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , que é implementada pelo aplicativo. A sessão de mídia usa a interface **IMFContentProtectionManager** para encaminhar um objeto de habilitador de conteúdo para o aplicativo. Os ativadores de conteúdo implementam a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . O aplicativo usa essa interface para adquirir os direitos necessários.

Um ativador de conteúdo pode dar suporte à aquisição automática de direitos, caso em que o ativador de conteúdo implementa todo o processo, e o aplicativo simplesmente monitora o status. Caso contrário, o aplicativo deve usar a aquisição de direitos não silenciosa, que é um processo em que o aplicativo envia dados HTTP POST para uma URL fornecida pelo habilitador de conteúdo.

Para reproduzir mídia protegida, um aplicativo segue as mesmas etapas fornecidas no tópico [como reproduzir arquivos de mídia com o Media Foundation](how-to-play-unprotected-media-files.md), com as seguintes etapas adicionais:

1.  Consulte se a origem da mídia contém conteúdo protegido. (Opcional).
2.  Crie a sessão de mídia no processo do PMP, em vez do processo do aplicativo.
3.  Execute a aquisição de direitos, se notificado para fazer isso pela sessão de mídia. Esta operação é executada de forma assíncrona pelo aplicativo.
4.  Conclua a operação assíncrona.

## <a name="query-for-protected-content"></a>Consulta de conteúdo protegido

Para consultar se uma fonte de mídia contém conteúdo protegido, chame a função [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) no descritor de apresentação da fonte de mídia. Se a função retornar S \_ OK, você deverá usar o PMP para reproduzir o conteúdo. Se a função retornar S \_ false, a PMP não será necessária e você poderá criar a sessão de mídia no processo do aplicativo. Como alternativa, você pode usar o PMP para reproduzir os dois tipos de conteúdo, protegidos e desprotegidos. Se você fizer isso, não precisará chamar **MFRequireProtectedEnvironment**.

Para obter mais informações sobre descritores de apresentação, consulte [descritores de apresentação](presentation-descriptors.md).

## <a name="create-the-pmp-media-session"></a>Criar a sessão de mídia do PMP

Para criar a sessão de mídia no PMP, chame [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Essa função é semelhante a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), mas em vez de criar a sessão de mídia no processo do aplicativo, ela cria a sessão de mídia no processo do PMP. O aplicativo recebe um ponteiro para um objeto proxy para a sessão de mídia. O aplicativo chama métodos [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) no objeto proxy, assim como faria na sessão de mídia. O objeto proxy encaminha as chamadas para a sessão de mídia entre o limite do processo.

Crie a sessão de mídia do PMP da seguinte maneira:

1.  Crie um novo repositório de atributos chamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Defina o [**atributo \_ \_ Gerenciador de \_ proteção \_ de conteúdo da sessão MF**](mf-session-content-protection-manager-attribute.md) no repositório de atributos. O valor desse atributo é um ponteiro para a implementação do seu aplicativo de [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager). Chame [**IMFAttributes:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) para definir o atributo.
3.  Chame [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para criar a sessão de mídia no processo do PMP. O parâmetro *pConfiguration* é um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) do repositório de atributos.


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



Em seguida, crie uma topologia de reprodução e a enfileirará na sessão de mídia, conforme descrito em [criando topologias de reprodução](creating-playback-topologies.md).

## <a name="perform-rights-acquisition"></a>Executar aquisição de direitos

Se a reprodução exigir a aquisição de direitos, a sessão de mídia chamará [**IMFContentProtectionManager:: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). O parâmetro *pEnablerActivate* desse método é um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Use essa interface para criar o objeto de habilitação de conteúdo, que expõe a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . Em seguida, use o habilitador de conteúdo para executar a etapa de aquisição de direitos.

Para criar o ativador de conteúdo, chame [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



Consulte o ponteiro [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) retornado para a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Use esta interface para obter eventos do objeto de habilitador de conteúdo. Para obter mais informações sobre eventos, consulte [geradores de eventos de mídia](media-event-generators.md).

Para descobrir se o ativador de conteúdo dá suporte à aquisição automática, chame [**IMFContentEnabler:: IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported). Se esse método retornar o valor **true**, o aplicativo deverá usar a aquisição automática. Caso contrário, use a aquisição não silenciosa.

O método [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) é assíncrono. O aplicativo deve executar a etapa de aquisição no thread do aplicativo. Uma abordagem é postar uma mensagem de janela privada na janela principal do aplicativo, notificando o thread do aplicativo para executar a aquisição. Enquanto a operação está pendente, o aplicativo deve armazenar o ponteiro de retorno de chamada e o objeto de estado que ele recebeu nos parâmetros *pCallback* e *punkState* de **BeginEnableContent**. Eles serão usados para concluir a operação assíncrona.

### <a name="automatic-acquisition"></a>Aquisição automática

Para executar a aquisição automática, chame [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable). Esse método é assíncrono. Quando a operação é concluída, o ativador de conteúdo envia um evento [MEEnablerCompleted](meenablercompleted.md) . O código de status do evento indica se a operação foi bem-sucedida. Se o código de status do evento MEEnablerCompleted for a \_ licença NS e \_ DRM \_ \_ não adquirida, o aplicativo deverá tentar usar a aquisição não silenciosa.

Enquanto a operação de aquisição está em andamento, o objeto habilitador pode enviar o evento [MEEnablerProgress](meenablerprogress.md) para indicar o progresso da operação. Para cancelar a operação, chame [**IMFContentEnabler:: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).

### <a name="non-silent-acquisition"></a>Aquisição não silenciosa

Se o método [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) retornar **false** ou o método [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) falhar com o código de erro licença do NS \_ E \_ DRM \_ \_ não adquirido, o aplicativo deverá executar uma aquisição não silenciosa, conforme descrito nas etapas a seguir:

1.  Chame [**IMFContentEnabler:: GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) para obter a URL para a aquisição de direitos. Esse método também retorna um sinalizador que indica se a URL é confiável.
2.  Chame [**IMFContentEnabler:: GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) para obter os dados http post.
3.  Chame [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable). Esse método faz com que o habilitador de conteúdo monitore o progresso da ação de aquisição de direitos.

4.  Envie os dados para a URL de aquisição de direitos usando uma ação HTTP POST. você pode usar o controle do internet Explorer ou as APIs do Windows internet (WinINet).

O código a seguir mostra as etapas 1 a 3. A etapa 4 depende dos requisitos específicos do seu aplicativo.


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



Quando a operação é concluída, o ativador de conteúdo envia um evento [MEEnablerCompleted](meenablercompleted.md) .

## <a name="complete-the-asynchronous-operation"></a>Concluir a operação assíncrona

Quando a aquisição de direitos é concluída, com êxito ou não, o aplicativo deve notificar a sessão de mídia, invocando o ponteiro de retorno de chamada fornecido no método [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .

1.  Crie um objeto de resultado assíncrono chamando [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).
2.  Invoque o retorno de chamada da sessão de mídia chamando [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).
3.  A sessão de mídia chamará [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent). Na implementação desse método, libere os ponteiros ou recursos que você alocou dentro de [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Retornar um **HRESULT** que indica o êxito geral da operação. Se a aquisição de direitos tiver falhado ou o usuário tiver cancelado antes de ser concluído, retorne um código de erro.

O código a seguir mostra como criar o resultado assíncrono e invocar o retorno de chamada.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> </dl>

 

 



