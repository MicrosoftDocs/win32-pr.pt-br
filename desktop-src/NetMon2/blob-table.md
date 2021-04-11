---
description: Contém uma matriz de BLOBs.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Estrutura de BLOB_TABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169381"
---
# <a name="blob_table-structure"></a><span data-ttu-id="4e652-103">Estrutura da tabela de BLOBs \_</span><span class="sxs-lookup"><span data-stu-id="4e652-103">BLOB\_TABLE structure</span></span>

<span data-ttu-id="4e652-104">A estrutura da **\_ tabela de BLOBs** contém uma matriz de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="4e652-104">The **BLOB\_TABLE** structure contains an array of BLOBs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e652-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e652-105">Syntax</span></span>


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a><span data-ttu-id="4e652-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4e652-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e652-107">**dwNumBlobs**</span><span class="sxs-lookup"><span data-stu-id="4e652-107">**dwNumBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="4e652-108">Indicador de que muitos BLOBs seguem.</span><span class="sxs-lookup"><span data-stu-id="4e652-108">Indicator that many BLOBs follow.</span></span>

</dd> <dt>

<span data-ttu-id="4e652-109">**hBlobs**</span><span class="sxs-lookup"><span data-stu-id="4e652-109">**hBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="4e652-110">Identificador para a matriz de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="4e652-110">Handle to the BLOB array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e652-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e652-111">Requirements</span></span>



| <span data-ttu-id="4e652-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e652-112">Requirement</span></span> | <span data-ttu-id="4e652-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4e652-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4e652-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e652-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4e652-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e652-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4e652-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e652-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4e652-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e652-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4e652-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e652-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e652-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e652-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




