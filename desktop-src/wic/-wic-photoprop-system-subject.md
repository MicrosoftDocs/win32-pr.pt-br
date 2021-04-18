---
description: A política de metadados de foto para a propriedade System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Política de metadados de foto System. Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789234"
---
# <a name="systemsubject-photo-metadata-policy"></a>Política de metadados de foto System. Subject

A política de metadados de foto para a propriedade [System. Subject](../properties/props-system-subject.md) .

### <a name="pkey"></a>PKEY

Assunto do PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

Uma VT \_ LPWSTR ou VT \_ LPWSTR

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40095} | \_bytes Unicode |
| 2     | /App1/IFD/{UShort = 270}   | ascii          |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40095} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/{UShort = 40095} |
| 2     | /App1/IFD/{UShort = 270}   |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{UShort = 40095} | \_bytes Unicode |
| 2     | /IFD/{UShort = 270}   | ascii          |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{UShort = 40095} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                |
|-------|---------------------|
| 1     | /IFD/{UShort = 40095} |
| 2     | /IFD/{UShort = 270}   |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema. Subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
