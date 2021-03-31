---
title: atributo de cadeia de caracteres (RPC)
description: O atributo \ String \ e a chamada de procedimento remoto (RPC).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e413c0b3b8f5a379dc3448f07aed4a5a7a6aba07
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917580"
---
# <a name="string-attribute-rpc"></a>atributo de cadeia de caracteres (RPC)

O \[ [](/windows/desktop/Midl/string) \] atributo String indica que o parâmetro é um ponteiro para uma matriz do tipo [Char](/windows/desktop/Midl/char-idl), [byte](/windows/desktop/Midl/byte)ou **w \_ Char**. Assim como com uma matriz compatível, o tamanho de um parâmetro de **\[ cadeia de caracteres \]** é determinado em tempo de execução. Ao contrário de uma matriz compatível, o desenvolvedor não precisa fornecer o comprimento associado à matriz – o atributo de **\[ cadeia de \] caracteres** informa ao stub para determinar o tamanho da matriz chamando **strlen**. Um atributo de **\[ cadeia de \] caracteres** não pode ser usado ao mesmo tempo que o \[ [comprimento \_](/windows/desktop/Midl/length-is) \] ou o \[ [último \_ são](/windows/desktop/Midl/last-is) \] atributos.

O **\[ no, \]** a combinação de atributos de cadeia de caracteres direciona o stub para passar a cadeia de caracteres do cliente para o servidor somente. A quantidade de memória alocada no servidor é igual ao tamanho da cadeia de caracteres transmitida mais uma.

Os \[ atributos [out](/windows/desktop/Midl/out-idl), **String** \] direcionam o stub para passar a cadeia de caracteres do servidor para o cliente somente. O design de chamada por valor da linguagem C insiste que todos os parâmetros de **\[ saída \]** devem ser ponteiros.

O parâmetro **\[ out \]** deve ser um ponteiro e, por padrão, todos os parâmetros de ponteiro são ponteiros de referência. O ponteiro de referência não é alterado durante a chamada; ele aponta para a mesma memória que antes da chamada. Para ponteiros de cadeia de caracteres, a restrição adicional do ponteiro de referência significa que o cliente deve alocar memória válida suficiente antes de fazer a chamada de procedimento remoto. Os stubs transmitem a cadeia de caracteres que os atributos **\[ out, String \]** indicam na memória já alocada no lado do cliente.

Os tópicos a seguir descrevem os protótipos de parâmetro de procedimento remoto para cadeias de caracteres:

-   [\[dentro, fora do protótipo de cadeia de caracteres \]](-in-out-string-prototype.md)
-   [\[no, String \] e \[ out, protótipo de cadeia de caracteres \]](-in-string-and-out-string-prototype.md)

 

 