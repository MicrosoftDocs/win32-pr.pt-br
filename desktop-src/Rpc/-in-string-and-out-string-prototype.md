---
title: " no, String e out, protótipo de cadeia de caracteres"
description: O protótipo de função a seguir usa dois parâmetros de um parâmetro \ in, String \ Parameter e an out, String \.
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917619"
---
# <a name="in-string-and-out-string-prototype"></a>\[no, String \] e \[ out, protótipo de cadeia de caracteres \]

O protótipo de função a seguir usa dois parâmetros: um parâmetro \[ [**in**](/windows/desktop/Midl/in), [**String**](/windows/desktop/Midl/string) \] e um \[ parâmetro [**out**](/windows/desktop/Midl/out-idl), **String** \] .

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

O primeiro parâmetro é \[ somente [**no**](/windows/desktop/Midl/in) \] . Essa cadeia de caracteres de entrada só é transmitida do cliente para o servidor. O servidor usa-o como base para processamento adicional. A cadeia de caracteres não é modificada e não é requerida pelo cliente, portanto, não precisa ser retornada ao cliente.

O segundo parâmetro, que representa a resposta do médico, está \[ [**fora**](/windows/desktop/Midl/out-idl) \] apenas. Essa cadeia de caracteres de resposta só é transmitida do servidor para o cliente. O tamanho de alocação é fornecido para que os stubs de servidor possam alocar memória para ele. Como *pszOutput* é um \[ ponteiro de [**referência**](/windows/desktop/Midl/ref) \] , o cliente deve ter memória suficiente alocada para a cadeia de caracteres antes da chamada. A cadeia de caracteres de resposta é gravada nessa área de memória quando o procedimento remoto retorna.

 

 