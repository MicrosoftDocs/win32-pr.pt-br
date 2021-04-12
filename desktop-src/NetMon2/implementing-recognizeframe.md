---
description: Os monitores de rede chamam a função RecognizeFrame de um analisador para determinar se o analisador reconhece os dados não reivindicados de um quadro.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementando RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297438"
---
# <a name="implementing-recognizeframe"></a><span data-ttu-id="caba7-103">Implementando RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="caba7-103">Implementing RecognizeFrame</span></span>

<span data-ttu-id="caba7-104">Os monitores de rede chamam a função [**RecognizeFrame**](recognizeframe.md) de um analisador para determinar se o analisador reconhece os dados não reivindicados de um quadro.</span><span class="sxs-lookup"><span data-stu-id="caba7-104">Network Monitors calls the [**RecognizeFrame**](recognizeframe.md) function of a parser to determine that the parser recognizes the unclaimed data of a frame.</span></span> <span data-ttu-id="caba7-105">Os dados não reivindicados podem estar no início de um quadro, mas normalmente os dados não reivindicados estão localizados no meio de um quadro.</span><span class="sxs-lookup"><span data-stu-id="caba7-105">The unclaimed data may be at the start of a frame, but typically, unclaimed data is located in the middle of a frame.</span></span> <span data-ttu-id="caba7-106">A ilustração a seguir mostra os dados não reivindicados localizados no meio de um quadro.</span><span class="sxs-lookup"><span data-stu-id="caba7-106">The following illustration shows unclaimed data located in the middle of a frame.</span></span>

![dados não reivindicados localizados no meio de um quadro](images/recognizeframe1.png)

<span data-ttu-id="caba7-108">Monitor de Rede fornece as seguintes informações ao chamar a função [**RecognizeFrame**](recognizeframe.md) :</span><span class="sxs-lookup"><span data-stu-id="caba7-108">Network Monitor provides the following information when it calls the [**RecognizeFrame**](recognizeframe.md) function:</span></span>

-   <span data-ttu-id="caba7-109">Um identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="caba7-109">A handle to the frame.</span></span>
-   <span data-ttu-id="caba7-110">Um ponteiro para o início do quadro.</span><span class="sxs-lookup"><span data-stu-id="caba7-110">A pointer to the start of the frame.</span></span>
-   <span data-ttu-id="caba7-111">Um ponteiro para o início dos dados não reivindicados.</span><span class="sxs-lookup"><span data-stu-id="caba7-111">A pointer to the start of the unclaimed data.</span></span>
-   <span data-ttu-id="caba7-112">O valor MAC do primeiro protocolo no quadro.</span><span class="sxs-lookup"><span data-stu-id="caba7-112">The MAC value of the first protocol in the frame.</span></span>
-   <span data-ttu-id="caba7-113">O número de bytes nos dados não reivindicados; ou seja, os bytes restantes no quadro.</span><span class="sxs-lookup"><span data-stu-id="caba7-113">The number of bytes in the unclaimed data; that is, the bytes remaining in the frame.</span></span>
-   <span data-ttu-id="caba7-114">Um identificador para o protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="caba7-114">A handle to the previous protocol.</span></span>
-   <span data-ttu-id="caba7-115">O deslocamento do protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="caba7-115">The offset of the previous protocol.</span></span>

<span data-ttu-id="caba7-116">Quando a DLL do analisador determina que os dados não reivindicados começam com o protocolo do analisador, a DLL do analisador determina o local em que o próximo protocolo começa e o seguinte protocolo.</span><span class="sxs-lookup"><span data-stu-id="caba7-116">When the parser DLL determines that unclaimed data starts with the parser protocol, the parser DLL determines where the next protocol starts, and which protocol follows.</span></span> <span data-ttu-id="caba7-117">A DLL do analisador funciona nas seguintes maneiras condicionais:</span><span class="sxs-lookup"><span data-stu-id="caba7-117">The parser DLL functions in the following conditional ways:</span></span>

-   <span data-ttu-id="caba7-118">Se a DLL do analisador reconhecer dados não reivindicados, a DLL do analisador definirá o parâmetro *pProtocolStatus* e retornará um ponteiro para o próximo protocolo no quadro, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="caba7-118">If the parser DLL recognizes unclaimed data, the parser DLL sets the *pProtocolStatus* parameter, and returns a pointer to either the next protocol in the frame, or **NULL**.</span></span> <span data-ttu-id="caba7-119">**NULL** será retornado se o protocolo atual for o último protocolo no quadro.</span><span class="sxs-lookup"><span data-stu-id="caba7-119">**NULL** is returned if the current protocol is the last protocol in the frame.</span></span>
-   <span data-ttu-id="caba7-120">Se a DLL do analisador reconhecer dados não reivindicados e identificar o protocolo a seguir (das informações fornecidas no protocolo), a DLL do analisador retornará um ponteiro para o identificador do próximo protocolo no parâmetro *phNextProtocol* da função.</span><span class="sxs-lookup"><span data-stu-id="caba7-120">If the parser DLL recognizes unclaimed data and identifies the protocol that follows (from information provided in the protocol), then the parser DLL returns a pointer to the handle of the next protocol in the *phNextProtocol* parameter of the function.</span></span>
-   <span data-ttu-id="caba7-121">Se a DLL do analisador não reconhecer dados não reivindicados, a DLL do analisador retornará o ponteiro para o início de dados não reivindicados e Monitor de Rede continuará tentando analisar os dados não reivindicados.</span><span class="sxs-lookup"><span data-stu-id="caba7-121">If the parser DLL does not recognize unclaimed data, the parser DLL returns the pointer to the start of unclaimed data, and Network Monitor continues trying to parse the unclaimed data.</span></span>

<span data-ttu-id="caba7-122">**Para implementar o RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="caba7-122">**To implement RecognizeFrame**</span></span>

1.  <span data-ttu-id="caba7-123">Teste para determinar se você reconhece o protocolo.</span><span class="sxs-lookup"><span data-stu-id="caba7-123">Test to determine that you recognize the protocol.</span></span>
2.  <span data-ttu-id="caba7-124">Se você reconhece dados não reivindicados e sabe qual protocolo segue, defina *pProtocolStatus* como protocolo do \_ próximo protocolo do status \_ \_ , defina *phNextProtocol* como um ponteiro que aponte para o identificador do próximo protocolo e, em seguida, retorne um ponteiro para o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="caba7-124">If you recognize unclaimed data and you know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_NEXT\_PROTOCOL, set *phNextProtocol* to a pointer that points to the handle for the next protocol, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="caba7-125">–ou–</span><span class="sxs-lookup"><span data-stu-id="caba7-125">–or–</span></span>

    <span data-ttu-id="caba7-126">Se você reconhece dados não reivindicados e não sabe qual protocolo segue, defina *pProtocolStatus* para status de protocolo \_ \_ reconhecido e, em seguida, retorne um ponteiro para o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="caba7-126">If you recognize unclaimed data and you do not know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_RECOGNIZED, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="caba7-127">–ou–</span><span class="sxs-lookup"><span data-stu-id="caba7-127">–or–</span></span>

    <span data-ttu-id="caba7-128">Se você reconhece dados não reivindicados e seu protocolo é o último protocolo em um quadro, defina *pProtocolStatus* para status de protocolo \_ \_ declarado e, em seguida, retorne **nulo**.</span><span class="sxs-lookup"><span data-stu-id="caba7-128">If you recognize unclaimed data and your protocol is the last protocol in a frame, set *pProtocolStatus* to PROTOCOL\_STATUS\_CLAIMED, and then return **NULL**.</span></span>

    <span data-ttu-id="caba7-129">–ou–</span><span class="sxs-lookup"><span data-stu-id="caba7-129">–or–</span></span>

    <span data-ttu-id="caba7-130">Se você não reconhecer dados não reivindicados, defina *pProtocolStatus* como status de \_ protocolo \_ não \_ reconhecido e, em seguida, retorne o ponteiro que é passado para você em *pProtocol*.</span><span class="sxs-lookup"><span data-stu-id="caba7-130">If you do not recognize unclaimed data, set *pProtocolStatus* to PROTOCOL\_STATUS\_NOT\_RECOGNIZED, and then return the pointer that is passed to you in *pProtocol*.</span></span>

<span data-ttu-id="caba7-131">Veja a seguir uma implementação básica do [**RecognizeFrame**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="caba7-131">The following is a basic implementation of [**RecognizeFrame**](recognizeframe.md).</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



