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
# <a name="implementing-scesvcattachmentanalyze"></a><span data-ttu-id="bf9f5-103">Implementando SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="bf9f5-103">Implementing SceSvcAttachmentAnalyze</span></span>

<span data-ttu-id="bf9f5-104">A função [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) deve recuperar as informações de configuração do banco de dados de segurança e do serviço, comparar os dois conjuntos de informações e, em seguida, atualizar a seção de análise do banco de dados de segurança com quaisquer diferenças.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-104">The [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) function must retrieve configuration information from the security database and the service, compare the two sets of information, and then update the analysis section of the security database with any differences.</span></span> <span data-ttu-id="bf9f5-105">Você pode garantir isso usando o algoritmo a seguir.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-105">You can ensure this by using the following algorithm.</span></span>

<span data-ttu-id="bf9f5-106">**Para implementar o SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="bf9f5-106">**To implement SceSvcAttachmentAnalyze**</span></span>

1.  <span data-ttu-id="bf9f5-107">Defina as variáveis necessárias para recuperar e definir as informações de segurança e os códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-107">Define the variables needed to retrieve and set the security information and return codes.</span></span>
2.  <span data-ttu-id="bf9f5-108">Chame a função de retorno de chamada pfQueryInfo na estrutura de retorno de chamada para recuperar informações de configuração do banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-108">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="bf9f5-109">Recupere as informações correspondentes do serviço.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-109">Retrieve the corresponding information from the service.</span></span>
4.  <span data-ttu-id="bf9f5-110">Compare os dados de configuração recuperados do serviço com o que foi recuperado do banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-110">Compare the configuration data retrieved from the service with that retrieved from the security database.</span></span>
5.  <span data-ttu-id="bf9f5-111">Se as informações não forem as mesmas, chame a função de retorno de chamada pfSetInfo na estrutura de retorno de chamada para atualizar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-111">If the information is not the same, call the pfSetInfo callback function in the callback structure to update the database.</span></span>
6.  <span data-ttu-id="bf9f5-112">Libere todos os buffers usados para recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-112">Free all buffers used to retrieve information.</span></span> <span data-ttu-id="bf9f5-113">Chame a função de retorno de chamada pfFreeInfo na estrutura de retorno de chamada para liberar memória usada para informações de banco de dados retornadas.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-113">Call the pfFreeInfo callback function in the callback structure to free memory used for returned database information.</span></span>
7.  <span data-ttu-id="bf9f5-114">Se houver qualquer mensagem que a extensão deseja adicionar ao arquivo de log de análise, chame a função de retorno de chamada pfLogInfo na estrutura de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-114">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
8.  <span data-ttu-id="bf9f5-115">Retorne os códigos **SCESTATUS** apropriados.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-115">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="bf9f5-116">O exemplo a seguir mostra uma implementação possível de [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="bf9f5-116">The following example shows one possible implementation of [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span></span> <span data-ttu-id="bf9f5-117">Observe que, neste exemplo, as funções QueryConfigurationLine e Comparevalue, respectivamente, consultam informações do serviço e comparam esses valores com aqueles recuperados do banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-117">Note that in this example, the functions QueryConfigurationLine and CompareValue respectively query information from the service and compare those values with those retrieved from the security database.</span></span> <span data-ttu-id="bf9f5-118">A implementação dessas funções não é mostrada.</span><span class="sxs-lookup"><span data-stu-id="bf9f5-118">The implementation of these functions is not shown.</span></span>


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



 

 



