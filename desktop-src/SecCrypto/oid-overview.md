---
description: A extensibilidade é obtida fornecendo-se o uso de novos identificadores de objeto (OIDs), novos tipos de codificação e novas DLLs.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Visão geral de OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85251fa2f7084a2c0a4f691216592edaba79109af4c7651de54764a802642c90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979891"
---
# <a name="oid-overview"></a>Visão geral de OID

A extensibilidade é obtida fornecendo-se o uso de novos [*identificadores de objeto*](../secgloss/o-gly.md) (OIDs), novos tipos de codificação e novas DLLs.

Os OIDs de CryptoAPI podem ter qualquer uma das seguintes formas:

-   Uma cadeia de caracteres numérica, como "1.2.3.500.88"
-   Uma cadeia de caracteres alfanumérica, como *MyFunction*
-   Uma constante com um valor menor ou igual a 0xFFFF. Essas constantes geralmente são associadas a um nome por meio do uso de uma instrução de **\# definição** em um arquivo de cabeçalho.

As funções extensíveis aceitam argumentos de tipo OID e Encoding. Essas funções pesquisam o registro do sistema para localizar uma DLL associada aos argumentos de OID e tipo de codificação passados para a função. Se uma DLL para a OID, a combinação de tipo de codificação for encontrada, a DLL será carregada e sua função será chamada. A ilustração a seguir mostra esse fluxo para a função [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :

![fluxo de OID](images/oidflow.png)

Isso permite que a funcionalidade da CryptoAPI seja estendida conforme a necessidade. O uso dessa metodologia impõe um fardo no desenvolvedor da nova funcionalidade para gravar todo o código necessário para essa funcionalidade. Para codificar uma nova estrutura de dados, por exemplo, a função na DLL deve executar todo o processo de codificação.

 

 
