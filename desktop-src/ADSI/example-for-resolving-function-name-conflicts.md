---
title: Exemplo para resolver conflitos de nome de função
description: Este tópico descreve como resolver conflitos de nome de função ao criar uma extensão para ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- adsi adsi, código de exemplo Visual Basic, resolvendo conflitos de nome de função
- resolvendo conflitos de nome de função ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6ce09251ba61b31768d973e258c568694067aff0420f0512a13913bb6fce90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179976"
---
# <a name="example-for-resolving-function-name-conflicts"></a>Exemplo para resolver conflitos de nome de função

Considere o seguinte:

-   IADs0 não dá suporte a Func0.
-   IADs1 dá suporte a func1 e Func0.
-   IADs2 dá suporte a func2 e Func0.

Todas as três interfaces são interfaces duplas.


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



Lembre-se de que, embora IADs1 não ofereça suporte a func2, um cliente ADSI reconhece um [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que dá suporte a todas as interfaces duplas e de expedição no modelo. Assim, o cliente ADSI pode chamar diretamente func2 usando myInf1. func2 sem resolver qual interface dá suporte a Func2.


```VB
myInf1.Func2
```



IADs1 e IADs2 têm uma função chamada Func0, mas IADs1:: Func0 é invocado diretamente usando o acesso vtable, porque os dois itens a seguir se aplicam ao cliente:

-   O cliente tem um ponteiro para o objeto IADs1 de interface dupla, que tem uma função chamada Func0.
-   o Visual Basic dá suporte ao acesso direct vtable, supondo que esse tipo de dados esteja disponível por meio da biblioteca de tipos.

No próximo exemplo de código, o cliente tem um ponteiro de interface dupla para IADs2 em vez de IADs1. Portanto, IADs2:: Func0 é invocado usando o acesso Direct vtable.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



Novamente, no próximo exemplo de código, IADs1 e IADs2 têm uma função chamada Func0, mas, aqui, o cliente tem um ponteiro para uma interface dupla, IADs0, que não tem uma função chamada Func0. Portanto, nenhum acesso Direct vtable pode ser executado. Em vez disso, [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) são chamados para invocar Func0.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Considere estes dois casos:

-   IADs1 e IADs2 são implementados por dois componentes COM, Ext1 e ext2, respectivamente. Se Ext1 vier antes de ext2 no registro, IADs1:: Func0 será invocado. No entanto, se o ext2 vier primeiro no registro, IADs2:: Func0 será invocado.
-   Se IADs1 e ADs2 forem implementados pelo mesmo objeto de extensão, Func0 será sempre invocado pelos métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) da extensão.

O desenvolvedor de extensão deve determinar como resolver conflitos de funções, ou propriedades, de diferentes interfaces duplas de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que têm o mesmo nome em uma extensão. A implementação dos métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) deve resolver esse conflito. Por exemplo, se você usar IMyInterface1:: func1 e IMyInterface2:: func1, em que IMyInterface1 e IMyInterface2 são interfaces duplas **IDispatch** com suporte no mesmo objeto de extensão. Os métodos **PrivateGetIDsOfNames** e **PrivateInvoke** devem determinar qual func1 deve ser sempre chamado.

O mesmo se aplica a DISPIDs conflitantes em diferentes interfaces dual ou [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .

Por exemplo, o DISPID de IMyInterface1:: Y é 2 no arquivo IMyInterface1. odl ou IMyInterface1. idl. O DISPID de IMyInterface2:: X também é 2 em iMyInterface2. odl. [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) deve retornar um DispId exclusivo, dentro da própria extensão, para cada, em vez de retornar o mesmo DISPID para ambos.

A ADSI resolve o primeiro problema não dá suporte a várias interfaces com nomes de função ou Propriedade conflitantes. Ele resolve o segundo problema adicionando um exclusivo, que está dentro do mesmo objeto de extensão, o número de interface para os bits não utilizados do DISPID.

 

 