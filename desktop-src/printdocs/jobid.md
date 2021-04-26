---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2d77d185ab7edc611a82f94a2ce92428d9f167
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998133"
---
# <a name="jobid"></a>JobID

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica uma ID exclusiva para o trabalho.

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

A estrutura XML desse elemento é:

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                      | Tipo de dados         | Unidade | Valores com suporte | Resumo |
|---------------------------|-------------------|------|------------------|---------|
| \_JobIDValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




