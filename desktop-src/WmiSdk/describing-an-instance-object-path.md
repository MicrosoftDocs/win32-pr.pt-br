---
description: Um caminho de objeto de instância descreve o local de uma instância de uma determinada classe dentro de um namespace específico.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Descrevendo um caminho de objeto de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297058"
---
# <a name="describing-an-instance-object-path"></a>Descrevendo um caminho de objeto de instância

Um caminho de objeto de instância descreve o local de uma instância de uma determinada classe dentro de um namespace específico.

Você pode ter vários tipos diferentes de caminhos de objeto de instância:

-   Completo

    Um caminho de objeto de instância completo acrescenta o nome e o valor da propriedade de chave para a classe a um caminho de objeto de classe completa.

    O exemplo a seguir mostra a definição do caminho completo do objeto de instância.

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   Relativo

    Um caminho de objeto relativo refere-se a uma instância localizada no namespace atual no servidor atual. O caminho relativo consiste no nome da classe seguido pelos nomes e valores das propriedades de chave dessa instância.

    O exemplo a seguir mostra a definição do caminho do objeto de instância relativo.

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   Relativo a uma única chave

    Para classes com apenas uma propriedade designada como chave, você pode omitir o nome da propriedade de chave.

    O exemplo a seguir mostra a definição do caminho do objeto de instância relativo com uma única chave.

    ``` syntax
    MyClass="e:"
    ```

-   Relativo a várias chaves

    Use uma vírgula para distinguir entre as chaves de uma instância com várias chaves.

    O exemplo a seguir mostra as definições do caminho do objeto de instância relativo com várias chaves.

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   Relativo para uma classe singleton

    O caminho relativo do objeto para uma classe singleton consiste no nome da classe seguido pela notação "= @".

    O exemplo a seguir mostra a definição do caminho de objeto da instância relativa para uma classe singleton.

    ``` syntax
    MySingletonClass=@
    ```

O procedimento a seguir descreve como recuperar uma instância de classe.

**Para recuperar uma instância de classe**

1.  Inicialize uma cadeia de caracteres que contenha o caminho do objeto com uma chamada para a função [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) .
2.  Inicialize um objeto que receberá a instância.
3.  Recupere o objeto com uma chamada para [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

    Para usar o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), você deve implementar a interface [**IWbemSink**](swbemsink.md) .

A \# instrução include a seguir é necessária para o código listado posteriormente neste tópico para ser compilado corretamente.


```C++
#include <wbemidl.h>
```



O exemplo de código a seguir descreve como recuperar uma instância de classe usando um caminho de objeto.


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



Para instâncias de classes que especificam várias propriedades como chave, o WMI não requer nenhuma ordenação específica de propriedades de chave em caminhos de objeto. Você só precisa especificar o valor de cada uma das propriedades no caminho do objeto.

O exemplo de código a seguir descreve duas descrições de chave equivalentes.

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
