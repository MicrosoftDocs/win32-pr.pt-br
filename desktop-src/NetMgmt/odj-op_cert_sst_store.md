---
title: OP_CERT_SST_STORE
description: Definição de IDL de OP_CERT_SST_STORE
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104369004"
---
# <a name="op_cert_sst_store-structure"></a><span data-ttu-id="8b170-103">Estrutura de OP_CERT_SST_STORE</span><span class="sxs-lookup"><span data-stu-id="8b170-103">OP_CERT_SST_STORE structure</span></span>

<span data-ttu-id="8b170-104">Contém um repositório de certificados serializado.</span><span class="sxs-lookup"><span data-stu-id="8b170-104">Contains a serialized certificate store.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b170-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b170-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a><span data-ttu-id="8b170-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8b170-106">Members</span></span>

### <a name="storelocation"></a><span data-ttu-id="8b170-107">StoreLocation</span><span class="sxs-lookup"><span data-stu-id="8b170-107">StoreLocation</span></span>

<span data-ttu-id="8b170-108">Contém um identificador para o repositório de certificados de [**locais de armazenamento do sistema**](../seccrypto/system-store-locations.md).</span><span class="sxs-lookup"><span data-stu-id="8b170-108">Contains an identifier for the certificate store from [**System Store Locations**](../seccrypto/system-store-locations.md).</span></span>

### <a name="pstorename"></a><span data-ttu-id="8b170-109">pStoreName</span><span class="sxs-lookup"><span data-stu-id="8b170-109">pStoreName</span></span>

<span data-ttu-id="8b170-110">Contém o nome da loja.</span><span class="sxs-lookup"><span data-stu-id="8b170-110">Contains the name of the store.</span></span>

### <a name="cbsst"></a><span data-ttu-id="8b170-111">cbSst</span><span class="sxs-lookup"><span data-stu-id="8b170-111">cbSst</span></span>

<span data-ttu-id="8b170-112">Contém o tamanho de pSst em bytes.</span><span class="sxs-lookup"><span data-stu-id="8b170-112">Contains the size of pSst in bytes.</span></span>

### <a name="psst"></a><span data-ttu-id="8b170-113">pSst</span><span class="sxs-lookup"><span data-stu-id="8b170-113">pSst</span></span>

<span data-ttu-id="8b170-114">Contém um repositório de certificados serializado (consulte [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="8b170-114">Contains a serialized certificate store (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="8b170-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b170-115">See also</span></span>

[<span data-ttu-id="8b170-116">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="8b170-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)