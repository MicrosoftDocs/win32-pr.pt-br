---
title: Controlar um download de BITS em uma conexão cara
description: Bloquear o download em uma conexão cara, como um link de celular móvel.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- baixando BITS, como
- baixa BITS, evitando custos caros
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7cb09dbd277d9ec74ce4988db210bf80c22d97ccaa3054a170fc1c9913282cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959485"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a>Controlar um download de BITS em uma conexão cara

Este tópico mostra como bloquear o download de um trabalho do BITS em uma conexão cara, como um link para celular móvel. BITS é uma API assíncrona em que o aplicativo cria um trabalho, adiciona URLs a esse trabalho e chama a função [**resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) do objeto de trabalho. A partir desse ponto, o BITS escolhe quando o trabalho é baixado com base em fatores como a prioridade do trabalho e a política de transferência. Depois que o download do trabalho for concluído, o BITS notificará o aplicativo de que a URL foi baixada (se o aplicativo tiver se registrado para a notificação de conclusão). Durante o tempo de vida do trabalho, se a rede do usuário final mudar, como se o usuário está viajando e atualmente incorrendo em tarifas de roaming, o BITS suspenderá o trabalho até que as condições de rede sejam ideais. As instruções passo a passo a seguir mostram como criar o trabalho e especificar as configurações de política de transferência apropriadas.

### <a name="prerequisites"></a>Pré-requisitos

-   Microsoft Visual Studio

## <a name="instructions"></a>Instruções

### <a name="step-1-include-the-required-bits-header-files"></a>Etapa 1: incluir os arquivos de cabeçalho do BITS necessários

Insira as seguintes diretivas de cabeçalho na parte superior do arquivo de origem.


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a>Etapa 2: inicializar COM

Antes de instanciar a interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) (usada para criar um trabalho do bits), você deve inicializar com, definir o modelo de Threading com e especificar um nível de representação de, pelo menos, o Impersonate de nível de imp do RPC \_ C \_ \_ \_ .


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



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a>Etapa 3: instanciar a interface IBackgroundCopyManager

Use a interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para criar trabalhos de transferência, recuperar um objeto enumerador que contém os trabalhos na fila e recuperar trabalhos individuais da fila.


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a>Etapa 4: criar o trabalho do BITS

Somente o usuário que cria o trabalho ou um usuário com privilégios de administrador pode adicionar arquivos ao trabalho e alterar as propriedades do trabalho.


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a>Etapa 5: especificar a configuração da política de transferência para o trabalho

É aqui que você especifica a política de transferência de estado de custo. Você pode definir vários sinalizadores de estado de custo de BITS \_ \_ usando uma combinação de bit a bit **ou** de para atingir os resultados desejados.


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



## <a name="example"></a>Exemplo

O exemplo de código a seguir mostra como definir a política de transferência de um trabalho do BITS para que o processamento do trabalho não ocorra enquanto determinadas condições são atendidas — por exemplo, quando o usuário está em roaming ou excedeu seu limite de transferência de dados mensal.


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



 

 




