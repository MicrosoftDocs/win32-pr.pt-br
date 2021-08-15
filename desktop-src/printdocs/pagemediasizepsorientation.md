---
description: Obter informações sobre o parâmetro PageMediaSizePSOrientation. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9070be6fdbd5129ff3ea63be368763c7547982331ee47ebdad6e8b0e43f2f4a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868181"
---
# <a name="pagemediasizepsorientation"></a>PageMediaSizePSOrientation

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica a orientação em relação à direção da orientação do feed (Referência PostScript especificação de formato de arquivo de [descrição da impressora).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)

-   [Informações do elemento](#element-information)
-   [Conteúdo da estrutura](#structure-content)

## <a name="element-information"></a>Informações do elemento



| Nome | Valor |
|----------------------------|-------------------------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                                     |
| Prefixo de definição de scoping <br/> | ?<br/>                                             |
| Observações <br/>          | Vinculado ao elemento PageMediaSize, opção CustomPS<br/> |



 

## <a name="structure-content"></a>Conteúdo da estrutura

A estrutura XML desse elemento é:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propriedades da estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Propriedade                | xsi:type           | Valor                        |
|-------------------------|--------------------|------------------------------|
| Tipo de dados<br/>     | string<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | inteiro<br/> | 0<br/>                 |
| MaxValue<br/>     | Número inteiro<br/> | 3<br/>                 |
| Minvalue<br/>     | inteiro<br/> | 0<br/>                 |
| Obrigatório<br/>    | string<br/>  | psk:Conditional<br/>   |
| Vários<br/>     | integer<br/> | 1<br/>                 |
| Unittype<br/>     | string<br/>  | PageMediaSizeEnum<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[PostScript Especificação de formato de arquivo de descrição da impressora](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




