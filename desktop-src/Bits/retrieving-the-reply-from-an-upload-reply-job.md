---
title: Recuperando a resposta de um trabalho de Upload-Reply
description: Para carregar dados em um aplicativo de servidor e fazê-lo retornar dados ao cliente, especifique o trabalho como um \_ trabalho de resposta de carregamento de tipo de trabalho BG \_ \_ \_ .
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 582a37a31c13c5cc3e0b44c51a767cfbe465c64c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916013"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a><span data-ttu-id="99f63-103">Recuperando a resposta de um trabalho de Upload-Reply</span><span class="sxs-lookup"><span data-stu-id="99f63-103">Retrieving the Reply from an Upload-Reply Job</span></span>

<span data-ttu-id="99f63-104">Um trabalho de Upload-Reply BITS, além de carregar um arquivo em um servidor, também examinará uma URL de resposta enviada como parte da resposta do servidor e, em seguida, seguirá automaticamente a URL de resposta e baixará uma resposta dela.</span><span class="sxs-lookup"><span data-stu-id="99f63-104">A BITS Upload-Reply job, in addition to uploading a file to a server, will also examine a reply URL sent as part of the server reply and then automatically follow the reply URL and download a response from it.</span></span> <span data-ttu-id="99f63-105">Confira a confirmação da documentação do [fragmento](/windows/desktop/Bits/ack-for-fragment) para obter mais detalhes sobre o valor do cabeçalho bits-Reply-URL.</span><span class="sxs-lookup"><span data-stu-id="99f63-105">See the [Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) documentation for more details about the BITS-Reply-URL header value.</span></span>

<span data-ttu-id="99f63-106">Defina o tipo de trabalho como \_ BG \_ \_ resposta de carregamento do tipo \_ de trabalho para criar um trabalho de tipo de Upload-Reply.</span><span class="sxs-lookup"><span data-stu-id="99f63-106">Set the job type as BG\_JOB\_TYPE\_UPLOAD\_REPLY to create an Upload-Reply type job.</span></span> <span data-ttu-id="99f63-107">Os dados de resposta estão disponíveis para o cliente depois que o trabalho entra no \_ estado de transferência do estado do trabalho BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="99f63-107">The reply data is available to the client after the job enters the BG\_JOB\_STATE\_TRANSFERRED state.</span></span> <span data-ttu-id="99f63-108">Para recuperar a resposta, chame um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="99f63-108">To retrieve the reply, call one of the following methods:</span></span>

-   [<span data-ttu-id="99f63-109">**IBackgroundCopyJob2::GetReplyData**</span><span class="sxs-lookup"><span data-stu-id="99f63-109">**IBackgroundCopyJob2::GetReplyData**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    <span data-ttu-id="99f63-110">Fornece uma cópia na memória dos dados de resposta.</span><span class="sxs-lookup"><span data-stu-id="99f63-110">Provides an in-memory copy of the reply data.</span></span> <span data-ttu-id="99f63-111">Use este método para ler os dados de resposta antes ou depois de chamar o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="99f63-111">Use this method to read the reply data before or after calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="99f63-112">Se os dados de resposta excederem 1 MB, o aplicativo deverá chamar o método [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) para recuperar o nome do arquivo de resposta e ler seu conteúdo diretamente.</span><span class="sxs-lookup"><span data-stu-id="99f63-112">If the reply data exceeds 1 MB, the application must call the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method to retrieve the name of the reply file and read its contents directly.</span></span>

-   [<span data-ttu-id="99f63-113">**IBackgroundCopyJob2::GetReplyFileName**</span><span class="sxs-lookup"><span data-stu-id="99f63-113">**IBackgroundCopyJob2::GetReplyFileName**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    <span data-ttu-id="99f63-114">Fornece o nome do arquivo que contém a resposta.</span><span class="sxs-lookup"><span data-stu-id="99f63-114">Provides the name of the file that contains the reply.</span></span> <span data-ttu-id="99f63-115">Você deve chamar o método **método ibackgroundcopyjob:: Complete** antes de abrir e ler o arquivo de resposta; o arquivo de resposta não estará disponível para o cliente até que você chame o método **Complete** .</span><span class="sxs-lookup"><span data-stu-id="99f63-115">You must call the **IBackgroundCopyJob::Complete** method before opening and reading the reply file; the reply file is not available to the client until you call the **Complete** method.</span></span>

<span data-ttu-id="99f63-116">Chame esses métodos no método [**IBackgroundCopyCallback:: JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) somente se a resposta for pequena e puder ser processada rapidamente para não bloquear o thread de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="99f63-116">Call these methods in your [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) method only if the reply is small and can be processed quickly so as to not block the callback thread.</span></span> <span data-ttu-id="99f63-117">Se você usar a [**notificação de linha de comando**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) em vez do retorno de chamada, passe o identificador de trabalho para o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="99f63-117">If you use [**command line notification**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) instead of the callback, pass the job identifier to the executable file.</span></span> <span data-ttu-id="99f63-118">O arquivo executável usa o identificador de trabalho para chamar o método **Complete** para disponibilizar o arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="99f63-118">The executable file uses the job identifier to call the **Complete** method to make the reply file available.</span></span>

<span data-ttu-id="99f63-119">Os exemplos a seguir mostram como usar cada método para recuperar os dados de resposta.</span><span class="sxs-lookup"><span data-stu-id="99f63-119">The following examples show how to use each method to retrieve the reply data.</span></span>

-   [<span data-ttu-id="99f63-120">Usando GetReplyData</span><span class="sxs-lookup"><span data-stu-id="99f63-120">Using GetReplyData</span></span>](#using-getreplydata)
-   [<span data-ttu-id="99f63-121">Usando GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="99f63-121">Using GetReplyFileName</span></span>](#using-getreplyfilename)

## <a name="using-getreplydata"></a><span data-ttu-id="99f63-122">Usando GetReplyData</span><span class="sxs-lookup"><span data-stu-id="99f63-122">Using GetReplyData</span></span>

<span data-ttu-id="99f63-123">O exemplo a seguir mostra como recuperar os dados de resposta usando o método [**IBackgroundCopyJob2:: GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) .</span><span class="sxs-lookup"><span data-stu-id="99f63-123">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) method.</span></span> <span data-ttu-id="99f63-124">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido, o tipo do trabalho é upload-Reply e o estado do trabalho é BG \_ Job \_ estado \_ transferido.</span><span class="sxs-lookup"><span data-stu-id="99f63-124">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of the job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


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



## <a name="using-getreplyfilename"></a><span data-ttu-id="99f63-125">Usando GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="99f63-125">Using GetReplyFileName</span></span>

<span data-ttu-id="99f63-126">O exemplo a seguir mostra como recuperar os dados de resposta usando o método [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) .</span><span class="sxs-lookup"><span data-stu-id="99f63-126">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method.</span></span> <span data-ttu-id="99f63-127">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido, o tipo de trabalho é upload-Reply e o estado do trabalho é BG \_ Job \_ estado \_ transferido.</span><span class="sxs-lookup"><span data-stu-id="99f63-127">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


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



 

 




