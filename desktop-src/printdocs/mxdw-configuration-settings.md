---
description: O Microsoft XPS Document Writer (MXDW) permite que os usuários criem arquivos de documento XPS Imprimindo de qualquer aplicativo do Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Definições de configuração do MXDW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105810958"
---
# <a name="mxdw-configuration-settings"></a>Definições de configuração do MXDW

O Microsoft XPS Document Writer (MXDW) permite que os usuários criem arquivos de documento XPS Imprimindo de qualquer aplicativo do Windows. Os desenvolvedores de aplicativos podem controlar as seguintes configurações de saída do MXDW usando as partes PrintTicket e PrintCapabilities do [esquema de impressão](./printschema.md).

## <a name="jobinterleaving"></a>JobInterleaving

A configuração JobInterleaving controla a ordem de intercalação de conteúdo para os documentos XPS. Para obter informações sobre intercalação de trabalhos, consulte a [especificação de papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf). O MXDW dá suporte às duas opções a seguir para essa configuração:

-   **Off** -esta opção desabilita a intercalação para que todos os dados de cada elemento de conteúdo no documento sejam contíguos, o que melhora a eficiência do acesso aleatório. Essa opção é melhor para exibir um documento XPS.
-   A opção **on** -this permite a intercalação para que os dados de cada elemento de conteúdo sejam divididos e reordenados para um processamento sequencial mais eficiente. Essa opção é melhor para download e impressão na Web.

O exemplo a seguir é um exemplo do XML de PrintCapabilities que inclui a configuração JobInterleaving.


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



O XML PrintTicket é semelhante, exceto que ele especifica uma opção específica. Consulte o [esquema de impressão](./printschema.md) para obter detalhes.

Como JobInterleaving não é uma das [palavras-chave públicas do esquema de impressão](./print-schema-public-keywords.md), você deve incluir uma declaração do namespace (neste caso, "ns0000" na marca **PrintCapabilities** (ou **PrintTicket**) no início do documento PrintCapabilities (ou PrintTicket), conforme mostrado no exemplo a seguir:


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>JobImageType

JobImageType controla o formato de saída dos formatos de bitmap inseridos. O MXDW dá suporte às quatro opções a seguir para essa configuração:

-   **JPEGHigh** -essa opção especifica a imagem JPEG com um alto nível de compactação. Essa opção produz o menor tamanho de arquivo, mas a qualidade de imagem mais baixa.
-   **JPEGMed** -essa opção especifica a imagem JPEG com um nível médio de compactação. Essa opção fornece o melhor equilíbrio entre o tamanho do arquivo e a qualidade da imagem.
-   **JPEGLow** -essa opção especifica a imagem JPEG com um baixo nível de compactação. Essa opção produz a redução mínima no tamanho do arquivo e a alta qualidade da imagem.
-   **Png** -essa opção especifica o formato de imagem png com compactação sem perdas. Essa opção produz o maior tamanho de arquivo e a qualidade de imagem mais alta.

O XML de PrintCapabilities da configuração JobImageType aparece abaixo:


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



O XML PrintTicket é semelhante, exceto que ele especifica uma opção específica. Consulte o [esquema de impressão](./printschema.md) para obter detalhes.

Como JobImageType não é uma das [palavras-chave públicas do esquema de impressão](./print-schema-public-keywords.md), você deve incluir uma declaração do namespace (neste caso, "ns0000" na marca **PrintCapabilities** (ou **PrintTicket**) no início do documento PrintCapabilities (ou PrintTicket), conforme mostrado no exemplo a seguir:


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Imprimir esquema](./printschema.md)
</dt> <dt>

[Downloads de licença e de especificação XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
