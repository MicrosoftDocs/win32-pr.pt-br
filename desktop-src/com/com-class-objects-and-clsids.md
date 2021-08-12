---
title: CLSIDs e objetos de classe COM
description: Um servidor COM é implementado como uma classe COM.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6bcd00f886d3a754a44658e669189d28fd2fa121248b667ba2a3928b626f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550620"
---
# <a name="com-class-objects-and-clsids"></a>CLSIDs e objetos de classe COM

Um servidor COM é implementado como uma classe COM. Uma *classe COM* é uma implementação de um grupo de interfaces no código executada sempre que você interage com um determinado objeto. Há uma distinção importante entre uma classe C++ e uma classe COM: no C++, uma classe é um tipo, enquanto uma classe COM é simplesmente uma definição do objeto e não carrega nenhum tipo, embora um programador C++ possa implementá-la usando uma classe C++. O COM foi projetado para permitir que uma classe seja usada por diferentes aplicativos, incluindo aplicativos escritos sem conhecimento da existência dessa classe específica. Portanto, o código de classe para um determinado tipo de objeto existe em uma DLL (biblioteca vinculada dinâmica) ou em outro aplicativo executável (EXE).

Cada classe COM é identificada por *um CLSID*, um GUID exclusivo de 128 bits, que o servidor deve registrar. O COM usa essa CLSID, a pedido de um cliente, para associar dados específicos à DLL ou EXE que contém o código que implementa a classe , criando assim uma instância do objeto .

Para clientes e servidores no mesmo computador, o CLSID do servidor é tudo o que o cliente precisa. Em cada computador, o COM mantém um banco de dados (ele usa o registro do sistema nas plataformas Microsoft Windows e Macintosh) de todos os CLSIDs para os servidores instalados no sistema. Esse é um mapeamento entre cada CLSID e o local da DLL ou EXE que ressalva o código para essa CLSID. O COM consulta esse banco de dados sempre que um cliente deseja criar uma instância de uma classe COM e usar seus serviços, para que o cliente nunca precise saber o local absoluto do código no computador.

Para sistemas distribuídos, o COM fornece entradas do Registro que permitem que um servidor remoto se registre para uso por um cliente. Embora os aplicativos precisem conhecer apenas o CLSID de um servidor, pois podem contar com o Registro para localizar o servidor, o COM permite que os clientes substituam as entradas do Registro e especifiquem locais do servidor para aproveitar ao máximo a rede. (Consulte [Localizando um objeto remoto](locating-a-remote-object.md).)

A maneira básica de criar uma instância de uma classe é por meio de um objeto de *classe* COM . Esse é simplesmente um objeto intermediário que dá suporte a funções comuns à criação de novas instâncias de uma determinada classe. A maioria dos objetos de classe usados para criar objetos de um CLSID é suportada pela interface [**IClassFactory,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) uma interface que inclui o importante [**método CreateInstance.**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) Você implementa uma interface **IClassFactory** para cada classe de objeto que você oferece para ser instautada. (Para obter mais informações sobre como implementar **IClassFactory,** consulte [Implementando IClassFactory](implementing-iclassfactory.md).)

> [!Note]  
> Os servidores que suportam alguma outra interface de fábrica de classe personalizada não são necessários para dar suporte especificamente [**a IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) No entanto, chamadas para funções de ativação diferentes de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (como [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)) exigem que o servidor seja suportado **por IClassFactory.**

 

Quando um cliente deseja criar uma instância do objeto do servidor, ele usa o CLSID do objeto desejado em uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). (Essa chamada pode ser direta ou implícita, por meio de uma das funções auxiliares de criação de objeto.) Essa função localiza o código associado ao CLSID, cria um objeto de classe e fornece um ponteiro para a interface solicitada. (**CoGetClassObject** recebe um *param riid* que especifica o ponteiro de interface desejado do cliente.)

> [!Note]  
> O COM tem apenas algumas funções nas quais muitas das outras são criadas. O mais importante deles é provavelmente [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), que é o que baseia todas as funções de criação de instância.

 

Com esse ponteiro, o chamador pode criar uma instância do objeto e recuperar um ponteiro para uma interface solicitada no objeto . Normalmente, essa é uma interface de inicialização, usada para ativar o objeto (colocá-lo no estado de execução) para que o cliente possa fazer qualquer trabalho com o objeto que deseja. Usando as funções básicas do COM, o cliente também deve ter cuidado para liberar todos os ponteiros de objeto.

Outro mecanismo para ativar instâncias de objeto é por meio do moniker de classe. Monikers de classe se vinculam ao objeto de classe da classe para a qual eles são criados. Para obter mais informações, consulte [Class Monikers](class-monikers.md).

O COM fornece várias funções auxiliares que reduzem o trabalho de criação de instâncias de objeto. Eles são descritos em [Funções auxiliares de criação de instância.](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um objeto por meio de um objeto de classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 