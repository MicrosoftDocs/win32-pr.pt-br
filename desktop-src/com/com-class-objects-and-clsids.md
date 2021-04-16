---
title: Objetos de classe COM e CLSIDs
description: Um servidor COM é implementado como uma classe COM.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfde2f379c4c7589db4cde283c8c67d720b21d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105765065"
---
# <a name="com-class-objects-and-clsids"></a>Objetos de classe COM e CLSIDs

Um servidor COM é implementado como uma classe COM. Uma *classe com* é uma implementação de um grupo de interfaces no código executado sempre que você interage com um determinado objeto. Há uma distinção importante entre uma classe C++ e uma classe COM: em C++, uma classe é um tipo, enquanto uma classe COM é simplesmente uma definição do objeto e não transporta nenhum tipo, embora um programador de C++ possa implementá-la usando uma classe C++. O COM foi projetado para permitir que uma classe seja usada por diferentes aplicativos, incluindo aplicativos escritos sem conhecimento da existência dessa classe específica. Portanto, o código de classe de um determinado tipo de objeto existe em uma DLL (biblioteca vinculada dinâmica) ou em outro aplicativo executável (EXE).

Cada classe COM é identificada por um *CLSID*, um GUID de 128 bits exclusivo, que o servidor deve registrar. O COM usa esse CLSID, na solicitação de um cliente, para associar dados específicos com a DLL ou EXE que contém o código que implementa a classe, criando assim uma instância do objeto.

Para clientes e servidores no mesmo computador, o CLSID do servidor é todo o cliente precisar. Em cada computador, o COM mantém um banco de dados (ele usa o registro do sistema em plataformas Microsoft Windows e Macintosh) de todos os CLSIDs para os servidores instalados no sistema. Esse é um mapeamento entre cada CLSID e o local do DLL ou EXE que abriga o código para esse CLSID. COM consulta esse banco de dados sempre que um cliente quiser criar uma instância de uma classe COM e usar seus serviços, o cliente nunca precisará saber o local absoluto do código no computador.

Para sistemas distribuídos, o COM fornece entradas de registro que permitem que um servidor remoto se registre para uso por um cliente. Embora os aplicativos precisem conhecer apenas o CLSID de um servidor, porque eles podem confiar no registro para localizar o servidor, o COM permite que os clientes substituam as entradas do registro e especifiquem os locais do servidor, para aproveitar ao máximo a rede. (Consulte [localizando um objeto remoto](locating-a-remote-object.md).)

A maneira básica de criar uma instância de uma classe é por meio de um *objeto de classe* com. Trata-se simplesmente de um objeto intermediário que dá suporte a funções comuns à criação de novas instâncias de uma determinada classe. A maioria dos objetos de classe usados para criar objetos de um CLSID dá suporte à interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , uma interface que inclui o método [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) importante. Implemente uma interface **IClassFactory** para cada classe de objeto que você oferece a ser instanciada. (Para obter mais informações sobre como implementar **IClassFactory**, consulte [implementando IClassFactory](implementing-iclassfactory.md).)

> [!Note]  
> Os servidores que dão suporte a alguma outra interface de fábrica de classe personalizada não são necessários para dar suporte a [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) especificamente. No entanto, as chamadas para funções de ativação que não sejam [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (como [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)) exigem que o servidor dê suporte a **IClassFactory**.

 

Quando um cliente deseja criar uma instância do objeto do servidor, ele usa o CLSID do objeto desejado em uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). (Essa chamada pode ser direta ou implícita, por meio de uma das funções auxiliares de criação de objeto.) Essa função localiza o código associado ao CLSID e cria um objeto de classe e fornece um ponteiro para a interface solicitada. (**CoGetClassObject** usa um parâmetro *riid* que especifica o ponteiro de interface desejado do cliente.)

> [!Note]  
> O COM tem apenas algumas funções nas quais muitos dos outros são criados. O mais importante deles é provavelmente [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), que se baseia em todas as funções de criação de instância.

 

Com esse ponteiro, o chamador pode criar uma instância do objeto e recuperar um ponteiro para uma interface solicitada no objeto. Normalmente, isso é uma interface de inicialização, usada para ativar o objeto (colocá-lo no estado de execução) para que o cliente possa fazer qualquer trabalho com o objeto que desejar. Usando as funções básicas do COM, o cliente também deve cuidar de liberar todos os ponteiros de objeto.

Outro mecanismo de ativação de instâncias de objeto é por meio do moniker de classe. Os monikers de classe são associados ao objeto de classe da classe para a qual eles são criados. Para obter mais informações, consulte [moniker de classe](class-monikers.md).

O COM fornece várias funções auxiliares que reduzem o trabalho de criação de instâncias de objeto. Elas são descritas em [funções auxiliares de criação de instância](instance-creation-helper-functions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um objeto por meio de um objeto de classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 