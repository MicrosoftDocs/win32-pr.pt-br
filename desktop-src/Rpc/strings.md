---
title: atributo string (RPC)
description: O atributo \ string\ e a RPC (Chamada de Procedimento Remoto).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e58b0750169a89f34840333f1ea55ee2ee096b24f3b87e425035f04ca759849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127696"
---
# <a name="string-attribute-rpc"></a>atributo string (RPC)

O atributo de cadeia de caracteres indica que o parâmetro é um ponteiro para uma matriz do \[ [](/windows/desktop/Midl/string) \] tipo [char](/windows/desktop/Midl/char-idl), [byte](/windows/desktop/Midl/byte)ou **w \_ char**. Assim como com uma matriz compatível, o tamanho de um parâmetro **\[ de \]** cadeia de caracteres é determinado em tempo de executar. Ao contrário de uma matriz compatível, o desenvolvedor não precisa **\[ \]** fornecer o comprimento associado à matriz – o atributo de cadeia de caracteres informa ao stub para determinar o tamanho da matriz chamando **strlen**. Um **\[ atributo de \]** cadeia de caracteres não pode ser usado ao mesmo tempo que o comprimento \[ [ \_ é](/windows/desktop/Midl/length-is) \] ou o último \[ [ \_ é](/windows/desktop/Midl/last-is) \] atributos.

A **\[ combinação \] de atributo de** cadeia de caracteres in direciona o stub para passar a cadeia de caracteres somente do cliente para o servidor. A quantidade de memória alocada no servidor é a mesma que o tamanho da cadeia de caracteres transmitida mais uma.

Os \[ [atributos de](/windows/desktop/Midl/out-idl)cadeia **de caracteres** out \] direcionam o stub para passar a cadeia de caracteres somente do servidor para o cliente. O design de chamada por valor da linguagem C diz que **todos \[ \]** os parâmetros de saída devem ser ponteiros.

O **\[ parâmetro out \]** deve ser um ponteiro e, por padrão, todos os parâmetros de ponteiro são ponteiros de referência. O ponteiro de referência não muda durante a chamada – ele aponta para a mesma memória que antes da chamada. Para ponteiros de cadeia de caracteres, a restrição adicional do ponteiro de referência significa que o cliente deve alocar memória válida suficiente antes de fazer a chamada de procedimento remoto. Os stubs transmitem a cadeia de caracteres que os **\[ atributos de \]** cadeia de caracteres out indicam para a memória já alocada no lado do cliente.

Os tópicos a seguir descrevem os protótipos de parâmetro de procedimento remoto para cadeias de caracteres:

-   [\[in, out, string \] Prototype](-in-out-string-prototype.md)
-   [\[in, string \] and \[ out, string \] Prototype](-in-string-and-out-string-prototype.md)

 

 