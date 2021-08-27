---
description: Saiba mais sobre o elemento JobName, que especifica um nome descritivo para o trabalho. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc05451cce8994a77017f2ff905698ad8a58ee67ef2895f7ed0b692388971b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112366"
---
# <a name="jobname"></a>JobName

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica um nome descritivo para o trabalho.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [Conteúdo de linguagem XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Nome | Valor |
|----------------------------|---------------------|
| Tipo de elemento <br/>   | Propriedade<br/> |
| Prefixo de escopo <br/> | Trabalho<br/>      |
| Observações <br/>          | Nenhum<br/>     |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é a seguinte:

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                        | Tipo de dados         | Unidade | Valores com suporte | Resumo |
|-----------------------------|-------------------|------|------------------|---------|
| \_JobNameValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




