---
title: Recuperação de intervalo de atributos
description: Um atributo com vários valores pode ter quase qualquer número de valores. Em muitos casos, pode ser vantajoso ou até mesmo necessário limitar o intervalo de valores recuperados por uma consulta.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI de Recuperação de Intervalo de Atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994b1c4535ebce264386b088a53b730e679147f07b4bef9fe99d3a45a63461fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840573"
---
# <a name="attribute-range-retrieval"></a>Recuperação de intervalo de atributos

Um atributo com vários valores pode ter quase qualquer número de valores. Em muitos casos, pode ser vantajoso ou até mesmo necessário limitar o intervalo de valores recuperados por uma consulta.

A recuperação de intervalo envolve solicitar um número limitado de valores de atributo em uma única consulta. O número de valores solicitados deve ser menor ou igual ao número máximo de valores com suporte pelo servidor. Para reduzir o número de vezes que a consulta deve entrar em contato com o servidor, o número de valores solicitados deve ser o mais próximo possível desse máximo. Para permitir que um aplicativo funcione corretamente com todos os Windows, um número máximo de 1000 deve ser usado.

Os especificadores de intervalo para uma consulta de propriedade exigem o seguinte formulário:


```C++
range=<low range>-<high range>
```



em que " intervalo baixo " é o índice baseado em zero do primeiro valor da propriedade a ser recuperado e " intervalo alto " é o índice baseado em zero do último valor da propriedade a &lt; &gt; ser &lt; &gt; recuperado. Zero é usado para " &lt; intervalo baixo " para especificar a primeira &gt; entrada. O caractere curinga ( \* ) pode ser usado para " intervalo alto " para especificar todas as entradas &lt; &gt; restantes.

A tabela a seguir lista exemplos de especificadores de intervalo.



| Exemplo      | Descrição                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| range=0-\*   | Recupere todos os valores de propriedade. Isso está sujeito aos limites impostos pelo servidor.                |
| range=0-500  | Recupere de 1º a 501º valores inclusive.                                                |
| range=2-3    | Recuperar 3º e 4º valores.                                                                  |
| range=501-\* | Recupere o 502º e todos os valores restantes. Isso está sujeito aos limites impostos pelo servidor. |



 

Há várias maneiras diferentes de recuperar um intervalo de valores de propriedade. O [**método IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pode ser usado em uma linguagem de automação ou C++. O **método IADs.GetInfoEx** é o método preferencial para executar a recuperação de intervalo. Para obter mais informações sobre como usar **IADs.GetInfoEx** para recuperação de intervalo, consulte [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).

Se uma linguagem de automação for usada, o ActiveX ADO (Directory Objects) poderá ser usado para recuperar um intervalo de valores de propriedade. Para obter mais informações sobre como usar o ADO para recuperação de intervalo, consulte [Using ADO for Range Retrieval](using-ado-for-range-retrieval.md).

Se C++ for usado, as interfaces [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) e [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) poderão ser usadas para recuperar um intervalo de valores de propriedade. Para obter mais informações sobre como usar **IDirectorySearch** e **IDirectoryObject** para recuperação de intervalo, consulte [Using IDirectorySearch and IDirectoryObject for Range Retrieval](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).

 

 




