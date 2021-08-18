---
description: A política de metadados de foto para a propriedade System. Photo. TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Política de metadados de foto System. Photo. TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e78086284e1ca13b01c5e7cd188b761afe7eeba8acb5f2bca103234f80955b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964755"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>Política de metadados de foto System. Photo. TranscodedForSync

A política de metadados de foto para a propriedade [System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ TranscodedForSync

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

BOOL do VT \_

### <a name="input-type"></a>Tipo de entrada

Booliano.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                  | Formato de disco  |
|-------|---------------------------------------|--------------|
| 1     | /App1/IFD/{UShort = 18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                  | Formato de disco  |
|-------|---------------------------------------|--------------|
| 1     | /App1/IFD/{UShort = 18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                  |
|-------|---------------------------------------|
| 1     | /App1/IFD/{UShort = 18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                      | Formato de disco  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{UShort = 18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                      | Formato de disco  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{UShort = 18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                      |
|-------|-------------------------------------------|
| 1     | /IFD/{UShort = 18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
