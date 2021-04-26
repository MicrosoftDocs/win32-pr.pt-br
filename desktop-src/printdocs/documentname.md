---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: DocumentName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66809ef18edb7aa313ea5218f9122acf4ddd1ee8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997793"
---
# <a name="documentname"></a>DocumentName

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica um nome descritivo para o documento.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [Conteúdo de linguagem XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Nome | Valor |
|----------------------------|---------------------|
| Tipo de elemento <br/>   | Propriedade<br/> |
| Prefixo de escopo <br/> | Documento<br/> |
| Observações <br/>          | Nenhum<br/>     |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é a seguinte:

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                             | Tipo de dados         | Unidade | Valores com suporte | Resumo |
|----------------------------------|-------------------|------|------------------|---------|
| \_DocumentNameValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




