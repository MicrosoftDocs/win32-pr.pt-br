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
# <a name="op_package-structure"></a><span data-ttu-id="17639-103">Estrutura de OP_PACKAGE</span><span class="sxs-lookup"><span data-stu-id="17639-103">OP_PACKAGE structure</span></span>

<span data-ttu-id="17639-104">Contém uma estrutura que contém uma OP_PACKAGE_COLLECTION serializada.</span><span class="sxs-lookup"><span data-stu-id="17639-104">Contains a structure that contains a serialized OP_PACKAGE_COLLECTION.</span></span>

## <a name="syntax"></a><span data-ttu-id="17639-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17639-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="17639-106">Membros</span><span class="sxs-lookup"><span data-stu-id="17639-106">Members</span></span>

### <a name="encryptiontype"></a><span data-ttu-id="17639-107">EncryptionType</span><span class="sxs-lookup"><span data-stu-id="17639-107">EncryptionType</span></span>

<span data-ttu-id="17639-108">Reservado para uso futuro e deve ser definido como GUID_NULL.</span><span class="sxs-lookup"><span data-stu-id="17639-108">Reserved for future use and MUST be set to GUID_NULL.</span></span>

### <a name="encryptioncontext"></a><span data-ttu-id="17639-109">EncryptionContext</span><span class="sxs-lookup"><span data-stu-id="17639-109">EncryptionContext</span></span>

<span data-ttu-id="17639-110">Reservado para uso futuro e deve ser definido como todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="17639-110">Reserved for future use and MUST be set to all zeros.</span></span>

### <a name="wrappedpartcollection"></a><span data-ttu-id="17639-111">WrappedPartCollection</span><span class="sxs-lookup"><span data-stu-id="17639-111">WrappedPartCollection</span></span>

<span data-ttu-id="17639-112">Uma estrutura de OP_BLOB que contém uma estrutura de OP_PACKAGE_COLLECTION serializada.</span><span class="sxs-lookup"><span data-stu-id="17639-112">An OP_BLOB structure that contains a serialized OP_PACKAGE_COLLECTION structure.</span></span>

### <a name="cbdecryptedpartcollection"></a><span data-ttu-id="17639-113">cbDecryptedPartCollection</span><span class="sxs-lookup"><span data-stu-id="17639-113">cbDecryptedPartCollection</span></span>

<span data-ttu-id="17639-114">Reservado para uso futuro e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="17639-114">Reserved for future use and MUST be set to zero.</span></span>

### <a name="extension"></a><span data-ttu-id="17639-115">Extensão</span><span class="sxs-lookup"><span data-stu-id="17639-115">Extension</span></span>

<span data-ttu-id="17639-116">Reservado para uso futuro e deve ser definido como todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="17639-116">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="17639-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="17639-117">See also</span></span>

[<span data-ttu-id="17639-118">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="17639-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="17639-119">**BLOB de OP \_**</span><span class="sxs-lookup"><span data-stu-id="17639-119">**OP\_BLOB**</span></span>](odj-op_blob.md)

[<span data-ttu-id="17639-120">**\_coleção de pacotes de op \_**</span><span class="sxs-lookup"><span data-stu-id="17639-120">**OP\_PACKAGE\_COLLECTION**</span></span>](odj-op_package_collection.md)
