---
title: Problemas de implementação para provedores ADSI
description: Problemas de implementação para provedores ADSI
ms.assetid: 0be772aa-e7d8-4d34-b55a-162abfb0bfd4
ms.tgt_platform: multiple
keywords:
- Problemas de implementação para ADSI de provedores ADSI
- ADSI de provedores, implementando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c362b04244580e448e7bb7bd78889e66db12fe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366720"
---
# <a name="implementation-issues-for-adsi-providers"></a>Problemas de implementação para provedores ADSI

Para implementar interfaces ADSI, primeiro implemente a interface COM [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Ao fornecer essa interface como uma camada de sobrecarga mínima, você fornece aos aplicativos cliente o controle necessário para acessar objetos de diretório diretamente do diretório, em vez de por meio do cache ADSI, que otimiza o desempenho da rede. Usar essa interface também fornecerá sua própria implementação com mais flexibilidade.

Em segundo lugar, implemente as interfaces do ADSI, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) da propriedade cache. [**IADs**](/windows/desktop/api/Iads/nn-iads-iadsgroup) e [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) também são interfaces em demanda frequente pelo software de administração do sistema.

Em terceiro lugar, implemente as interfaces de gerenciamento de esquema se o seu serviço de diretório tiver um esquema subjacente: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax). Se não houver nenhum esquema subjacente, use essas interfaces para abstrair as classes e as propriedades usadas pelo serviço de diretório. Os esquemas podem ser usados para publicar os recursos do serviço de diretório em clientes ADSI.

## <a name="collections"></a>Coleções

Os componentes do provedor ADSI podem seguir um dos três modelos para armazenar em cache as coleções durante a enumeração. A escolha de um modelo de cache determina o comportamento de ADSI quando um objeto em uma coleção é excluído do serviço de diretório subjacente externo para ADSI.

Os modelos de cache incluem:

-   Coleções armazenadas em cache antecipadamente. A coleção de instâncias de objeto é recuperada do serviço de diretório subjacente em sua totalidade quando [**iadscollection:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) é chamado para criar um novo objeto enumerador. Se o objeto de origem de uma instância de objeto de Active Directory na coleção recuperada for excluído do serviço de diretório subjacente, o cliente não reconhecerá a exclusão até que um [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tente acessar a coleção.
-   Coleções em cache incrementalmente. A coleção é recuperada do serviço de diretório subjacente um objeto por vez quando [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) é chamado. [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) retornará ao início da coleção no cache e **IEnumVARIANT:: Next** retornará os objetos armazenados em cache até que o final do cache seja atingido; nesse ponto, novos objetos serão adicionados do armazenamento subjacente. Quando uma instância de objeto de Active Directory estiver no cache, o cliente não ficará ciente de sua exclusão do serviço de diretório subjacente até que um [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tente acessar o objeto.
-   Coleções não armazenadas em cache. A coleção é recuperada do serviço de diretório subjacente um objeto por vez quando [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) é chamado. [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) retornará ao início da coleção no armazenamento subjacente. As operações **IEnumVARIANT:: Next** e **IEnumVARIANT:: Reset** não podem recuperar objetos excluídos, pois os objetos são recuperados sob demanda do serviço de diretório subjacente. Somente o objeto atual é armazenado em cache; Se o objeto atual for excluído, o cliente não ficará ciente de sua exclusão do serviço de diretório subjacente até que um [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tente acessar o objeto.

Independentemente do modelo de cache, lembre-se de que a enumeração ADSI retorna Active Directory interfaces de serviço para o chamador. Para evitar a sobrecarga de obter um novo ponteiro de interface, os aplicativos ADSI devem armazenar em cache os ponteiros de interface retornados para objetos que pretendem manipular. Por exemplo, um aplicativo Visual Basic que enumera um contêiner e popula uma caixa de listagem com nomes pode armazenar em cache os ponteiros de interface associados aos nomes para uso posterior. Essa abordagem fornecerá um desempenho maior do que popular a caixa de listagem durante a enumeração e obter um novo ponteiro de interface quando o usuário fizer uma seleção.

## <a name="about-dispatch-ids"></a>Sobre as IDs de expedição

[**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) é uma interface de automação definida pelo com para controladores que não usam interfaces com diretamente. O acesso a um objeto por meio de **IDispatch** é chamado de acesso associado a nome ou de ligação tardia, pois ocorre em tempo de execução ("tardia") e usa nomes de cadeia de caracteres de propriedades e métodos para resolver referências ("nome"). Em tempo de execução, os clientes passam o nome da cadeia de caracteres da propriedade ou do método que desejam chamar para o método [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames)(). Se a propriedade ou o método existir no objeto, o identificador de expedição (dispID) da função correspondente será recuperado. Em seguida, o dispID é usado para executar a função por meio de [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)(). O uso de **IDispatch**, propriedades e métodos nas interfaces expostas por um único objeto aparece como uma lista simples. Como o acesso associado a nomes requer duas chamadas de função, ele é menos eficiente do que usar uma interface COM diretamente. Os clientes são incentivados a usar as interfaces COM ADSI nos objetos quando o desempenho é uma consideração. Controladores de automação avançados, como Visual Basic 4,0, podem chamar outras interfaces COM, bem como **IDispatch**, se as interfaces estiverem em conformidade com as restrições de automação para tipos de dados e passagem de parâmetros.

Os provedores ADSI geram dispIDs dinamicamente para cada objeto Active Directory. Os dispIDs recuperados por meio de [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) para um determinado objeto são os valores gerados, mas não os valores que estão em IDL para o objeto. Os usuários de [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) devem chamar **GetIDsOfNames** para obter DISPIDs válidos em tempo de execução.

## <a name="type-information-and-type-libraries"></a>Informações de tipo e bibliotecas de tipos

O SDK do ADSI fornece uma biblioteca de tipos, activeds. tlb, que documenta todas as interfaces padrão com suporte da ADSI. Um provedor deve fornecer uma biblioteca de tipos semelhante para todas as interfaces encontradas em activeds. tlb, além de quaisquer dados de tipo adicionais para as interfaces implementadas no componente do provedor.

Este é um exemplo de código IDL.

``` syntax
[ object, uuid(IID_IADsXYZ), oleautomation, dual ]
interface IADsXYZ: IDispatch
{
// Read-only properties.
[propget]
HRESULT AReadOnlyProp ([out, retval]BSTR *pbstrAReadOnlyProp);
 
// Read/write properties.
[propget]
HRESULT AReadWriteProp ([out, retval]long *plAReadWriteProp);
[propput]
HRESULT AReadWriteProp ([in]long lAReadWriteProp);
 
// Methods.
HRESULT AMethod ([in]DATE dateInParameter,
[out, retval]BSTR *pbstrReturnValue);
};
```

## <a name="thread-safety"></a>Acesso thread-safe

A Component Object Model (COM) descreve os três modelos de Threading a seguir. Os aplicativos COM indicam qual modelo está em uso ao inicializar a biblioteca COM usando as funções [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) e [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) :

-   Thread único. O modelo de thread único assume um único thread de execução em um processo, supondo que as estruturas de dados COM em um processo não precisem de serialização de acesso.
-   Threading de apartamento. Um objeto COM é associado ao thread que o criou. As chamadas para um objeto em outro thread devem ser executadas pelo thread que criou esse objeto. Para fazer isso, o thread de origem invoca um proxy de cliente que organiza a chamada de método e a entrega a uma função de stub de servidor no thread de destino por meio da fila de mensagens do Win32 associada ao thread de destino.
-   Threading gratuito. Os objetos COM são considerados thread-safe. Vários threads têm acesso permitido a qualquer objeto no processo sem nenhuma serialização imposta.

A ADSI não assume nenhum modelo de Threading específico. Os escritores de componentes do provedor devem assumir o modelo de Threading gratuito e garantir a consistência de suas estruturas de dados internas, protegendo-as contra threads não seguros, ou seja, sem coordenadas, por meio do uso de objetos de sincronização, como seções ou semáforos críticos.

## <a name="object-locking"></a>Bloqueio de objeto

A ADSI não impõe nem define um esquema de bloqueio de objeto. Provedores para namespaces que dão suporte à serialização de acesso usando bloqueio podem expor o esquema de bloqueio subjacente por meio de extensões específicas do provedor para a ADSI.

## <a name="property-names-within-a-schema"></a>Nomes de propriedade dentro de um esquema

ADSI representa propriedades como objetos de propriedade dentro do contêiner de esquema ADSI. Isso exige que os nomes de propriedade sejam exclusivos em cada contêiner de esquema. O provedor deve garantir que não haja colisões de nome.

## <a name="primary-interface"></a>Interface primária

Quando um provedor não pode identificar qual interface deve ser retornada como a interface primária, **IID \_ IADs** deve ser retornado. Isso fornece acesso com limite de nome a todas as propriedades de um objeto por meio de [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) e os métodos [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**iads::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put)e [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

 

 