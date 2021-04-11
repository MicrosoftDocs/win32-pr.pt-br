---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014213bdd2e11cc2587cef580a0b48fe03172ef0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172579"
---
# <a name="pageicmrenderingintent"></a>PageICMRenderingIntent

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve a tentativa de renderização conforme definido pela especificação ICC v2. Esse valor deve ser ignorado se uma imagem ou elemento gráfico tiver um perfil inserido que especifica a tentativa de renderização.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [Conteúdo de linguagem XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Nome                       |                    |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Recurso<br/> |
| Prefixo de escopo <br/> | ?<br/>    |
| Observações <br/>          | Nenhum <br/>   |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                               | Tipo de dados         | Unidade                  | Valores com suporte                                                                                                                                                                      | Resumo                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | characters<br/> | Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define uma opção que, quando selecionada, desabilita esse recurso.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace. O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




