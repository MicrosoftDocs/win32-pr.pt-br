---
title: ODJ_BLOB
description: Definição de IDL de ODJ_BLOB
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104454437"
---
# <a name="odj_blob-structure"></a>Estrutura de ODJ_BLOB

Especifica uma estrutura que contém uma estrutura de ODJ_WIN7BLOB serializada ou uma estrutura de OP_PACKAGE serializada.

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
|ODJ_WIN7_FORMAT (0x00000001)|Os bytes contidos em pBlob devem conter uma estrutura de ODJ_WIN7_BLOB serializada.|
|ODJ_WIN8_FORMAT (0x00000002)|Os bytes contidos em pBlob devem conter uma estrutura de OP_PACKAGE serializada.|

### <a name="cbblob"></a>cbBlob

Isso deve ser definido como o número de bytes na matriz pBlob.

### <a name="pblob"></a>pBlob

Aponta para um buffer de bytes que contém uma estrutura serializada, conforme especificado por ulODJFormat acima.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

