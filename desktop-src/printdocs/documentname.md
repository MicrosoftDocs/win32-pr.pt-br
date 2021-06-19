---
description: Saiba mais sobre a propriedade DocumentName, que especifica um nome descritivo para o documento.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: Documentname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202ff1f5bac85fec3feac9f141834adfcd37e70
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409269"
---
# <a name="documentname"></a>Documentname

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica um nome descritivo para o documento.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [linguagem XML conteúdo (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|---------------------|
| Tipo de elemento <br/>   | Propriedade<br/> |
| Prefixo de definição de scoping <br/> | Documento<br/> |
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



 

## <a name="extensible-markup-language-xml-content"></a>linguagem XML conteúdo (XML)

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




