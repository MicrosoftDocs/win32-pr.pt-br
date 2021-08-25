---
description: Monitor de Rede usa a função de exportação ParserAutoInstallInfo para instalar um analisador. Quando ParserAutoInstallInfo é chamado, o analisador retorna uma estrutura de PARSERDLLINFO de PF \_ que contém todas as informações que monitor de rede precisa para instalar uma DLL do analisador.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implementando ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d1c797f53ad110392fea304cc0a610fdb0f9346c745e2f7dea2bff16208e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743076"
---
# <a name="implementing-parserautoinstallinfo"></a>Implementando ParserAutoInstallInfo

Monitor de Rede usa a função de exportação [**ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar um analisador. Quando **ParserAutoInstallInfo** é chamado, o analisador retorna uma estrutura de [**\_ PARSERDLLINFO de PF**](pf-parserdllinfo.md) que contém todas as informações que monitor de rede precisa para instalar uma DLL do analisador.

> [!Note]  
> Monitor de Rede mantém uma lista de analisadores existentes no arquivo [*Parser.ini*](p.md) e cria um arquivo ini separado para cada analisador instalado.

 

Durante o processo de instalação, a DLL do analisador deve identificar o seguinte:

-   O número de analisadores na DLL — incluindo um nome e uma descrição de comentário para cada analisador.
-   Os protocolos que precedem o protocolo analisador.
-   Os protocolos que seguem o protocolo do analisador.

> [!Note]  
> Monitor de Rede usa as informações do protocolo analisador anterior e seguinte para atualizar os [*conjuntos de entrega*](h.md) e seguir os [*conjuntos*](f.md) de analisadores identificados pela DLL do analisador.

 

O procedimento a seguir identifica as etapas necessárias para implementar o [**ParserAutoInstallInfo**](parserautoinstallinfo.md).

**Para implementar o ParserAutoInstallInfo**

1.  Aloque uma estrutura de [**\_ PARSERDLLINFO de PF**](pf-parserdllinfo.md) usando **HeapAlloc**.
2.  Retornar memória para o heap usando **HeapFree**.
3.  Lembre-se de que essa chamada também deve alocar uma estrutura de [**PF \_ PARSERINFO**](pf-parserinfo.md) para cada analisador na dll.
4.  Especifique o número de analisadores (normalmente um) que a DLL contém no membro **nParsers** de [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).
5.  Especifique um nome, comentário e arquivo de ajuda opcional nos membros **szProtocolName**, **szComment** e **szHelpFile** de cada estrutura de [**\_ PARSERINFO de PF**](pf-parserinfo.md) .
6.  Especifique os protocolos que precedem cada protocolo DLL. Uma das condições a seguir se aplica a um conjunto de entregas de entrada.
    -   Se os protocolos anteriores puderem determinar que o protocolo segue dos dados nos protocolos anteriores, defina o membro **pWhoHandsOffToMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). Nesse caso, o protocolo é então adicionado aos conjuntos de [*entrega*](h.md) dos protocolos anteriores.
    -   Se os protocolos anteriores não puderem determinar que o protocolo segue dos dados nos protocolos anteriores, defina membro **pWhoCanPrecedeMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). Nesse caso, o protocolo é então adicionado aos conjuntos de protocolos a [*seguir*](f.md) .
7.  Especifique os protocolos que seguem cada protocolo de DLL. Uma das condições a seguir se aplica a um conjunto de acompanhamento de saída.
    -   Se o protocolo puder determinar quais protocolos seguem com base nos dados em seu protocolo, defina o membro **pWhoDoIHandOffTo** de [**PF \_ PARSERINFO**](pf-parserinfo.md). Nesse caso, esses protocolos são adicionados ao [*conjunto de entrega*](h.md) de seus protocolos.
    -   Se o protocolo não puder determinar quais protocolos seguem com base nos dados em seu protocolo, defina o membro **pWhoCanFollowMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). Nesse caso, esses protocolos são adicionados ao conjunto de [*acompanhamento*](f.md) do seu protocolo.
8.  Retorne a estrutura de [**\_ PARSERDLLINFO do PF**](pf-parserdllinfo.md) para monitor de rede.

Veja a seguir uma implementação básica do [**ParserAutoInstallInfo**](parserautoinstallinfo.md). O exemplo de código é obtido do analisador genérico que o Monitor de Rede fornece.

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

 

 



