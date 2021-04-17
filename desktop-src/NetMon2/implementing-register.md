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
# <a name="implementing-register"></a><span data-ttu-id="bf7b2-104">Implementando o registro</span><span class="sxs-lookup"><span data-stu-id="bf7b2-104">Implementing Register</span></span>

<span data-ttu-id="bf7b2-105">Monitor de Rede carrega uma captura do arquivo de captura e, em seguida, começa a chamar a função de [**registro**](register-parser.md) para todos os protocolos que ele pode identificar.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-105">Network Monitor loads a capture from the capture file, and then starts calling the [**Register**](register-parser.md) function for all the protocols that it can identify.</span></span> <span data-ttu-id="bf7b2-106">Cada DLL do analisador deve implementar uma função de **registro** para cada protocolo compatível com a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-106">Each parser DLL must implement a **Register** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="bf7b2-107">Cada implementação da função de [**registro**](register-parser.md) deve chamar as funções [**CreatePropertyDatabase**](createpropertydatabase.md) e [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) para criar e preencher o banco de [*dados de propriedades*](p.md) para o protocolo e, em seguida, [**createentregatable**](createhandofftable.md) para criar a [*tabela de entrega*](h.md) para o protocolo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-107">Each implementation of the [**Register**](register-parser.md) function must call the [**CreatePropertyDatabase**](createpropertydatabase.md) and [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) functions to create and fill-in the [*property database*](p.md) for the protocol, and then the [**CreateHandoffTable**](createhandofftable.md) to create the [*handoff table*](h.md) for the protocol — if needed.</span></span>

> [!Note]  
> <span data-ttu-id="bf7b2-108">As propriedades de protocolo são definidas para Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-108">Protocol properties are defined for Network Monitor.</span></span> <span data-ttu-id="bf7b2-109">As propriedades não são mapeadas para um local em dados de captura até que a função de exportação [**anexaproperties**](attachproperties.md) seja chamada.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-109">Properties are not mapped to a location in a capture data until the [**AttachProperties**](attachproperties.md) export function is called.</span></span>

 

<span data-ttu-id="bf7b2-110">O procedimento a seguir identifica as etapas necessárias para implementar a função de [**registro**](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="bf7b2-110">The following procedure identifies the steps necessary to implement the [**Register**](register-parser.md) function.</span></span>

<span data-ttu-id="bf7b2-111">**Para implementar o registro para um protocolo**</span><span class="sxs-lookup"><span data-stu-id="bf7b2-111">**To implement Register for one protocol**</span></span>

1.  <span data-ttu-id="bf7b2-112">Defina uma matriz de estruturas [**PROPERTYINFO**](propertyinfo.md) para descrever cada propriedade que o protocolo suporta.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-112">Define an array of [**PROPERTYINFO**](propertyinfo.md) structures to describe each property that the protocol supports.</span></span>
2.  <span data-ttu-id="bf7b2-113">Chame [**CreatePropertyDatabase**](createpropertydatabase.md) para fornecer um identificador de protocolo e o número de propriedades que o protocolo suporta.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-113">Call [**CreatePropertyDatabase**](createpropertydatabase.md) to provide a protocol handle, and the number of properties that the protocol supports.</span></span>
3.  <span data-ttu-id="bf7b2-114">Chame [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) em um loop para adicionar cada propriedade definida na matriz de estrutura [**PROPERTYINFO**](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="bf7b2-114">Call [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in a loop to add each property defined in the [**PROPERTYINFO**](propertyinfo.md) structure array.</span></span>
4.  <span data-ttu-id="bf7b2-115">Se o protocolo usar uma tabela de entrega, chame [**Createentregatable**](createhandofftable.md)— depois que todas as propriedades do protocolo forem adicionadas ao banco de dados de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-115">If the protocol uses a handoff table, call [**CreateHandoffTable**](createhandofftable.md)— after all the properties of the protocol are added to the property database.</span></span>

<span data-ttu-id="bf7b2-116">A seguir está uma implementação básica do [**registro**](register-parser.md).</span><span class="sxs-lookup"><span data-stu-id="bf7b2-116">The following is a basic implementation of [**Register**](register-parser.md).</span></span> <span data-ttu-id="bf7b2-117">Observe que um banco de dados de propriedade é criado para um protocolo que dá suporte apenas a duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-117">Note that a property database is created for a protocol that supports only two properties.</span></span> <span data-ttu-id="bf7b2-118">Este exemplo de código é obtido do analisador genérico que o Monitor de Rede fornece.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-118">This code example is taken from the generic parser that Network Monitor provides.</span></span>

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

 

 
