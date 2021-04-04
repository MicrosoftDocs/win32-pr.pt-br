---
title: Controlar um download de BITS em uma conexão cara
description: Bloquear o download em uma conexão cara, como um link de celular móvel.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- baixando BITS, como
- baixa BITS, evitando custos caros
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 6326838f08f1879929d9a6be67ef94c4aa035e00
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103823494"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a><span data-ttu-id="d060d-105">Controlar um download de BITS em uma conexão cara</span><span class="sxs-lookup"><span data-stu-id="d060d-105">Control a BITS download over an expensive connection</span></span>

<span data-ttu-id="d060d-106">Este tópico mostra como bloquear o download de um trabalho do BITS em uma conexão cara, como um link para celular móvel.</span><span class="sxs-lookup"><span data-stu-id="d060d-106">This topic shows how to block a BITS job from downloading over an expensive connection such as a roaming cellular link.</span></span> <span data-ttu-id="d060d-107">BITS é uma API assíncrona em que o aplicativo cria um trabalho, adiciona URLs a esse trabalho e chama a função [**resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) do objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d060d-107">BITS is an asynchronous API where the application creates a job, adds URLs to that job, and calls the job object's [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) function.</span></span> <span data-ttu-id="d060d-108">A partir desse ponto, o BITS escolhe quando o trabalho é baixado com base em fatores como a prioridade do trabalho e a política de transferência.</span><span class="sxs-lookup"><span data-stu-id="d060d-108">From that point, BITS chooses when the job downloads based on factors such as job priority and the transfer policy.</span></span> <span data-ttu-id="d060d-109">Depois que o download do trabalho for concluído, o BITS notificará o aplicativo de que a URL foi baixada (se o aplicativo tiver se registrado para a notificação de conclusão).</span><span class="sxs-lookup"><span data-stu-id="d060d-109">After the job has finished downloading, BITS notifies the application that the URL has been downloaded (if the application has registered for completion notification).</span></span> <span data-ttu-id="d060d-110">Durante o tempo de vida do trabalho, se a rede do usuário final mudar, como se o usuário está viajando e atualmente incorrendo em tarifas de roaming, o BITS suspenderá o trabalho até que as condições de rede sejam ideais.</span><span class="sxs-lookup"><span data-stu-id="d060d-110">During the job's lifetime, if the end user's network changes—such as if the user is traveling and is currently incurring roaming fees—then BITS will suspend the job until network conditions are optimal.</span></span> <span data-ttu-id="d060d-111">As instruções passo a passo a seguir mostram como criar o trabalho e especificar as configurações de política de transferência apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d060d-111">The following step-by-step instructions show how to create the job and specify the appropriate transfer policy settings.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d060d-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d060d-112">Prerequisites</span></span>

-   <span data-ttu-id="d060d-113">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d060d-113">Microsoft Visual Studio</span></span>

## <a name="instructions"></a><span data-ttu-id="d060d-114">Instruções</span><span class="sxs-lookup"><span data-stu-id="d060d-114">Instructions</span></span>

### <a name="step-1-include-the-required-bits-header-files"></a><span data-ttu-id="d060d-115">Etapa 1: incluir os arquivos de cabeçalho do BITS necessários</span><span class="sxs-lookup"><span data-stu-id="d060d-115">Step 1: Include the required BITS header files</span></span>

<span data-ttu-id="d060d-116">Insira as seguintes diretivas de cabeçalho na parte superior do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="d060d-116">Insert the following header directives at the top of the source file.</span></span>


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a><span data-ttu-id="d060d-117">Etapa 2: inicializar COM</span><span class="sxs-lookup"><span data-stu-id="d060d-117">Step 2: Initialize COM</span></span>

<span data-ttu-id="d060d-118">Antes de instanciar a interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) (usada para criar um trabalho do bits), você deve inicializar com, definir o modelo de Threading com e especificar um nível de representação de, pelo menos, o Impersonate de nível de imp do RPC \_ C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d060d-118">Before instantiating the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface (used to create a BITS job), you must initialize COM, set the COM threading model, and specify an impersonation level of at least RPC\_C\_IMP\_LEVEL\_IMPERSONATE.</span></span>


```C++
// Initialize COM and specify the COM threading model.
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 // Specify an impersonation level of at least RPC_C_IMP_LEVEL_IMPERSONATE.
 hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                           RPC_C_AUTHN_LEVEL_CONNECT,
                           RPC_C_IMP_LEVEL_IMPERSONATE,
                           NULL, EOAC_NONE, 0);
 if (SUCCEEDED(hr))
 {
  ...
```



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a><span data-ttu-id="d060d-119">Etapa 3: instanciar a interface IBackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="d060d-119">Step 3: Instantiate the IBackgroundCopyManager interface</span></span>

<span data-ttu-id="d060d-120">Use a interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para criar trabalhos de transferência, recuperar um objeto enumerador que contém os trabalhos na fila e recuperar trabalhos individuais da fila.</span><span class="sxs-lookup"><span data-stu-id="d060d-120">Use the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to create transfer jobs, retrieve an enumerator object that contains the jobs in the queue, and retrieve individual jobs from the queue.</span></span>


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a><span data-ttu-id="d060d-121">Etapa 4: criar o trabalho do BITS</span><span class="sxs-lookup"><span data-stu-id="d060d-121">Step 4: Create the BITS job</span></span>

<span data-ttu-id="d060d-122">Somente o usuário que cria o trabalho ou um usuário com privilégios de administrador pode adicionar arquivos ao trabalho e alterar as propriedades do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d060d-122">Only the user who creates the job or a user with administrator privileges can add files to the job and change the job's properties.</span></span>


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a><span data-ttu-id="d060d-123">Etapa 5: especificar a configuração da política de transferência para o trabalho</span><span class="sxs-lookup"><span data-stu-id="d060d-123">Step 5: Specify the transfer policy setting for the job</span></span>

<span data-ttu-id="d060d-124">É aqui que você especifica a política de transferência de estado de custo.</span><span class="sxs-lookup"><span data-stu-id="d060d-124">This is where you specify the cost state transfer policy.</span></span> <span data-ttu-id="d060d-125">Você pode definir vários sinalizadores de estado de custo de BITS \_ \_ usando uma combinação de bit a bit **ou** de para atingir os resultados desejados.</span><span class="sxs-lookup"><span data-stu-id="d060d-125">You can set several BITS\_COST\_STATE flags by using a bitwise **OR** combination to achieve the desired results.</span></span>


```C++
BITS_JOB_PROPERTY_VALUE propval;
IBackgroundCopyJob5* pBackgroundCopyJob5;

propval.Dword = BITS_COST_STATE_USAGE_BASED
              | BITS_COST_STATE_OVERCAP_THROTTLED
              | BITS_COST_STATE_BELOW_CAP
              | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
              | BITS_COST_STATE_UNRESTRICTED;

hr = pBackgroundCopyJob->QueryInterface(__uuidof(IBackgroundCopyJob5),
                                        reinterpret_cast<void**>(&pBackgroundCopyJob5));
if(SUCCEEDED(hr))
{
 pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);
}
```



## <a name="example"></a><span data-ttu-id="d060d-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d060d-126">Example</span></span>

<span data-ttu-id="d060d-127">O exemplo de código a seguir mostra como definir a política de transferência de um trabalho do BITS para que o processamento do trabalho não ocorra enquanto determinadas condições são atendidas — por exemplo, quando o usuário está em roaming ou excedeu seu limite de transferência de dados mensal.</span><span class="sxs-lookup"><span data-stu-id="d060d-127">The following code example shows how to set a BITS job's transfer policy so that the processing of the job doesn't occur while certain conditions are met—such as when the user is roaming or has exceeded their monthly data transfer limit.</span></span>


```C++
//*********************************************************
//
//    Copyright (c) Microsoft. All rights reserved.
//    This code is licensed under the Microsoft Public License.
//    THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF
//    ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY
//    IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR
//    PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.
//
//*********************************************************

#define WIN32_LEAN_AND_MEAN             // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // define wprintf


int main()
{
 HRESULT hr = S_OK;
 GUID guidJob;
 IBackgroundCopyJob5* pBackgroundCopyJob5;  
 IBackgroundCopyJob* pBackgroundCopyJob;
 IBackgroundCopyManager* pQueueMgr;
 BITS_JOB_PROPERTY_VALUE propval;

 // Specify the COM threading model.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  // The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
  hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                            RPC_C_AUTHN_LEVEL_CONNECT,
                            RPC_C_IMP_LEVEL_IMPERSONATE,
                            NULL, EOAC_NONE, 0);

  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                         NULL,
                         CLSCTX_LOCAL_SERVER,
                         __uuidof(IBackgroundCopyManager),
                         (void **)&pQueueMgr);

   if (FAILED(hr))
   {
    // Failed to connect to BITS.
    wprintf(L"Failed to connect to BITS with error %x\n",hr);
    goto done;
   }

   // Create a BITS job.
   wprintf(L"Creating Job...\n");

   hr = pQueueMgr->CreateJob(L"TransferPolicy",
                             BG_JOB_TYPE_DOWNLOAD,
                             &guidJob,
                             (IBackgroundCopyJob **)&pBackgroundCopyJob);

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }

   wprintf(L" Job is succesfully created ...\n");

   // Set the Transfer Policy for the job.
   propval.Dword = BITS_COST_STATE_USAGE_BASED 
                 | BITS_COST_STATE_OVERCAP_THROTTLED
                 | BITS_COST_STATE_BELOW_CAP
                 | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
                 | BITS_COST_STATE_UNRESTRICTED;

   hr = pBackgroundCopyJob->QueryInterface(
         __uuidof(IBackgroundCopyJob5),
         reinterpret_cast<void**>(&pBackgroundCopyJob5)
        );

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }
   pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);

   // Get the Transfer Policy for the new job.
   BITS_JOB_PROPERTY_VALUE actual_propval;

   wprintf(L"Getting TransferPolicy Property ...\n");

   hr = pBackgroundCopyJob5->GetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, 
                                         &actual_propval);
   if (FAILED(hr))
   {
    // SetSSLSecurityFlags failed.
    wprintf(L"GetProperty failed with error %x\n",hr);
    goto cancel;
   }

   DWORD job_transferpolicy = actual_propval.Dword;
   wprintf(L"get TransferPolicy Property returned %#x\n", job_transferpolicy);
  }
done:
  CoUninitialize();
 }
 return 1;

cancel:
 pBackgroundCopyJob->Cancel(); 
 pBackgroundCopyJob->Release();
 goto done;
}
```



 

 




