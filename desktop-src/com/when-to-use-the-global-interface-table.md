---
title: Quando usar a tabela de interface global
description: Quando usar a tabela de interface global
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008409"
---
# <a name="when-to-use-the-global-interface-table"></a>Quando usar a tabela de interface global

Se você estiver desempacotando um ponteiro de interface várias vezes entre Apartments em um processo, você poderá usar a interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Com outras técnicas, você precisaria fazer o reempacotamento a cada vez.

> [!Note]  
> Se o ponteiro de interface não tiver marshaling apenas uma vez, talvez você queira usar a função [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) . Ele também pode ser usado para passar um ponteiro de interface de um thread para outro thread no mesmo processo.

 

A interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) também torna mais simples o problema anteriormente mais difícil para o programador. Esse problema ocorre quando as seguintes condições se aplicam:

-   Um objeto ágil no processo agrega o marshaler de thread livre.
-   Esse mesmo objeto Agile também contém ponteiros de interface (como variáveis de membro) para outros objetos que não são ágeis e não agregam o marshaler de thread livre.

Nessa situação, se o objeto externo for empacotado para outro apartamento e o aplicativo for chamado, e o objeto tentar chamar em qualquer um de seus ponteiros de interface de variável de membro que não sejam de thread livre ou que sejam proxies para objetos em outros Apartments, poderá obter resultados incorretos ou o thread de erro RPC \_ E \_ incorreto \_ . Esse erro ocorre porque a interface interna foi projetada para ser chamada somente do apartamento no qual ela foi armazenada pela primeira vez na variável de membro.

Para resolver esse problema, o objeto externo que agrega o marshaler de thread livre deve chamar [**IGlobalInterfaceTable:: RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) na interface interna e armazenar o cookie resultante em sua variável de membro, em vez de armazenar o ponteiro de interface real. Quando o objeto externo deseja chamar em um ponteiro de interface do objeto interno, ele deve chamar [**IGlobalInterfaceTable:: GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), usar o ponteiro de interface retornado e, em seguida, liberá-lo. Quando o objeto externo desaparece, ele deve chamar [**IGlobalInterfaceTable:: RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) para remover a interface da tabela de interface global.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando a tabela de interface global](creating-the-global-interface-table.md)
</dt> </dl>

 

 