---
title: ODJ_BLOB
description: ODJ_BLOB IDL Definition
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: aa1c2b593e0e9f63a52672eb3b29ee83fbf86ea91d7f4860f2351a8e4538f05d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779566"
---
# <a name="odj_blob-structure"></a>ODJ_BLOB estrutura

Especifica uma estrutura que contém uma estrutura ODJ_WIN7BLOB serializada ou uma estrutura OP_PACKAGE serializada.

## <a name="syntax"></a>Sintaxe

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>Membros

### <a name="ulodjformat"></a>ulODJFormat

Especifica a versão lógica da estrutura e deve ser definida como um dos seguintes valores:

|Valor|Significado|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|Os bytes contidos em pBlob devem conter uma estrutura ODJ_WIN7_BLOB serializada.|
|ODJ_WIN8_FORMAT (0x00000002)|Os bytes contidos em pBlob devem conter uma estrutura OP_PACKAGE serializada.|

### <a name="cbblob"></a>cbBlob

Isso deve ser definido como o número de bytes na matriz pBlob.

### <a name="pblob"></a>pBlob

Aponta para um buffer de byte que contém uma estrutura serializada, conforme especificado por ulODJFormat acima.

## <a name="see-also"></a>Confira também

[**Definições de IDL de Junção de Domínio Offline**](odj-idl.md)

