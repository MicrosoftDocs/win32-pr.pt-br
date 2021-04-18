---
description: Chama a função Attachproperties para mapear as propriedades que existem em uma parte dos dados reconhecidos.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implementando Anexaproperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787046"
---
# <a name="implementing-attachproperties"></a>Implementando Anexaproperties

Monitor de Rede chama a função [**attachproperties**](attachproperties.md) para mapear as propriedades que existem em uma parte dos dados reconhecidos. A função [**attachproperties**](attachproperties.md) mapeia as propriedades para um local específico.

Monitor de Rede usa o processo a seguir para analisar os dados em um quadro.

-   Primeiro, Monitor de Rede chama [RecognizeFrame](recognizeframe.md) para reconhecer todos os protocolos existentes em um quadro.
-   Em seguida, Monitor de Rede chama [**anexaproperties**](attachproperties.md) para cada analisador que reconhece uma parte dos dados.

Quando Monitor de Rede chama a função [attachproperties](attachproperties.md) para os dados reconhecidos, o analisador que é chamado deve analisar os dados e, em seguida, mapear cada propriedade existente para um local nos dados reconhecidos. O analisador determina quais propriedades existem e onde cada propriedade está localizada nos dados. A figura a seguir mostra dados reconhecidos pelo analisador.

![dados reconhecidos do analisador](images/attachproperties1.png)

Durante a implementação de [**attachproperties**](attachproperties.md), você deve chamar uma das funções a seguir para cada propriedade existente em um quadro de dados.

-   Chame a função [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) quando desejar modificar os dados de propriedade em um quadro.
-   Chame a função [**AttachPropertyInstance**](attachpropertyinstance.md) quando não quiser modificar os dados de propriedade em um quadro.

> [!Note]  
> É recomendável que você use os dados como eles existem na captura.

 

O procedimento a seguir identifica as etapas necessárias para implementar [**anexaproperties**](attachproperties.md).

**Para implementar Anexaproperties**

1.  Determine quais propriedades existem e o local da propriedade nos dados.
2.  Chame [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) para cada propriedade com um valor que você deseja modificar.
3.  Chame [**AttachPropertyInstance**](attachpropertyinstance.md) para cada propriedade com um valor que você não deseja modificar. Normalmente, essa é a única função que você precisa chamar.

A seguir está uma implementação básica de [**attachproperties**](attachproperties.md). Lembre-se de que o exemplo não inclui o código para determinar quais propriedades existem ou o código para localizar as propriedades.

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



