---
title: Criando a tabela de interface global
description: Criando a tabela de interface global
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366785"
---
# <a name="creating-the-global-interface-table"></a>Criando a tabela de interface global

Use a chamada a seguir para criar o objeto de tabela de interface global e obter um ponteiro para [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> Ao criar o objeto de tabela de interface global usando a chamada anterior, é necessário vincular à biblioteca UUID. lib. Isso resolverá os símbolos externos CLSID \_ StdGlobalInterfaceTable e IID \_ IGlobalInterfaceTable.

 

Há uma única instância da tabela de interface global por processo, portanto, todas as chamadas para essa função em um processo retornam a mesma instância.

Após a chamada para a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , registre a interface do apartamento na qual ela reside com uma chamada para o método [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) . Esse método fornece um cookie que identifica a interface e sua localização. Um apartamento que procura um ponteiro para essa interface, em seguida, chama o método [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) com esse cookie e a implementação, em seguida, fornece um ponteiro de interface para o apartamento de chamada. Para revogar o registro global da interface, qualquer Apartment pode chamar o método [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .

Um exemplo simples de uso de [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) seria quando você deseja passar um ponteiro de interface em um objeto em um STA (single-threaded apartment) para um thread de trabalho em outro apartamento. Em vez de ter que empacotá-lo em um fluxo e passar o fluxo para o thread de trabalho como um parâmetro de thread, o **IGlobalInterfaceTable** permite que você passe um cookie.

Ao registrar a interface na tabela de interface global, você obtém um cookie que pode ser usado em vez de passar o ponteiro real (sempre que você precisa passar o ponteiro), para um parâmetro sem método que vai para outro apartamento (como um parâmetro para [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) até [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) ou para a memória em processo acessível fora do seu apartamento.

É necessário ter cuidado porque o uso de interfaces globais coloca a carga extra sobre o programador de gerenciar problemas, como condições de corrida e exclusão mútua, que estão associados ao acesso ao estado global de vários threads simultaneamente.

COM fornece uma implementação padrão da interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . É altamente recomendável que você use essa implementação padrão porque ela fornece uma funcionalidade completa de thread-safe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Quando usar a tabela de interface global](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 