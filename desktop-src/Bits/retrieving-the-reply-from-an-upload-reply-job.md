---
title: Recuperando a resposta de um trabalho Upload-Reply trabalho
description: Para carregar dados em um aplicativo de servidor e fazer com que ele retorne dados para o cliente, especifique o trabalho como um trabalho de RESPOSTA DE UPLOAD DE TIPO DE TRABALHO \_ \_ \_ \_ BG.
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 79ca145a3ed243209fc0059b20823e32da3cf3974850a6bc3e872f43dbd40aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004876"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Recuperando a resposta de um trabalho Upload-Reply trabalho

Um trabalho Upload-Reply BITS, além de carregar um arquivo em um servidor, também examinará uma URL de resposta enviada como parte da resposta do servidor e, em seguida, seguirá automaticamente a URL de resposta e baixará uma resposta dele. Consulte a [documentação do Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) para obter mais detalhes sobre o valor do título BITS-Reply-URL.

De definir o tipo de trabalho como BG \_ JOB TYPE UPLOAD REPLY para criar um Upload-Reply tipo de \_ \_ \_ trabalho. Os dados de resposta estarão disponíveis para o cliente depois que o trabalho entrar no estado BG \_ JOB \_ STATE \_ TRANSFERRED. Para recuperar a resposta, chame um dos seguintes métodos:

-   [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Fornece uma cópia na memória dos dados de resposta. Use esse método para ler os dados de resposta antes ou depois de chamar o [**método IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Se os dados de resposta excederem 1 MB, o aplicativo deverá chamar o método [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) para recuperar o nome do arquivo de resposta e ler seu conteúdo diretamente.

-   [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Fornece o nome do arquivo que contém a resposta. Você deve chamar o **método IBackgroundCopyJob::Complete** antes de abrir e ler o arquivo de resposta; O arquivo de resposta não estará disponível para o cliente até que você chame o **método** Complete.

Chame esses métodos em seu método [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) somente se a resposta for pequena e puder ser processada rapidamente para não bloquear o thread de retorno de chamada. Se você usar [**a notificação de linha de**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) comando em vez do retorno de chamada, passe o identificador de trabalho para o arquivo executável. O arquivo executável usa o identificador de trabalho para chamar **o método Complete** para disponibilizar o arquivo de resposta.

Os exemplos a seguir mostram como usar cada método para recuperar os dados de resposta.

-   [Usando GetReplyData](#using-getreplydata)
-   [Usando GetReplyFileName](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Usando GetReplyData

O exemplo a seguir mostra como recuperar os dados de resposta usando o [**método IBackgroundCopyJob2::GetReplyData.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) O exemplo pressupo que o ponteiro da interface [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido, o tipo do trabalho é upload-reply e o estado do trabalho é BG \_ JOB STATE \_ \_ TRANSFERRED.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BYTE* pReply = NULL;
UINT64 ReplySize;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyData method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyData(&pReply, &ReplySize);
    if (S_OK == hr))
    {
        if (pReply)
        {
            //Do something with the data.
            CoTaskMemFree(pReply);
        }
        else
        {
            //The server application did not return a reply.
        }
    }
    else if (BG_E_TOO_LARGE == hr)
    {
        //The reply exceeds 1 MB. To retrieve the reply, get the reply file name,
        //complete the job, open the reply file, and read the reply.
    }
    else
    {
        //Handle the error
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



## <a name="using-getreplyfilename"></a>Usando GetReplyFileName

O exemplo a seguir mostra como recuperar os dados de resposta usando [**o método IBackgroundCopyJob2::GetReplyFileName.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) O exemplo pressupo que o ponteiro da interface [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido, o tipo de trabalho é upload-reply e o estado do trabalho é BG \_ JOB STATE \_ \_ TRANSFERRED.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR* pszFileName = NULL;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyFileName method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyFileName(&pszFileName);
    if (SUCCEEDED(hr))
    {
        //Calling the Complete method removes the job from the queue, 
        //so make sure you maintain an interface pointer to this job 
        //or retrieve any job related information that you require 
        //when processing the reply.
        hr = pJob->Complete();

        //Open, read the file, and do something with the data.
        CoTaskMemFree(pszFileName);
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



 

 




