---
title: Sobre .NET Framework tipos de dados
description: Sobre .NET Framework tipos de dados
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player,.NET Framework
- Windows Media Player modelo de objeto,.NET Framework
- modelo de objeto, .NET Framework
- Windows Media Player Mobile,.NET Framework
- Windows Media Player ActiveX controle,.NET Framework
- Windows Media Player Controle ActiveX dispositivo móvel, .NET Framework
- ActiveX controle,.NET Framework
- .NET Framework, tipos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36854d971b0fc220f8f77b754b08b486ff93d339935bedcf33edca39fb701e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004507"
---
# <a name="about-net-framework-data-types"></a>Sobre .NET Framework tipos de dados

Esta seção contém as informações necessárias para converter a Referência de Modelo de Objeto orientada a script em tipos de dados .NET Framework Microsoft. A referência de script Windows Media Player tem quase todas as informações necessárias para usar o controle Windows Media Player em um programa baseado em .NET Framework e, na maioria dos casos, a sintaxe será semelhante à de outras linguagens de script, como o Microsoft JScript.

A Windows Media Player referência fornece o tipo JScript dados e, se necessário, a conversão C++. Por exemplo, um **Número** pode ser retornado por um método . JScript trata todos os números da mesma maneira, mas outras linguagens distinguem entre diferentes tipos de números (inteiro, ponto flutuante e assim por diante). A referência fornece a conversão C++ para tipos de dados de número porque os números podem ser processados de forma diferente pelo C++. Por exemplo, o C++ usa o **tipo de dados int** para aritmética de inteiro e **float para** ponto flutuante.

O .NET Framework usa um sistema ligeiramente diferente de tipos de dados base. A tabela a seguir mostra as diferenças nos tipos de dados comuns que você provavelmente usará. Para obter mais informações .NET Framework tipos de dados base e a conversão em outros sistemas de tipo de dados, consulte a discussão guia do desenvolvedor do .NET Framework sobre tipos de dados base do Namespace do Sistema.

Esta tabela fornece o nome .NET Framework classe e o tipo de dados C#. Os tipos de dados para outros idiomas são definidos para cada idioma em suas respectivas referências de idioma.



| Tipo de dados de script | Tipo de dados em C++     | .NET Framework classe (tipo de dados C#) |
|------------------|-------------------|---------------------------------------|
| **Número**       | **int**           | **Int32** (**int**)                   |
| **Número**       | **longo**          | **Int32** (**int**)                   |
| **Número**       | **double**        | **Double** (**double**)               |
| **Número**       | **float**         | **Single** (**float**)                |
| **Cadeia de caracteres**       | **BSTR**          | **Cadeia de** caracteres (**cadeia de caracteres**)               |
| **Booliano**      | **VARIANT \_ BOOL** | **Boolean** (**bool**)                |
| **Objeto**       | **Objeto**        | **Object** (**object**)               |



 

Se você estiver usando Visual Studio, poderá usar a tecnologia Microsoft IntelliSense para determinar qual tipo de dados é esperado para uma função específica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Incorporação do controle Windows Media Player em uma solução .NET Framework dados**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




