---
description: A política de metadados de foto para a propriedade System. Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Política de metadados de foto System. Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3e17190205b3df5c2ede9b1a7db231d0fdbbe21
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882696"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Política de metadados de foto System. Copyright

A política de metadados de foto para a propriedade [System. Copyright](../properties/props-system-copyright.md) .

### <a name="pkey"></a>PKEY

\_Direitos autorais do PKEY

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

String

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Order | Caminho                                      | Formato de disco |
|-------|-------------------------------------------|-------------|
|       | /App1/IFD/{UShort = 33432}                  | ascii       |
|       | aviso de/app13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /XMP/ &lt; xmpalt &gt; DC: direitos              | Unicode     |
|       | /XMP/DC: direitos                            | Unicode     |
|       | aviso de/app13/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                      | Formato de disco |
|-------|-------------------------------------------|-------------|
|       | /XMP/DC: direitos                            | Unicode     |
|       | /XMP/ &lt; xmpalt &gt; DC: direitos              | Unicode     |
|       | aviso de/app13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /App1/IFD/{UShort = 33432}                  | ascii       |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                      |
|-------|-------------------------------------------|
|       | /XMP/DC: direitos                            |
|       | aviso de/app13/IRB/8bimiptc/IPTC/Copyright |
|       | /App1/IFD/{UShort = 33432}                  |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Order | Caminho                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
|       | /IFD/{UShort = 33432}                     | ascii       |
|       | aviso de/IFD/IPTC/Copyright              |             |
|       | /IFD/XMP/ &lt; xmpalt &gt; DC: direitos        | Unicode     |
|       | /IFD/XMP/DC: direitos                      | Unicode     |
|       | aviso de/IFD/IPTC/Copyright              |             |
|       | aviso de/IFD/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
|       | /IFD/XMP/DC: direitos                      | Unicode     |
|       | /IFD/XMP/ &lt; xmpalt &gt; DC: direitos        | Unicode     |
|       | aviso de/IFD/IPTC/Copyright              |             |
|       | aviso de/IFD/IRB/8bimiptc/IPTC/Copyright |             |
|       | /IFD/{UShort = 33432}                     | ascii       |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                    |
|-------|-----------------------------------------|
|       | /IFD/XMP/DC: direitos                      |
|       | aviso de/IFD/IPTC/Copyright              |
|       | aviso de/IFD/IRB/8bimiptc/IPTC/Copyright |
|       | /IFD/{UShort = 33432}                     |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
