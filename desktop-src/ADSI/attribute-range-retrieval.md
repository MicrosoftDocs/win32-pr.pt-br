---
title: Recuperação de intervalo de atributos
description: Um atributo com valores múltiplos pode ter quase qualquer número de valores. Em muitos casos, pode ser vantajoso, ou até mesmo necessário, limitar o intervalo de valores que são recuperados por uma consulta.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI de recuperação de intervalo de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915915"
---
# <a name="attribute-range-retrieval"></a>Recuperação de intervalo de atributos

Um atributo com valores múltiplos pode ter quase qualquer número de valores. Em muitos casos, pode ser vantajoso, ou até mesmo necessário, limitar o intervalo de valores que são recuperados por uma consulta.

A recuperação de intervalo envolve a solicitação de um número limitado de valores de atributo em uma única consulta. O número de valores solicitados deve ser menor ou igual ao número máximo de valores com suporte pelo servidor. Para reduzir o número de vezes que a consulta deve entrar em contato com o servidor, o número de valores solicitados deve ser o mais próximo possível do máximo possível. Para permitir que um aplicativo funcione corretamente com todos os servidores Windows, um número máximo de 1000 deve ser usado.

Os especificadores de intervalo para uma consulta de propriedade exigem o seguinte formato:


```C++
range=<low range>-<high range>
```



em que " &lt; intervalo baixo &gt; " é o índice de base zero do primeiro valor da propriedade a ser recuperado e " &lt; intervalo alto &gt; " é o índice de base zero do último valor da propriedade a ser recuperado. Zero é usado para " &lt; intervalo baixo &gt; " para especificar a primeira entrada. O caractere curinga ( \* ) pode ser usado para " &lt; intervalo alto &gt; " para especificar todas as entradas restantes.

A tabela a seguir lista exemplos de especificadores de intervalo.



| Exemplo      | Descrição                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| intervalo = 0-\*   | Recupere todos os valores de propriedade. Isso está sujeito a limites impostos pelo servidor.                |
| intervalo = 0-500  | Recupere de 1 a 501st valores inclusivamente.                                                |
| intervalo = 2-3    | Recupere os 3 e 4º valores.                                                                  |
| intervalo = 501-\* | Recupere o 502nd e todos os valores restantes. Isso está sujeito a limites impostos pelo servidor. |



 

Há várias maneiras diferentes de recuperar um intervalo de valores de propriedade. O método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pode ser usado em uma linguagem de automação ou em um C++. O método **IADs. GetInfoEx** é o método preferencial para executar a recuperação de intervalo. Para obter mais informações sobre como usar **IADs. GetInfoEx** para recuperação de intervalo, consulte [usando IADs:: GetInfoEx para recuperação de intervalo](using-iads--getinfoex-for-range-retrieval.md).

Se um idioma de automação for usado, o ADO (objetos de diretório do ActiveX) poderá ser usado para recuperar um intervalo de valores de propriedade. Para obter mais informações sobre como usar o ADO para recuperação de intervalo, consulte [usando ADO para recuperação de intervalo](using-ado-for-range-retrieval.md).

Se o C++ for usado, as interfaces [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) e [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) poderão ser usadas para recuperar um intervalo de valores de propriedade. Para obter mais informações sobre como usar **IDirectorySearch** e **IDirectoryObject** para recuperação de intervalo, consulte [usando IDirectorySearch e IDirectoryObject para recuperação de intervalo](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).

 

 




