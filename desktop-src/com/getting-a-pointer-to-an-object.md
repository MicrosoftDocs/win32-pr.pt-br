---
title: Obtendo um ponteiro para um objeto
description: Obtendo um ponteiro para um objeto
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0476d36390e7077e7fdd75eef8d95e8173683891
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2020
ms.locfileid: "105787655"
---
# <a name="getting-a-pointer-to-an-object"></a>Obtendo um ponteiro para um objeto

Como o COM não tem um modelo de classe estrito, há quatro maneiras pelas quais um cliente pode instanciar ou obter um ponteiro para uma interface em um objeto:

-   Chamar uma função de biblioteca COM que cria um objeto de um tipo predeterminado; ou seja, a função retornará um ponteiro para apenas uma interface específica para uma classe de objeto específica.
-   Chame uma função de biblioteca COM que possa criar um objeto com base em um identificador de classe (CLSID) e que retorne qualquer tipo de ponteiro de interface solicitado.
-   Chame um método de alguma interface que crie outro objeto (ou se conecte a um existente) e retorne um ponteiro de interface nesse objeto separado.
-   Implemente um objeto com uma interface por meio da qual outros objetos passam o ponteiro de interface diretamente para o cliente.

Para obter informações sobre como obter ponteiros para outras interfaces em um objeto depois que você tiver o primeiro, consulte [QueryInterface: navegando em um objeto](queryinterface--navigating-in-an-object.md).

## <a name="creating-an-object-of-a-predetermined-type"></a>Criando um objeto de um tipo predeterminado

Há várias funções COM, como [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc), que retornam ponteiros para implementações de interface específicas. (**CoGetMalloc** recupera um ponteiro para o alocador de memória com padrão.) A maioria delas são funções auxiliares e a maioria dessas funções são descritas nas seções de referência desta documentação, sob a área específica à qual estão relacionadas, como armazenamento ou transferência de dados.

## <a name="creating-an-object-based-on-a-clsid"></a>Criando um objeto com base em um CLSID

Há várias funções que, considerando um CLSID, um cliente pode chamar para criar uma instância de objeto e obter um ponteiro para ela. Todas essas funções são baseadas na função [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), que cria um objeto de classe e fornece um ponteiro para uma interface que permite que você crie instâncias dessa classe. Embora haja informações que indiquem em qual sistema o servidor reside, não há necessidade de que essas informações estejam contidas no cliente. O cliente precisa saber apenas o CLSID e nunca o caminho absoluto do código do servidor. Para obter mais informações, consulte [criando um objeto por meio de um objeto de classe](creating-an-object-through-a-class-object.md).

## <a name="returning-a-pointer-to-a-separate-object"></a>Retornando um ponteiro para um objeto separado

Entre os muitos métodos de interface que retornam um ponteiro para um objeto separado, há vários que criam e retornam um ponteiro para um *objeto enumerador*, que permite determinar quantos itens de um determinado tipo um objeto mantém. O COM define interfaces para enumerar uma grande variedade de itens, como cadeias de caracteres, estruturas importantes, monikers e ponteiros de interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . A maneira típica de criar uma instância de enumerador e obter um ponteiro para sua interface é chamar um método de outra interface. Por exemplo, a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) define dois métodos, [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) e [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), que retornam ponteiros para interfaces em dois objetos de enumeração diferentes. Há muitos outros exemplos em COM dos métodos que retornam ponteiros para objetos, como a interface de documento OLE composto [**IOleObject:: GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite), que, quando chamado no objeto incorporado ou vinculado, retorna um ponteiro para a implementação do objeto de contêiner de [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite).

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a>Implementando um objeto por meio do qual passar um ponteiro de interface diretamente para o cliente

Quando dois objetos, como um contêiner de documento OLE composto e um servidor, precisam de comunicação bidirecional, cada um implementa um objeto que contém um método de interface por meio do qual ele pode passar um ponteiro de interface para o outro objeto. O objeto de implementação, que também é o cliente do objeto criado, pode chamar o método e obter o ponteiro que foi passado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> <dt>

[Responsabilidades do servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 




