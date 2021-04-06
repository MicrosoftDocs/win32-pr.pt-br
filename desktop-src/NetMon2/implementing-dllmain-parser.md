---
description: Monitor de Rede usa a função de exportação DllMain para identificar a existência do analisador e liberar os recursos que o Monitor de Rede usa para armazenar informações sobre o analisador.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementando o analisador DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646787"
---
# <a name="implementing-dllmain-parser"></a><span data-ttu-id="7dc7c-103">Implementando o analisador DllMain</span><span class="sxs-lookup"><span data-stu-id="7dc7c-103">Implementing DllMain Parser</span></span>

<span data-ttu-id="7dc7c-104">Monitor de Rede usa a função de exportação **DllMain** para identificar a existência do analisador e liberar os recursos que o monitor de rede usa para armazenar informações sobre o analisador.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-104">Network Monitor uses the **DllMain** export function to identify the existence of the parser, and release resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="7dc7c-105">Quando Monitor de Rede chama **DllMain** pela primeira vez, a DLL do analisador chama [**createprotocol**](createprotocol.md) para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7dc7c-105">When Network Monitor calls **DllMain** for the first time, the parser DLL calls [**CreateProtocol**](createprotocol.md) to do the following:</span></span>

-   <span data-ttu-id="7dc7c-106">Especifique o protocolo que o analisador detecta.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-106">Specify the protocol that the parser detects.</span></span>
-   <span data-ttu-id="7dc7c-107">Forneça pontos de entrada para as funções de exportação do analisador restantes que Monitor de Rede chamadas.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-107">Provide entry points for remaining parser export functions that Network Monitor calls.</span></span>

<span data-ttu-id="7dc7c-108">Quando Monitor de Rede chama **DllMain** pela última vez, **DllMain** chama [**DestroyProtocol**](destroyprotocol.md) para liberar todos os recursos que monitor de rede usa para armazenar informações sobre o analisador.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-108">When Network Monitor calls **DllMain** for the last time, **DllMain** calls [**DestroyProtocol**](destroyprotocol.md) to release all resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="7dc7c-109">O procedimento a seguir identifica as etapas necessárias para implementar o **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-109">The following procedure identifies the steps necessary to implement **DllMain**.</span></span>

<span data-ttu-id="7dc7c-110">**Para implementar o DllMain**</span><span class="sxs-lookup"><span data-stu-id="7dc7c-110">**To implement DllMain**</span></span>

1.  <span data-ttu-id="7dc7c-111">Especifique a estrutura de [**entryPoints**](entrypoints.md) para a função [**createprotocol**](createprotocol.md) e a variável de anexação global.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-111">Specify the [**ENTRYPOINTS**](entrypoints.md) structure for the [**CreateProtocol**](createprotocol.md) function and global Attach variable.</span></span> <span data-ttu-id="7dc7c-112">A variável de anexação é usada para rastrear o número de instâncias de protocolo que estão em execução.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-112">The Attach variable is used to track the number of protocol instances that are running.</span></span>
2.  <span data-ttu-id="7dc7c-113">Examine o valor do parâmetro de *comando* definido pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-113">Look at the value of the *Command* parameter that the operating system sets.</span></span>

    <span data-ttu-id="7dc7c-114">Se o parâmetro de *comando* for definido como dll do \_ processo \_ anexar e anexar for 0, chame [**createprotocol**](createprotocol.md) para fornecer o nome do protocolo e os pontos de entrada para as seguintes funções de exportação.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-114">If the *Command* parameter is set to DLL\_PROCESS\_ATTACH and Attach is 0, then call [**CreateProtocol**](createprotocol.md) to provide the protocol name and entry points for the following export functions.</span></span>

    -   <span data-ttu-id="7dc7c-115">**Registrar**</span><span class="sxs-lookup"><span data-stu-id="7dc7c-115">**Register**</span></span>
    -   <span data-ttu-id="7dc7c-116">**Cancelar registro**</span><span class="sxs-lookup"><span data-stu-id="7dc7c-116">**Deregister**</span></span>
    -   <span data-ttu-id="7dc7c-117">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="7dc7c-117">**RecognizeFrame**</span></span>
    -   <span data-ttu-id="7dc7c-118">**Anexarproperties**</span><span class="sxs-lookup"><span data-stu-id="7dc7c-118">**AttachProperties**</span></span>
    -   <span data-ttu-id="7dc7c-119">**Formatproperties** (obrigatório somente se monitor de rede exibir as propriedades de protocolo).</span><span class="sxs-lookup"><span data-stu-id="7dc7c-119">**FormatProperties** (only required if Network Monitor will be displaying the protocol properties).</span></span>

    <span data-ttu-id="7dc7c-120">Se o parâmetro de *comando* for definido como \_ dll \_ , desanexar e anexar é 0, chame [**DestroyProtocol**](destroyprotocol.md) usando o identificador de instância que o [**createprotocol**](createprotocol.md) retorna.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-120">If the *Command* parameter is set to DLL\_PROCESS\_DETACH and Attach is 0, then call [**DestroyProtocol**](destroyprotocol.md) using the instance handle that [**CreateProtocol**](createprotocol.md) returns.</span></span>

3.  <span data-ttu-id="7dc7c-121">Retornar **true** porque a função do analisador **DllMain** sempre deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-121">Return **TRUE** because the **DllMain** parser function must always return **TRUE**.</span></span>

<span data-ttu-id="7dc7c-122">A seguir está uma implementação básica do **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-122">The following is a basic implementation of **DllMain**.</span></span> <span data-ttu-id="7dc7c-123">O exemplo de código usa uma instrução Case para interceptar valores do parâmetro *Command* para determinar se [**createprotocol**](createprotocol.md) ou [**DestroyProtocol**](destroyprotocol.md) devem ser chamados.</span><span class="sxs-lookup"><span data-stu-id="7dc7c-123">The code example uses a case statement to trap values of the *Command* parameter to determine if [**CreateProtocol**](createprotocol.md) or [**DestroyProtocol**](destroyprotocol.md) should be called.</span></span>

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



