---
title: Resolução de conflitos de nome de função/Propriedade em automação em extensões
description: Neste tópico, \ 0034; objeto \ 0034; indica o objeto, como um todo, como um cliente ADSI o exibe. Ou seja, ADSI e todas as suas extensões.
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- Resolução de conflitos de função e nome de propriedade em automação em extensões
- ADSI de extensões, resolvendo conflitos de nome de função e Propriedade na automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a7ac99b99ecdf0ee1b940f066d9e8166a15542
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366706"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>Resolução de conflitos de nome de função/Propriedade em automação em extensões

Neste tópico, "Object" indica o objeto, como um todo, como um cliente ADSI o exibe. Ou seja, ADSI e todas as suas extensões.

## <a name="same-function-name-with-the-same-parameters"></a>Mesmo nome de função com os mesmos parâmetros

Se duas ou mais interfaces duplas [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) em um objeto oferecerem suporte a uma propriedade ou um método com o mesmo nome, por exemplo, **func1**, a invocação será determinada usando os critérios a seguir. Se o cliente tiver um ponteiro para uma das interfaces duplas que dão suporte a um método chamado **func1** e se o ambiente de automação der suporte ao acesso vtable, **func1** será invocado diretamente por meio do acesso ADSI vtable.

Se qualquer uma das condições acima for false, [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) serão chamados para invocar **func1**.

Para obter mais informações e uma breve explicação sobre como um cliente pode adicionar um ponteiro a uma interface dupla e uma descrição dos tipos de ambientes que dão suporte ao acesso vtable, consulte [associação tardia versus acesso vtable no modelo de extensão ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).

Como todos os objetos de extensão redirecionam as funções [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de volta para o agregador, o agregador controla qual **func1** é invocado. As regras são:

-   Se qualquer interface, e houver apenas uma, se houver, no agregador (ADSI) oferece suporte a uma função chamada **func1**, o agregador invocará seu próprio **func1**.
-   Caso contrário, o agregador passará por cada uma de suas extensões, na ordem listada no registro, e encontrará a primeira extensão que implementa uma função chamada **func1**. É possível, mas improvável, que várias interfaces duplas [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) nessa primeira extensão tenham uma função chamada **func1**. A extensão deve determinar qual **func1** deve ser sempre chamado na automação.

## <a name="same-function-name-with-different-parameters"></a>Mesmo nome de função com parâmetros diferentes

A seção anterior abordou como resolver conflitos de nome de função, ou seja, nomes de função que têm o mesmo nome de função e a mesma lista de parâmetros, como número, tipo e ordem, quando ocorre na automação. E se duas funções tiverem o mesmo nome, mas parâmetros diferentes? Se um cliente ADSI invocar a função usando [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) sem usar vários nomes para especificar os parâmetros, o modelo de extensão ADSI não poderá desambiguar as funções. Com base no esquema de resolução discutido acima, a primeira extensão no registro que dá suporte a essa função por meio de uma de suas interfaces tem sua versão dessa função invocada, e a chamada pode falhar ou gerar resultados incorretos.

Por exemplo:

-   Extn1 (primeiro no registro em classe CA – prioridade mais alta) dá suporte a **IInterface1**.
-   Extn2 (terceiro no registro em classe CA – prioridade mais baixa) dá suporte a **IInterface2**.
-   **IInterface1** dá suporte a **Method1 (int param1, int param2)**.
-   **IInterface2** dá suporte a **Method1 (int param1)**.

Um cliente ADSI tem um ponteiro de interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para um objeto da classe ca. Ele quer invocar **IInterface2:: Method1**. Se o cliente chama "pDispatch->GetIDsOfNames (IID \_ NULL, rgszNames, 1, My \_ LCID, rgDispId)" armazenando apenas o nome da função "method1" *em \[ rgszNames \] 0*, **IInterface1:: Method1** em vez do desired **IInterface2:: Method1** é invocado e a função falha porque o número de parâmetros é diferente.

Para minimizar esse problema, os desenvolvedores de extensão podem prefixar seus nomes de função com seus próprios identificadores específicos e evitar designs de interface que usam funções de mesmo nome, mas parâmetros diferentes.

Se ocorrer um conflito de nomes, os clientes ADSI poderão evitar o problema pelo acesso direto vtable se a interface for uma interface dupla. Se o acesso Direct vtable não for possível, os clientes ADSI devem chamar [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) com vários nomes, especificando os nomes de função, bem como os parâmetros na matriz *rgszNames* descrita anteriormente.

Visual Basic 5 não chama a função [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) com vários nomes. Ou seja, ele passa apenas o nome da função para **GetIDsOfNames**, mas não para argumentos. No entanto, Visual Basic 5 permite que os usuários invoquem uma função pelo acesso Direct vtable, em vez de invocar a função **IDispatch:: GetIDsOfNames** se a interface for uma interface dupla. Os desenvolvedores devem usar o acesso Direct vtable, se possível.

Para obter mais informações sobre a resolução de conflitos de nome, consulte o [exemplo para resolver conflitos de nome de função](example-for-resolving-function-name-conflicts.md).

 

 