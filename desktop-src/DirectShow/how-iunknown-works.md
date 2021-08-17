---
description: Como o IUnknown funciona
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Como o IUnknown funciona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1523a8de5d9b99df60ebaff540d4bf9468799e3be1361a4be111f15a142bbea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015584"
---
# <a name="how-iunknown-works"></a>Como o IUnknown funciona

Os métodos em **IUnknown** permitem que um aplicativo consulte interfaces no componente e gerencie a contagem de referência do componente.

**Contagem de referência**

A contagem de referência é uma variável interna, incrementada no **método AddRef** e decrementada no **método Release.** As classes base gerenciam a contagem de referência e sincronizam o acesso à contagem de referência entre vários threads.

**Consultas de interface**

Consultar uma interface também é simples. O chamador passa dois parâmetros: um IID (identificador de interface) e o endereço de um ponteiro. Se o componente dá suporte à interface solicitada, ele define o ponteiro para a interface, incrementa sua própria contagem de referência e retorna S \_ OK. Caso contrário, ele define o ponteiro como **NULL** e retorna E \_ NOINTERFACE. O pseudocódigo a seguir mostra a estrutura geral do **método QueryInterface.** A agregação de componentes, descrita na próxima seção, apresenta alguma complexidade adicional.


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



A única diferença entre o **método QueryInterface** de um componente e o método **QueryInterface** de outro é a lista de IIDs que cada componente testa. Para cada interface compatível com o componente, o componente deve testar a IID dessa interface.

**Agregação e delegação**

A agregação de componentes deve ser transparente para o chamador. Portanto, a agregação deve expor uma única interface **IUnknown,** com o componente agregado adiando para a implementação do componente externo. Caso contrário, o chamador verá duas interfaces **IUnknown** diferentes na mesma agregação. Se o componente não for agregado, ele usará sua própria implementação.

Para dar suporte a esse comportamento, o componente deve adicionar um nível de indcisão. Uma *delegação de IUnknown* delega o trabalho para o local apropriado: para o componente externo, se houver um ou para a versão interna do componente. Um *IUnknown nãodelista* faz o trabalho, conforme descrito na seção anterior.

A versão de delegação é pública e mantém o nome **IUnknown**. A versão não dedificação foi renomeada [**como INonDeltingUnknown.**](inondelegatingunknown.md) Esse nome não faz parte da especificação COM, porque não é uma interface pública.

Quando o cliente cria uma instância do componente, ele chama o **método IClassFactory::CreateInstance.** Um parâmetro é um ponteiro para a interface **IUnknown** do componente de agregação ou **NULL** se a nova instância não for agregada. O componente usa esse parâmetro para armazenar uma variável de membro que indica qual interface **IUnknown** usar, conforme mostrado no exemplo a seguir:


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



Cada método na delegação **de IUnknown** chama sua contraparte não dedelting, conforme mostrado no exemplo a seguir:


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



Pela natureza da delegação, os métodos de delegação são idênticos em cada componente. Somente as versões que não são de versões de versões são alteradas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



