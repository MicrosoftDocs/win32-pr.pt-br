---
description: A política de metadados de foto para a propriedade System.Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Política de metadados de foto System.Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9321e866c34027df3e932f84d532162def959cbaf365bb4020c19647d547adea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881966"
---
# <a name="systemsubject-photo-metadata-policy"></a>Política de metadados de foto System.Subject

A política de metadados de foto para a [propriedade System.Subject.](../properties/props-system-subject.md)

### <a name="pkey"></a>Pkey

Assunto \_ PKEY

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ LPWSTR ou VT \_ LPWSTR

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort=40095} | Bytes \_ unicode |
| 2     | /app1/ifd/{ushort=270}   | ascii          |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort=40095} | Bytes \_ unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /app1/ifd/{ushort=40095} |
| 2     | /app1/ifd/{ushort=270}   |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort=40095} | Bytes \_ unicode |
| 2     | /ifd/{ushort=270}   | ascii          |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort=40095} | Bytes \_ unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                |
|-------|---------------------|
| 1     | /ifd/{ushort=40095} |
| 2     | /ifd/{ushort=270}   |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
