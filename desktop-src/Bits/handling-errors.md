---
title: Tratamento de erros (BITS)
description: Há dois tipos de erros a tratar em seu aplicativo.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- tratamento de erros BITS
- transferir trabalho BITS , erros
- bits de erros
- erros BITS , tratamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1b0f389b6f0bdeefdfd5868b444384af26027b9b688a8fb83ba89ea370b9360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528806"
---
# <a name="handling-errors-bits"></a>Tratamento de erros (BITS)

Há dois tipos de erros a tratar em seu aplicativo. O primeiro erro é uma chamada de método com falha. Cada método retorna um **valor HRESULT.** A página de referência para cada método identifica os valores de retorno que é mais provável de gerar. Para obter valores de retorno adicionais, consulte [Valores de retorno bits](bits-return-values.md). Para obter o texto da mensagem associado ao valor de retorno, chame o [**método IBackgroundCopyManager::GetErrorDescription.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription)

O segundo tipo de erro a ser identificado é um trabalho [cujo](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) estado faz a transição para ERRO DE ESTADO DO TRABALHO [BG \_ \_ \_](/windows/desktop/api/Bits/ne-bits-bg_job_state) ou ERRO TRANSITÓRIO DE ESTADO **\_ \_ \_ DO \_** TRABALHO BG . Para recuperar informações relacionadas a esses tipos de erros, chame o método [**IBackgroundCopyJob::GetError do**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) trabalho. O método retorna um ponteiro de interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) que contém informações usadas para determinar a causa do erro. Você também pode receber uma notificação de erro registrando-se para receber a notificação de eventos. Para obter detalhes, [consulte Registrando um retorno de chamada COM.](registering-a-com-callback.md)

O BITS considera cada trabalho como atômico. Se um dos arquivos no trabalho gerar um erro, o trabalho permanecerá em um estado de erro até que o erro seja resolvido. Portanto, você não pode excluir o arquivo que está causando o erro do trabalho. No entanto, se o erro for causado pelo servidor não estar disponível ou um arquivo remoto inválido, você poderá chamar o método [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) para identificar um novo servidor ou nome de arquivo.

Depois de determinar a causa do erro, execute uma das seguintes opções:

-   Cancele o trabalho chamando o [**método IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   Para um trabalho de download, chame o método [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) para salvar os arquivos transferidos com êxito antes do erro.
-   Corrige o erro e chame o [**método IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para concluir o trabalho.

Para um trabalho de upload-resposta, verifique o valor do membro **BytesTotal** da estrutura [**BG \_ JOB REPLY \_ \_ PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) para determinar se o erro ocorreu na parte de upload ou resposta do trabalho. Ocorreu um erro no upload se o valor for BG \_ SIZE \_ UNKNOWN.

O exemplo a seguir mostra como recuperar um ponteiro de interface [**IBackgroundCopyError.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) O exemplo pressupo que o ponteiro da interface [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.


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



 

 




