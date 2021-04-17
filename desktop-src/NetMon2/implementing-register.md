---
description: Monitor de Rede carrega uma captura do arquivo de captura e, em seguida, começa a chamar a função de registro para todos os protocolos que ele pode identificar. Cada DLL do analisador deve implementar uma função de registro para cada protocolo compatível com a DLL do analisador.
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: Implementando o registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59f34f5f97925627184db7188aac0a9eb796a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768701"
---
# <a name="implementing-register"></a>Implementando o registro

Monitor de Rede carrega uma captura do arquivo de captura e, em seguida, começa a chamar a função de [**registro**](register-parser.md) para todos os protocolos que ele pode identificar. Cada DLL do analisador deve implementar uma função de **registro** para cada protocolo compatível com a DLL do analisador.

Cada implementação da função de [**registro**](register-parser.md) deve chamar as funções [**CreatePropertyDatabase**](createpropertydatabase.md) e [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) para criar e preencher o banco de [*dados de propriedades*](p.md) para o protocolo e, em seguida, [**createentregatable**](createhandofftable.md) para criar a [*tabela de entrega*](h.md) para o protocolo, se necessário.

> [!Note]  
> As propriedades de protocolo são definidas para Monitor de Rede. As propriedades não são mapeadas para um local em dados de captura até que a função de exportação [**anexaproperties**](attachproperties.md) seja chamada.

 

O procedimento a seguir identifica as etapas necessárias para implementar a função de [**registro**](register-parser.md) .

**Para implementar o registro para um protocolo**

1.  Defina uma matriz de estruturas [**PROPERTYINFO**](propertyinfo.md) para descrever cada propriedade que o protocolo suporta.
2.  Chame [**CreatePropertyDatabase**](createpropertydatabase.md) para fornecer um identificador de protocolo e o número de propriedades que o protocolo suporta.
3.  Chame [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) em um loop para adicionar cada propriedade definida na matriz de estrutura [**PROPERTYINFO**](propertyinfo.md) .
4.  Se o protocolo usar uma tabela de entrega, chame [**Createentregatable**](createhandofftable.md)— depois que todas as propriedades do protocolo forem adicionadas ao banco de dados de propriedades.

A seguir está uma implementação básica do [**registro**](register-parser.md). Observe que um banco de dados de propriedade é criado para um protocolo que dá suporte apenas a duas propriedades. Este exemplo de código é obtido do analisador genérico que o Monitor de Rede fornece.

``` syntax
#include <windows.h>

PROPERTYINFO MyProtocolPropertyTable[]
{
  // Summary property (0)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "Summary",                       // Property label.
     "Summary of protocol packet",    // Property comment.
     PROP_TYPE_SUMMARY,               // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

  // WORD property (1)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "WORD property",                 // Property label.
     "16-bit WORD property",         // Property comment.
     PROP_TYPE_WORD,                  // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

}

void BHAPI MyProtocolRegister( HPPROTOCOL hProtocol) 
{
  // Create property database.
  DWORD dwNumberOfProperties = 2;
  CreatePropertyDatabase (hProtocol,
                          dwNumberOfProperties
                          );
  
  // Add properties to database.
  WORD i;
  for( i=0; i< dwNumberOfProperties; i++)
  {
     AddProperty(hProtocol, &MyProtocolPropertyTable[i]);
  }

  // Create handoff table.
  CreateHandoffTable("myProtocolHandoffTable",
                          "myProtocol.ini",
                           hTable,
                           MaxEntries,
                           10       // Handoff set values are base 10.
                          )
}
```

 

 
