---
description: Um alias no WMI é uma referência simbólica em uma classe ou instância de classe localizada em outro lugar em um arquivo formato MOF (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Criando um alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814142"
---
# <a name="creating-a-wmi-alias"></a>Criando um alias WMI

Um [*alias*](gloss-a.md) no WMI é uma referência simbólica em uma classe ou instância de classe localizada em outro lugar em um arquivo formato MOF (MOF). O compilador MOF usa aliases para estabelecer referências entre classes e instâncias. O compilador resolve aliases para as classes às quais se referem, de modo que os nomes de alias não estão disponíveis no código compilado. Como resultado, os aplicativos cliente não podem se referir a classes que usam aliases.

> [!Note]  
> O WMI dá suporte à referência direta, mas não a aliases circulares.

 

Um alias tem escopo somente dentro do arquivo MOF no qual você declara o alias. Portanto, normalmente você usa um alias como um atalho para um caminho de objeto longo.

**Para definir um alias**

1.  Adicione a frase "como $*aliasname*" à declaração de instância ou classe.
2.  Os nomes de alias seguem as mesmas regras que os nomes de instância e classe, exceto que os nomes de alias devem começar com um cifrão ($). Sublinhados podem aparecer em um nome de alias após o caractere inicial.

O exemplo de código a seguir descreve como usar um alias em uma definição de classe.

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

Os exemplos de código a seguir descrevem como usar um alias como uma referência simbólica para um caminho de objeto. Esses exemplos declaram duas classes para descrever um disco: a classe Disk para indicar a letra da unidade e a classe DiskRef para indicar o caminho do disco. Um alias é definido para a instância de classe de disco. Esse alias é usado como o valor para a propriedade PathToDisk na instância DiskRef.

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma classe](creating-a-class.md)
</dt> </dl>

 

 



