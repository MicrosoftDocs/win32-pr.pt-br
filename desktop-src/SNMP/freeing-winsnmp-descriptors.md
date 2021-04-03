---
title: Liberando descritores de WinSNMP
description: O ambiente de programação WinSNMP atribui a desalocação de recursos de descritor à implementação WinSNMP ou ao aplicativo WinSNMP, dependendo de qual componente aloca a memória para o descritor.
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97828c55d59932b7f4bdb75cbcf98964edd4a7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084862"
---
# <a name="freeing-winsnmp-descriptors"></a>Liberando descritores de WinSNMP

O ambiente de programação WinSNMP atribui a desalocação de recursos de descritor à implementação WinSNMP ou ao aplicativo WinSNMP, dependendo de qual componente aloca a memória para o descritor.

Para liberar os recursos para um descritor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , as seguintes regras se aplicam:

-   Para parâmetros de entrada

    Como o aplicativo WinSNMP aloca a memória para objetos de entrada com comprimentos variáveis, o aplicativo deve liberar essa memória usando uma função apropriada. Por exemplo, se o aplicativo alocou os recursos com uma chamada para a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) , ele deve usar a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) para desalocar os recursos. Se o aplicativo alocou os recursos com uma chamada para a função [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) , ele deve chamar a função [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree) .

-   Para parâmetros de saída

    Uma chamada para qualquer uma das seguintes funções resulta na implementação Alocando memória para um descritor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) : [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb), [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg), [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy), [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)e [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid).

    Como a implementação aloca a memória para esses objetos de saída, o aplicativo deve chamar a função [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desalocar os recursos. Essa função permite que a implementação libere a memória alocada para o membro **PTR** dessas estruturas.

Para liberar os recursos para uma estrutura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) , um aplicativo WinSNMP deve verificar o membro da **sintaxe** de uma estrutura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) para avaliar corretamente o membro **Value** da estrutura. Se o membro de **sintaxe** indicar que o membro de **valor** é um descritor [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) ou [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) e a implementação alocou os recursos para o descritor, o aplicativo deverá chamar [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor). Isso permite que a implementação libere a memória. Se o aplicativo alocou os recursos, ele deve liberar a memória usando uma função apropriada, conforme indicado anteriormente.

Para obter mais informações, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).

 

 