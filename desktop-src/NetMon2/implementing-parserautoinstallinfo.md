---
description: Monitor de Rede usa a função de exportação ParserAutoInstallInfo para instalar um analisador. Quando ParserAutoInstallInfo é chamado, o analisador retorna uma estrutura de PARSERDLLINFO de PF \_ que contém todas as informações que monitor de rede precisa para instalar uma DLL do analisador.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implementando ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d79a9ba5036673acb076be9f3634dae7556b5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810296"
---
# <a name="implementing-parserautoinstallinfo"></a><span data-ttu-id="5be95-104">Implementando ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="5be95-104">Implementing ParserAutoInstallInfo</span></span>

<span data-ttu-id="5be95-105">Monitor de Rede usa a função de exportação [**ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar um analisador.</span><span class="sxs-lookup"><span data-stu-id="5be95-105">Network Monitor uses the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export function to install a parser.</span></span> <span data-ttu-id="5be95-106">Quando **ParserAutoInstallInfo** é chamado, o analisador retorna uma estrutura de [**\_ PARSERDLLINFO de PF**](pf-parserdllinfo.md) que contém todas as informações que monitor de rede precisa para instalar uma DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="5be95-106">When **ParserAutoInstallInfo** is called, the parser returns a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure containing all the information that Network Monitor needs to install a parser DLL.</span></span>

> [!Note]  
> <span data-ttu-id="5be95-107">Monitor de Rede mantém uma lista de analisadores existentes no arquivo [*Parser.ini*](p.md) e cria um arquivo ini separado para cada analisador instalado.</span><span class="sxs-lookup"><span data-stu-id="5be95-107">Network Monitor keeps a list of existing parsers in the [*Parser.ini*](p.md) file, and creates a separate INI file for each installed parser.</span></span>

 

<span data-ttu-id="5be95-108">Durante o processo de instalação, a DLL do analisador deve identificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5be95-108">During the installation process, the parser DLL must identify the following:</span></span>

-   <span data-ttu-id="5be95-109">O número de analisadores na DLL — incluindo um nome e uma descrição de comentário para cada analisador.</span><span class="sxs-lookup"><span data-stu-id="5be95-109">The number of parsers in the DLL—including a name and comment description for each parser.</span></span>
-   <span data-ttu-id="5be95-110">Os protocolos que precedem o protocolo analisador.</span><span class="sxs-lookup"><span data-stu-id="5be95-110">The protocols that precede the parser protocol.</span></span>
-   <span data-ttu-id="5be95-111">Os protocolos que seguem o protocolo do analisador.</span><span class="sxs-lookup"><span data-stu-id="5be95-111">The protocols that follow the parser protocol.</span></span>

> [!Note]  
> <span data-ttu-id="5be95-112">Monitor de Rede usa as informações do protocolo analisador anterior e seguinte para atualizar os [*conjuntos de entrega*](h.md) e seguir os [*conjuntos*](f.md) de analisadores identificados pela DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="5be95-112">Network Monitor uses the preceding and following parser protocol information to update the [*handoff sets*](h.md) and [*follow sets*](f.md) of parsers that your parser DLL identifies.</span></span>

 

<span data-ttu-id="5be95-113">O procedimento a seguir identifica as etapas necessárias para implementar o [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5be95-113">The following procedure identifies the steps necessary to implement [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span>

<span data-ttu-id="5be95-114">**Para implementar o ParserAutoInstallInfo**</span><span class="sxs-lookup"><span data-stu-id="5be95-114">**To implement ParserAutoInstallInfo**</span></span>

1.  <span data-ttu-id="5be95-115">Aloque uma estrutura de [**\_ PARSERDLLINFO de PF**](pf-parserdllinfo.md) usando **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="5be95-115">Allocate a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure using **HeapAlloc**.</span></span>
2.  <span data-ttu-id="5be95-116">Retornar memória para o heap usando **HeapFree**.</span><span class="sxs-lookup"><span data-stu-id="5be95-116">Return memory to the heap using **HeapFree**.</span></span>
3.  <span data-ttu-id="5be95-117">Lembre-se de que essa chamada também deve alocar uma estrutura de [**PF \_ PARSERINFO**](pf-parserinfo.md) para cada analisador na dll.</span><span class="sxs-lookup"><span data-stu-id="5be95-117">Be aware that this call must also allocate a [**PF\_PARSERINFO**](pf-parserinfo.md) structure for each parser in the DLL.</span></span>
4.  <span data-ttu-id="5be95-118">Especifique o número de analisadores (normalmente um) que a DLL contém no membro **nParsers** de [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5be95-118">Specify the number of parsers (typically one) that the DLL contains in the **nParsers** member of [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md).</span></span>
5.  <span data-ttu-id="5be95-119">Especifique um nome, comentário e arquivo de ajuda opcional nos membros **szProtocolName**, **szComment** e **szHelpFile** de cada estrutura de [**\_ PARSERINFO de PF**](pf-parserinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="5be95-119">Specify a name, comment, and optional Help file in the **szProtocolName**, **szComment**, and **szHelpFile** members of each [**PF\_PARSERINFO**](pf-parserinfo.md) structure.</span></span>
6.  <span data-ttu-id="5be95-120">Especifique os protocolos que precedem cada protocolo DLL.</span><span class="sxs-lookup"><span data-stu-id="5be95-120">Specify the protocols that precede each DLL protocol.</span></span> <span data-ttu-id="5be95-121">Uma das condições a seguir se aplica a um conjunto de entregas de entrada.</span><span class="sxs-lookup"><span data-stu-id="5be95-121">One of the following conditions applies to an incoming handoff set.</span></span>
    -   <span data-ttu-id="5be95-122">Se os protocolos anteriores puderem determinar que o protocolo segue dos dados nos protocolos anteriores, defina o membro **pWhoHandsOffToMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5be95-122">If the preceding protocols can determine that your protocol follows from data in the preceding protocols, set the **pWhoHandsOffToMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="5be95-123">Nesse caso, o protocolo é então adicionado aos conjuntos de [*entrega*](h.md) dos protocolos anteriores.</span><span class="sxs-lookup"><span data-stu-id="5be95-123">In this case, your protocol is then added to the [*handoff sets*](h.md) of the preceding protocols.</span></span>
    -   <span data-ttu-id="5be95-124">Se os protocolos anteriores não puderem determinar que o protocolo segue dos dados nos protocolos anteriores, defina membro **pWhoCanPrecedeMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5be95-124">If the preceding protocols cannot determine that your protocol follows from data in the preceding protocols, set **pWhoCanPrecedeMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="5be95-125">Nesse caso, o protocolo é então adicionado aos conjuntos de protocolos a [*seguir*](f.md) .</span><span class="sxs-lookup"><span data-stu-id="5be95-125">In this case, the your protocol is then added to the [*follow sets*](f.md) of the protocols.</span></span>
7.  <span data-ttu-id="5be95-126">Especifique os protocolos que seguem cada protocolo de DLL.</span><span class="sxs-lookup"><span data-stu-id="5be95-126">Specify the protocols that follow each DLL protocol.</span></span> <span data-ttu-id="5be95-127">Uma das condições a seguir se aplica a um conjunto de acompanhamento de saída.</span><span class="sxs-lookup"><span data-stu-id="5be95-127">One of the following conditions applies to an outgoing follow-set.</span></span>
    -   <span data-ttu-id="5be95-128">Se o protocolo puder determinar quais protocolos seguem com base nos dados em seu protocolo, defina o membro **pWhoDoIHandOffTo** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5be95-128">If your protocol can determine which protocols follow based on data in your protocol, set the **pWhoDoIHandOffTo** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="5be95-129">Nesse caso, esses protocolos são adicionados ao [*conjunto de entrega*](h.md) de seus protocolos.</span><span class="sxs-lookup"><span data-stu-id="5be95-129">In this case, the these protocols are added to the [*handoff set*](h.md) of your protocols.</span></span>
    -   <span data-ttu-id="5be95-130">Se o protocolo não puder determinar quais protocolos seguem com base nos dados em seu protocolo, defina o membro **pWhoCanFollowMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5be95-130">If your protocol cannot determine which protocols follow based on data in your protocol, set the **pWhoCanFollowMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="5be95-131">Nesse caso, esses protocolos são adicionados ao conjunto de [*acompanhamento*](f.md) do seu protocolo.</span><span class="sxs-lookup"><span data-stu-id="5be95-131">In this case, these protocols are added to the [*follow set*](f.md) of your protocol.</span></span>
8.  <span data-ttu-id="5be95-132">Retorne a estrutura de [**\_ PARSERDLLINFO do PF**](pf-parserdllinfo.md) para monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="5be95-132">Return the [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure to Network Monitor.</span></span>

<span data-ttu-id="5be95-133">Veja a seguir uma implementação básica do [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5be95-133">The following is a basic implementation of [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span> <span data-ttu-id="5be95-134">O exemplo de código é obtido do analisador genérico que o Monitor de Rede fornece.</span><span class="sxs-lookup"><span data-stu-id="5be95-134">The code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo() 
{

  /////////////////////////////////////////////////////////////////
  //
  // Allocate memory for PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  PPF_PARSERDLLINFO pParserDllInfo; 
  PPF_PARSERINFO    pParserInfo;
  DWORD NumProtocols;
        DWORD NumParsers;
        DWORD NumFollows;
  NumParsers = 1;
  
  pParserDllInfo = (PPF_PARSERDLLINFO)HeapAlloc( GetProcessHeap(),
                                                 HEAP_ZERO_MEMORY,
                                                 sizeof( PF_PARSERDLLINFO ) +
                                                 NumParsers * sizeof( PF_PARSERINFO) );
  if( pParserDllInfo == NULL)
  {
    return NULL;
  }
  

    
  /////////////////////////////////////////////////////////////////
  //
  // Specify the number of parsers in the DLL.
  //
  /////////////////////////////////////////////////////////////////
  
  pParserDllInfo->nParsers = NumParsers;
  

  /////////////////////////////////////////////////////////////////
  // 
  // Specify the name, comment, and Help file for each protocol.
  // 
  /////////////////////////////////////////////////////////////////
  pParserInfo = &(pParserDllInfo->ParserInfo[0]);
  sprintf_s( pParserInfo->szProtocolName, MAX_PROTOCOL_NAME_LEN, 
    "TestProtocol" );
  sprintf_s( pParserInfo->szComment, MAX_PROTOCOL_COMMENT_LEN,
    "Test protocol for SDK" );
  sprintf_s( pParserInfo->szHelpFile, MAX_PATH, "");
  

  
  /////////////////////////////////////////////////////////////////
  //
  // Specify preceding protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_HANDOFFSET    pHandoffSet;
  PPF_HANDOFFENTRY  pHandoffEntry;
  
  // Allocate PF_HANDOFFSET structure.
  NumHandoffs = 1;                   
  pHandoffSet = (PPF_HANDOFFSET)HeapAlloc( GetProcessHeap(),
                                           HEAP_ZERO_MEMORY,
                                           sizeof( PF_HANDOFFSET ) +
                                           NumHandoffs * sizeof( PF_HANDOFFENTRY) );
  if( pHandoffSet == NULL )
  {
     return pParserDllInfo;
  }

  // Fill in handoff set
  pParserInfo->pWhoHandsOffToMe = pHandoffSet;
  pHandoffSet->nEntries = NumHandoffs;

  // TCP PORT FFFF
  pHandoffEntry = &(pHandoffSet->Entry[0]);
  sprintf_s( pHandoffEntry->szIniFile, MAX_PATH, "TCPIP.INI" );
  sprintf_s( pHandoffEntry->szIniSection, MAX_PATH, "TCP_HandoffSet" );
  sprintf_s( pHandoffEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, 
    "BLRPLATE" );
  pHandoffEntry->dwHandOffValue =        0xFFFF;
  pHandoffEntry->ValueFormatBase =       HANDOFF_VALUE_FORMAT_BASE_DECIMAL;    
  
  

  /////////////////////////////////////////////////////////////////
  //
  // Specify the following protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_FOLLOWSET     pFollowSet;
  PPF_FOLLOWENTRY   pFollowEntry;
 
  // Allocate PF_FOLLOWSET structure
  NumFollows = 1;
  pFollowSet = (PPF_FOLLOWSET)HeapAlloc( GetProcessHeap(),
                                         HEAP_ZERO_MEMORY,
                                         sizeof( PF_FOLLOWSET ) +
                                         NumFollows * sizeof( PF_FOLLOWENTRY) );
  if( pFollowSet == NULL )
  {
    return pParserDllInfo;
  }

  // Fill in the follow set
  pParserInfo->pWhoCanFollowMe = pFollowSet;
  pFollowSet->nEntries = NumFollows;

  // Add SMB
  pFollowEntry = &(pFollowSet->Entry[0]);
  sprintf_s( pFollowEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, "SMB" );
  


  /////////////////////////////////////////////////////////////////
  //
  // Return the PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  return pParserDllInfo;

}
```

 

 



