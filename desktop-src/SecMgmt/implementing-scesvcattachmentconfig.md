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
# <a name="implementing-scesvcattachmentconfig"></a><span data-ttu-id="33542-103">Implementando SceSvcAttachmentConfig</span><span class="sxs-lookup"><span data-stu-id="33542-103">Implementing SceSvcAttachmentConfig</span></span>

<span data-ttu-id="33542-104">A função [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) deve recuperar informações do banco de dados de segurança e, em seguida, usar essas informações para configurar o serviço.</span><span class="sxs-lookup"><span data-stu-id="33542-104">The [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) function must retrieve information from the security database and then use that information to configure the service.</span></span>

<span data-ttu-id="33542-105">Ao implementar o [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), você pode recuperar todas as informações e, em seguida, configurar o serviço, ou recuperar e configurar o serviço em etapas.</span><span class="sxs-lookup"><span data-stu-id="33542-105">When implementing [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), you can either retrieve all of the information and then configure the service, or retrieve and configure the service in steps.</span></span> <span data-ttu-id="33542-106">O algoritmo a seguir recupera todas as informações e, em seguida, configura o serviço.</span><span class="sxs-lookup"><span data-stu-id="33542-106">The following algorithm retrieves all of the information and then configures the service.</span></span>

<span data-ttu-id="33542-107">**Para implementar o SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="33542-107">**To implement SceSvcAttachmentConfig**</span></span>

1.  <span data-ttu-id="33542-108">Defina as variáveis necessárias para recuperar informações e códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="33542-108">Define the variables needed to retrieve information and return codes.</span></span>
2.  <span data-ttu-id="33542-109">Chame a função de retorno de chamada pfQueryInfo na estrutura de retorno de chamada para recuperar informações de configuração do banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="33542-109">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="33542-110">Configure o sistema com as informações retornadas.</span><span class="sxs-lookup"><span data-stu-id="33542-110">Configure the system with the returned information.</span></span>
4.  <span data-ttu-id="33542-111">Chame a função de retorno de chamada pfFreeInfo na estrutura de retorno de chamada para liberar memória usada para informações retornadas.</span><span class="sxs-lookup"><span data-stu-id="33542-111">Call the pfFreeInfo callback function in the callback structure to free memory used for returned information.</span></span>
5.  <span data-ttu-id="33542-112">Se houver qualquer mensagem que a extensão deseja adicionar ao arquivo de log de análise, chame a função de retorno de chamada pfLogInfo na estrutura de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="33542-112">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
6.  <span data-ttu-id="33542-113">Retorne os códigos **SCESTATUS** apropriados.</span><span class="sxs-lookup"><span data-stu-id="33542-113">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="33542-114">O exemplo a seguir mostra uma implementação possível de [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="33542-114">The following example shows one possible implementation of [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span></span> <span data-ttu-id="33542-115">Observe que, neste exemplo, a função ProcessConfigurationLine define a configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="33542-115">Note that in this example, the function ProcessConfigurationLine sets the service configuration.</span></span> <span data-ttu-id="33542-116">A implementação dessa função não é mostrada.</span><span class="sxs-lookup"><span data-stu-id="33542-116">The implementation of this function is not shown.</span></span>


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



 

 



