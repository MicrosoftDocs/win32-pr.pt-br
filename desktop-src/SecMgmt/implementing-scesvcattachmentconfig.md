---
description: Deve recuperar informações do banco de dados de segurança e, em seguida, usar essas informações para configurar o serviço.
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: Implementando SceSvcAttachmentConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98eb519e6422e3036ddfb203811322befd2713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922236"
---
# <a name="implementing-scesvcattachmentconfig"></a>Implementando SceSvcAttachmentConfig

A função [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) deve recuperar informações do banco de dados de segurança e, em seguida, usar essas informações para configurar o serviço.

Ao implementar o [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), você pode recuperar todas as informações e, em seguida, configurar o serviço, ou recuperar e configurar o serviço em etapas. O algoritmo a seguir recupera todas as informações e, em seguida, configura o serviço.

**Para implementar o SceSvcAttachmentConfig**

1.  Defina as variáveis necessárias para recuperar informações e códigos de retorno.
2.  Chame a função de retorno de chamada pfQueryInfo na estrutura de retorno de chamada para recuperar informações de configuração do banco de dados de segurança.
3.  Configure o sistema com as informações retornadas.
4.  Chame a função de retorno de chamada pfFreeInfo na estrutura de retorno de chamada para liberar memória usada para informações retornadas.
5.  Se houver qualquer mensagem que a extensão deseja adicionar ao arquivo de log de análise, chame a função de retorno de chamada pfLogInfo na estrutura de retorno de chamada.
6.  Retorne os códigos **SCESTATUS** apropriados.

O exemplo a seguir mostra uma implementação possível de [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md). Observe que, neste exemplo, a função ProcessConfigurationLine define a configuração do serviço. A implementação dessa função não é mostrada.


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig (
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
      // Retrieve configuration information and configure
      // system. 
      ////////////////////////////////////////////////////
      do
      {
            retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                  SceSvcConfigurationInfo,
                                  NULL,
                                  FALSE,
                                  (PVOID *)&pConfigInfo,
                                  &EnumContext
                                 );
            if (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
            {
              ULONG i:
              //////////////////////////////////////////////////
              // Configure system.
              /////////////////////////////////////////////////
              for(i = 0; < pConfigInfo->Count; i++)
              {
                if(pConfigInfo->Line[i].Key == NULL) 
                    continue;
                ProcessConfigurationLine(pConfigInfo->Line[i]);
              }
      
      
              //////////////////////////////////////////////////
              // Free data returned.
              /////////////////////////////////////////////////
              (*(pSceCbInfo->pfFreeInfo)) ((PVOPID)pConfigInfo);
              pConfigInfo = NULL;
            }
        } while (retCode == SCESTATUS_SUCCESS && CountReturned > 0);
  
  
  ////////////////////////////////////////////////////
  // Add code for other return codes if retCode is 
  // not SCESTATUS_SUCCESS.
  ///////////////////////////////////////////////////
  return retCode;
}
```



 

 



