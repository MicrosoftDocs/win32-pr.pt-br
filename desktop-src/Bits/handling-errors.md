---
title: Tratamento de erros (BITS)
description: Há dois tipos de erros a serem manipulados em seu aplicativo.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- tratando BITS de erros
- transferir BITS de trabalho, erros
- BITS de erros
- BITS de erros, lidando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008683"
---
# <a name="handling-errors-bits"></a><span data-ttu-id="e2db2-107">Tratamento de erros (BITS)</span><span class="sxs-lookup"><span data-stu-id="e2db2-107">Handling Errors (BITS)</span></span>

<span data-ttu-id="e2db2-108">Há dois tipos de erros a serem manipulados em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2db2-108">There are two types of errors to handle in your application.</span></span> <span data-ttu-id="e2db2-109">O primeiro erro é uma chamada de método com falha.</span><span class="sxs-lookup"><span data-stu-id="e2db2-109">The first error is a failed method call.</span></span> <span data-ttu-id="e2db2-110">Cada método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2db2-110">Each method returns an **HRESULT** value.</span></span> <span data-ttu-id="e2db2-111">A página de referência para cada método identifica os valores de retorno que é mais provável de gerar.</span><span class="sxs-lookup"><span data-stu-id="e2db2-111">The reference page for each method identifies the return values that it is most likely to generate.</span></span> <span data-ttu-id="e2db2-112">Para obter valores de retorno adicionais, consulte [valores de retorno de bits](bits-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e2db2-112">For additional return values, see [BITS Return Values](bits-return-values.md).</span></span> <span data-ttu-id="e2db2-113">Para obter o texto da mensagem associado ao valor de retorno, chame o método [**IBackgroundCopyManager:: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .</span><span class="sxs-lookup"><span data-stu-id="e2db2-113">To get the message text associated with the return value, call the [**IBackgroundCopyManager::GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) method.</span></span>

<span data-ttu-id="e2db2-114">O segundo tipo de erro a ser manipulado é um trabalho cujo [estado](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) faz a transição para o [BG \_ erro de \_ estado \_ do trabalho](/windows/desktop/api/Bits/ne-bits-bg_job_state) ou um **\_ \_ \_ \_ erro temporário de estado do trabalho BG**.</span><span class="sxs-lookup"><span data-stu-id="e2db2-114">The second type of error to handle is a job whose [state](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) transitions to [BG\_JOB\_STATE\_ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) or **BG\_JOB\_STATE\_TRANSIENT\_ERROR**.</span></span> <span data-ttu-id="e2db2-115">Para recuperar informações relacionadas a esses tipos de erros, chame o método [**método ibackgroundcopyjob:: geterro**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e2db2-115">To retrieve information related to these types of errors, call the job's [**IBackgroundCopyJob::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) method.</span></span> <span data-ttu-id="e2db2-116">O método retorna um ponteiro de interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) que contém as informações que você usa para determinar a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="e2db2-116">The method returns an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer that contains information you use to determine the cause of the error.</span></span> <span data-ttu-id="e2db2-117">Você também pode receber a notificação de erro registrando para receber a notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="e2db2-117">You can also receive error notification by registering to receive event notification.</span></span> <span data-ttu-id="e2db2-118">Para obter detalhes, consulte [registrando um retorno de chamada com](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="e2db2-118">For details, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="e2db2-119">O BITS considera cada trabalho como atômico.</span><span class="sxs-lookup"><span data-stu-id="e2db2-119">BITS considers each job to be atomic.</span></span> <span data-ttu-id="e2db2-120">Se um dos arquivos no trabalho gerar um erro, o trabalho permanecerá em um estado de erro até que o erro seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="e2db2-120">If one of the files in the job generates an error, the job remains in an error state until the error is resolved.</span></span> <span data-ttu-id="e2db2-121">Portanto, você não pode excluir o arquivo que está causando o erro do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e2db2-121">Thus, you cannot delete the file that is causing the error from the job.</span></span> <span data-ttu-id="e2db2-122">No entanto, se o erro for causado pelo servidor não estar disponível ou por um arquivo remoto inválido, você poderá chamar o método [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou [**IBackgroundCopyFile2:: setremotename**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) para identificar um novo servidor ou nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2db2-122">However, if the error is caused by the server not being available or an invalid remote file, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) or [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method to identify a new server or file name.</span></span>

<span data-ttu-id="e2db2-123">Depois de determinar a causa do erro, execute uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="e2db2-123">After determining the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="e2db2-124">Cancele o trabalho chamando o método [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="e2db2-124">Cancel the job by calling the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>
-   <span data-ttu-id="e2db2-125">Para um trabalho de download, chame o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) para salvar os arquivos que foram transferidos com êxito antes de o erro ter ocorrido.</span><span class="sxs-lookup"><span data-stu-id="e2db2-125">For a download job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method to save the files that transferred successfully before the error occurred.</span></span>
-   <span data-ttu-id="e2db2-126">Corrija o erro e chame o método [**método ibackgroundcopyjob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para concluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e2db2-126">Fix the error and call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method to finish the job.</span></span>

<span data-ttu-id="e2db2-127">Para um trabalho de resposta de upload, verifique o valor do membro **bytesTotal** da estrutura [**de \_ \_ \_ progresso de resposta do trabalho BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) para determinar se o erro ocorreu na parte de upload ou resposta do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e2db2-127">For an upload-reply job, check the value of the **BytesTotal** member of the [**BG\_JOB\_REPLY\_PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) structure to determine if the error occurred on the upload or reply portion of the job.</span></span> <span data-ttu-id="e2db2-128">O erro ocorreu no carregamento se o valor for BG \_ tamanho \_ desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e2db2-128">The error occurred on the upload if the value is BG\_SIZE\_UNKNOWN.</span></span>

<span data-ttu-id="e2db2-129">O exemplo a seguir mostra como recuperar um ponteiro de interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) .</span><span class="sxs-lookup"><span data-stu-id="e2db2-129">The following example shows how to retrieve an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer.</span></span> <span data-ttu-id="e2db2-130">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.</span><span class="sxs-lookup"><span data-stu-id="e2db2-130">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




