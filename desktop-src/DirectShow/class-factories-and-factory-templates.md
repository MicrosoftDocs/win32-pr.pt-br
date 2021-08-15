---
description: Este tópico descreve como implementar uma DLL para um filtro DirectShow, usando as classes DirectShow base.
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Fábricas de classes e modelos de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9329a0b8cfd22a316add88664604df190ae96c765359c723aa2302c5b1fa1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402201"
---
# <a name="class-factories-and-factory-templates"></a>Fábricas de classes e modelos de fábrica

Este tópico descreve como implementar uma DLL para um filtro DirectShow, usando o [DirectShow Classes Base](directshow-base-classes.md).

Antes que um cliente crie uma instância de um objeto COM, ele cria uma instância da fábrica de classes do objeto, usando uma chamada para a [**função CoGetClassObject.**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) Em seguida, o cliente chama o método **IClassFactory::CreateInstance da** fábrica de classe. É a fábrica de classes que realmente cria o componente e retorna um ponteiro para a interface solicitada. (A [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) combina essas etapas, dentro da chamada de função.)

A ilustração a seguir mostra a sequência de chamadas de método.

![chamadas de método para criar uma fábrica de classes](images/classfactory.png)

[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) chama a [**função DllGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) que é definida na DLL. Essa função cria a fábrica de classes e retorna um ponteiro para uma interface na fábrica de classes. DirectShow implementa **DllGetClassObject** para você, mas a função depende do código de uma maneira específica. Para entender como ele funciona, você deve entender como DirectShow implementa fábricas de classes.

Uma fábrica de classes é um objeto COM dedicado à criação de outro objeto COM. Cada fábrica de classes tem um tipo de objeto que ele cria. No DirectShow, cada fábrica de classes é uma instância da mesma classe C++, **CClassFactory.** As fábricas de classes são especializadas por meio de outra classe, [**CFactoryTemplate**](cfactorytemplate.md), também chamada de *modelo de fábrica*. Cada fábrica de classes contém um ponteiro para um modelo de fábrica. O modelo de fábrica contém informações sobre um componente específico, como o CLSID (identificador de classe) do componente e um ponteiro para uma função que cria o componente.

A DLL declara uma matriz global de modelos de fábrica, um para cada componente na DLL. Quando [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) faz uma nova fábrica de classes, ele pesquisa na matriz um modelo com um CLSID correspondente. Supondo que ele encontre um, ele cria uma fábrica de classes que contém um ponteiro para o modelo correspondente. Quando o cliente chama **IClassFactory::CreateInstance**, o fábrica de classe chama a função de instanância definida no modelo.

A ilustração a seguir mostra a sequência de chamadas de método.

![modelos de fábrica de classe em uma dll](images/classfactory2.png)

O benefício dessa arquitetura é que você pode definir apenas algumas coisas que são específicas para seu componente, como a função de instalização, sem implementar toda a fábrica de classes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar uma DLL DirectShow filtro de dados](how-to-create-a-dll.md)
</dt> </dl>

 

 
