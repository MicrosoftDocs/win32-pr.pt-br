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
# <a name="handling-errors-bits"></a>Tratamento de erros (BITS)

Há dois tipos de erros a serem manipulados em seu aplicativo. O primeiro erro é uma chamada de método com falha. Cada método retorna um valor **HRESULT** . A página de referência para cada método identifica os valores de retorno que é mais provável de gerar. Para obter valores de retorno adicionais, consulte [valores de retorno de bits](bits-return-values.md). Para obter o texto da mensagem associado ao valor de retorno, chame o método [**IBackgroundCopyManager:: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .

O segundo tipo de erro a ser manipulado é um trabalho cujo [estado](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) faz a transição para o [BG \_ erro de \_ estado \_ do trabalho](/windows/desktop/api/Bits/ne-bits-bg_job_state) ou um **\_ \_ \_ \_ erro temporário de estado do trabalho BG**. Para recuperar informações relacionadas a esses tipos de erros, chame o método [**método ibackgroundcopyjob:: geterro**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) do trabalho. O método retorna um ponteiro de interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) que contém as informações que você usa para determinar a causa do erro. Você também pode receber a notificação de erro registrando para receber a notificação de eventos. Para obter detalhes, consulte [registrando um retorno de chamada com](registering-a-com-callback.md).

O BITS considera cada trabalho como atômico. Se um dos arquivos no trabalho gerar um erro, o trabalho permanecerá em um estado de erro até que o erro seja resolvido. Portanto, você não pode excluir o arquivo que está causando o erro do trabalho. No entanto, se o erro for causado pelo servidor não estar disponível ou por um arquivo remoto inválido, você poderá chamar o método [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou [**IBackgroundCopyFile2:: setremotename**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) para identificar um novo servidor ou nome de arquivo.

Depois de determinar a causa do erro, execute uma das seguintes opções:

-   Cancele o trabalho chamando o método [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .
-   Para um trabalho de download, chame o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) para salvar os arquivos que foram transferidos com êxito antes de o erro ter ocorrido.
-   Corrija o erro e chame o método [**método ibackgroundcopyjob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para concluir o trabalho.

Para um trabalho de resposta de upload, verifique o valor do membro **bytesTotal** da estrutura [**de \_ \_ \_ progresso de resposta do trabalho BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) para determinar se o erro ocorreu na parte de upload ou resposta do trabalho. O erro ocorreu no carregamento se o valor for BG \_ tamanho \_ desconhecido.

O exemplo a seguir mostra como recuperar um ponteiro de interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) . O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.


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



 

 




