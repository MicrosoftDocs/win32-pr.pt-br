---
description: É necessário recuperar as informações de configuração do banco de dados de segurança e do serviço, comparar os dois conjuntos de informações e, em seguida, atualizar a seção de análise do banco de dados de segurança com quaisquer diferenças.
ms.assetid: f8420dde-55a2-40a0-b10d-140c28c0e9e4
title: Implementando SceSvcAttachmentAnalyze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f8501be2caac84c3dc96363eb85a8bc787d2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170637"
---
# <a name="implementing-scesvcattachmentanalyze"></a>Implementando SceSvcAttachmentAnalyze

A função [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) deve recuperar as informações de configuração do banco de dados de segurança e do serviço, comparar os dois conjuntos de informações e, em seguida, atualizar a seção de análise do banco de dados de segurança com quaisquer diferenças. Você pode garantir isso usando o algoritmo a seguir.

**Para implementar o SceSvcAttachmentAnalyze**

1.  Defina as variáveis necessárias para recuperar e definir as informações de segurança e os códigos de retorno.
2.  Chame a função de retorno de chamada pfQueryInfo na estrutura de retorno de chamada para recuperar informações de configuração do banco de dados de segurança.
3.  Recupere as informações correspondentes do serviço.
4.  Compare os dados de configuração recuperados do serviço com o que foi recuperado do banco de dados de segurança.
5.  Se as informações não forem as mesmas, chame a função de retorno de chamada pfSetInfo na estrutura de retorno de chamada para atualizar o banco de dados.
6.  Libere todos os buffers usados para recuperar informações. Chame a função de retorno de chamada pfFreeInfo na estrutura de retorno de chamada para liberar memória usada para informações de banco de dados retornadas.
7.  Se houver qualquer mensagem que a extensão deseja adicionar ao arquivo de log de análise, chame a função de retorno de chamada pfLogInfo na estrutura de retorno de chamada.
8.  Retorne os códigos **SCESTATUS** apropriados.

O exemplo a seguir mostra uma implementação possível de [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md). Observe que, neste exemplo, as funções QueryConfigurationLine e Comparevalue, respectivamente, consultam informações do serviço e comparam esses valores com aqueles recuperados do banco de dados de segurança. A implementação dessas funções não é mostrada.


```C++
#include <windows.h>

SCESTATUS WINAPI SceSvcAttachmentAnalyze (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo
)
{
  
    ////////////////////////////////////////////////////
    // Define variables.
    ////////////////////////////////////////////////////
    PSCESVC_CONFIGURATION_INFO     pConfigInfo = NULL;
    SCESTATUS                      retCode;
    SCE_ENUMERATION_CONTEXT        EnumContext = 0;
  
  

    if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ) 
    {
        return(SCESTATUS_INVALID_PARAMETER);
    }


  ////////////////////////////////////////////////////
  // Retrieve information from security database.
  ///////////////////////////////////////////////////
    do
    {
        retCode =  (*(pSceCbInfo->pfQueryInfo))(
                              pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              NULL,
                              FALSE,
                              &pConfigInfo,
                              &EnumContext
                              );
        if(retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
        {
          ULONG i;
          for(i = 0;i < pConfigInfo->Count; i++)
          {
            if(pConfigInfo->Line[I].Key == NULL) 
                continue;
        
        //////////////////////////////////////////////
        // Query service for corresponding key.
        //////////////////////////////////////////////
            QueryConfigurationLine(
                               pConfigInfo->Line[i].Key,
                               &SystemValue);
        
        //////////////////////////////////////////////
        // Compare values.
        //////////////////////////////////////////////
            CompareValue(
                     pConfigInfo->Line[i].Key,
                     SystemValue,
                     pConfigInfo->Line[i].Value,
                     &Result);
        
        //////////////////////////////////////////////
        // Write to security database if values are 
        // not equal.
        //////////////////////////////////////////////
            if(Result != NULL)
            {
              retCode =  (*(pSceCbInfo->pfSetInfo))(pSceCbInfo->sceHandle,
                                      SceSvcAnalysisInfo,
                                      pConfigInfo->Line[i].Key,
                                      TRUE,
                                      Result);
              if(retCode != SCESTATUS_SUCCESS)
              {
                //////////////////////////////////////////
                // Add code to handle other return codes.
                //////////////////////////////////////////
              }
            }
        }
      
          //////////////////////////////////////////////
          // Free all buffers used to retrieve 
          // SceSvcFree frees memory allocated by call 
          // to SceSvcQueryQueryInfo. 
          /////////////////////////////////////////
        (*(pSceCbInfo->pfFreeInfo)) (PVOID)pConfigInfo);
          pConfigInfo = NULL;
    }
  } while (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL);
  
  
  //////////////////////////////////////////////////
  // If the return code is not SCESTATUS_SUCCESS, add code to 
  // set error message appropriately.
  //////////////////////////////////////////////////
  return retCode;
}
```



 

 



