---
description: Obter informações sobre o parâmetro PageMediaSizePSHeightOffset. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a904b8e1d1ef9f917dae96d863563eff2b5bc8e6dd7b43a0e1d24783eb87077e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471039"
---
# <a name="pagemediasizepsheightoffset"></a>PageMediaSizePSHeightOffset

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica o deslocamento, paralelo à direção da orientação do feed (Referência PostScript especificação de formato de arquivo de descrição [da impressora).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)

-   [Informações do elemento](#element-information)
-   [Conteúdo da estrutura](#structure-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|-------------------------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                                     |
| Prefixo de definição de scoping <br/> | ?<br/>                                             |
| Observações <br/>          | Vinculado ao elemento PageMediaSize, opção CustomPS<br/> |



 

## <a name="structure-content"></a>Conteúdo da estrutura

A estrutura XML desse elemento é:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeightOffset">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propriedades da estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Propriedade                | xsi:type           | Valor                      |
|-------------------------|--------------------|----------------------------|
| Tipo de dados<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | Número inteiro<br/> | não definido<br/>       |
| MaxValue<br/>     | Número inteiro<br/> | não definido<br/>       |
| Minvalue<br/>     | Número inteiro<br/> | não definido<br/>       |
| Obrigatório<br/>    | string<br/>  | psk:Conditional<br/> |
| Vários<br/>     | integer<br/> | 1<br/>               |
| Unittype<br/>     | string<br/>  | Mícrons<br/>         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[PostScript Especificação de formato de arquivo de descrição da impressora](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




