---
title: OP_PACKAGE
description: Definição de IDL de OP_PACKAGE
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "105790658"
---
# <a name="op_package-structure"></a>Estrutura de OP_PACKAGE

Contém uma estrutura que contém uma OP_PACKAGE_COLLECTION serializada.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a>Membros

### <a name="encryptiontype"></a>EncryptionType

Reservado para uso futuro e deve ser definido como GUID_NULL.

### <a name="encryptioncontext"></a>EncryptionContext

Reservado para uso futuro e deve ser definido como todos os zeros.

### <a name="wrappedpartcollection"></a>WrappedPartCollection

Uma estrutura de OP_BLOB que contém uma estrutura de OP_PACKAGE_COLLECTION serializada.

### <a name="cbdecryptedpartcollection"></a>cbDecryptedPartCollection

Reservado para uso futuro e deve ser definido como zero.

### <a name="extension"></a>Extensão

Reservado para uso futuro e deve ser definido como todos os zeros.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**BLOB de OP \_**](odj-op_blob.md)

[**\_coleção de pacotes de op \_**](odj-op_package_collection.md)
