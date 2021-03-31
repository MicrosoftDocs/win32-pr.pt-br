---
title: Sobre tipos de dados de .NET Framework
description: Sobre tipos de dados de .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player,. NET Framework
- Modelo de objeto do Windows Media Player,. NET Framework
- modelo de objeto,. NET Framework
- Windows Media Player Mobile, .NET Framework
- Controle ActiveX do Windows Media Player, .NET Framework
- Controle ActiveX móvel do Windows Media Player, .NET Framework
- Controle ActiveX, .NET Framework
- .NET Framework, tipos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006018"
---
# <a name="about-net-framework-data-types"></a>Sobre tipos de dados de .NET Framework

Esta seção contém as informações necessárias para converter a referência de modelo de objeto orientado a script em tipos de dados base do Microsoft .NET Framework. A referência de script do Windows Media Player tem quase todas as informações de que você precisa para usar o controle do Windows Media Player em um programa baseado em .NET Framework e, na maioria dos casos, a sintaxe será semelhante à de outras linguagens de script, como o Microsoft JScript.

A referência do Windows Media Player fornece o tipo de dados JScript e, se necessário, a conversão de C++. Por exemplo, um **número** pode ser retornado por um método. O JScript trata todos os números da mesma forma, mas outras linguagens distinguem entre diferentes tipos de números (inteiro, ponto flutuante e assim por diante). A referência fornece a conversão de C++ para tipos de dados de número porque os números podem ser processados de forma diferente pelo C++. Por exemplo, C++ usa o tipo de dados **int** para inteiro aritmético e **flutuante** para ponto flutuante.

O .NET Framework usa um sistema um pouco diferente de tipos de dados base. A tabela a seguir mostra as diferenças nos tipos de dados comuns que você provavelmente usará. Para obter mais informações sobre .NET Framework tipos de dados básicos e a conversão em outros sistemas de tipo de dados, consulte a discussão guia do desenvolvedor de .NET Framework do namespace System base de tipos de dados.

Esta tabela fornece o .NET Framework nome da classe e o tipo de dados C#. Os tipos de dados para outros idiomas são definidos para cada idioma em suas respectivas referências de idioma.



| Tipo de dados script | Tipo de dados em C++     | Classe .NET Framework (tipo de dados C#) |
|------------------|-------------------|---------------------------------------|
| **Número**       | **int**           | **Int32** (**int**)                   |
| **Número**       | **longo**          | **Int32** (**int**)                   |
| **Número**       | **double**        | **Double** (**duplo**)               |
| **Número**       | **float**         | **Single** (**float**)                |
| **Cadeia de caracteres**       | **BSTR**          | **Cadeia de caracteres** (**cadeia de caracteres**)               |
| **Booliano**      | **BOOL de variante \_** | **Booliano** (**bool**)                |
| **Objeto**       | **Objeto**        | **Objeto** (**objeto**)               |



 

Se você estiver usando o Visual Studio, poderá usar a tecnologia Microsoft IntelliSense para determinar qual tipo de dados é esperado para uma função específica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Inserindo o controle do Windows Media Player em uma solução .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




