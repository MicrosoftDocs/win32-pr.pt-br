---
description: Define a estrutura do arquivo de cabeçalho de Monitor de Rede.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Estrutura de CAPTUREFILE_HEADER_VALUES (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752019"
---
# <a name="capturefile_header_values-structure"></a><span data-ttu-id="7cbe6-103">Estrutura de \_ valores de cabeçalho de captura \_</span><span class="sxs-lookup"><span data-stu-id="7cbe6-103">CAPTUREFILE\_HEADER\_VALUES structure</span></span>

<span data-ttu-id="7cbe6-104">A estrutura de **\_ \_ valores de cabeçalho** do arquivo de captura define a estrutura do arquivo de cabeçalho monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-104">The **CAPTUREFILE\_HEADER\_VALUES** structure defines the Network Monitor header file structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbe6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cbe6-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a><span data-ttu-id="7cbe6-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7cbe6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7cbe6-107">**Signature**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-107">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-108">Identificador exclusivo: ' GMBU.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-108">Unique identifier: 'GMBU.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-109">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-109">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-110">Binary, decimal codificado (secundário).</span><span class="sxs-lookup"><span data-stu-id="7cbe6-110">Binary, coded decimal (minor).</span></span> <span data-ttu-id="7cbe6-111">O valor desse membro deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="7cbe6-111">The value of this member should be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-112">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-112">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-113">Decimal codificado em binário (principal).</span><span class="sxs-lookup"><span data-stu-id="7cbe6-113">Binary coded decimal (major).</span></span> <span data-ttu-id="7cbe6-114">Esse valor deve ser 2.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-114">This value should be 2.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-116">Tipo de topologia.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-116">Topology type.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-117">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-118">Hora da captura.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-118">Time of capture.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-119">**FrameTableOffset**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-119">**FrameTableOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-120">Tabela de índice de quadro.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-120">Frame index table.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-121">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-121">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-122">Tamanho da tabela do índice do quadro.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-122">Frame index table size.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-123">**UserDataOffset**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-123">**UserDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-124">Deslocamento de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-124">User data offset.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-125">**UserDataLength**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-125">**UserDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-126">Comprimento dos dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-126">User data length.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-127">**CommentDataOffset**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-127">**CommentDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-128">Deslocamento de dados de comentário.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-128">Comment data offset.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-129">**CommentDataLength**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-129">**CommentDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-130">Comprimento dos dados do comentário.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-130">Length of comment data.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-131">**StatisticsOffset**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-131">**StatisticsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-132">Deslocamento para a estrutura de **estatísticas** .</span><span class="sxs-lookup"><span data-stu-id="7cbe6-132">Offset to the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-133">**StatisticsLength**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-133">**StatisticsLength**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-134">Comprimento da estrutura de **estatísticas** .</span><span class="sxs-lookup"><span data-stu-id="7cbe6-134">Length of the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-135">**NetworkInfoOffset**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-135">**NetworkInfoOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-136">Deslocamento para a estrutura **NETWORKINFO** .</span><span class="sxs-lookup"><span data-stu-id="7cbe6-136">Offset to the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-137">**NetworkInfoLength**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-137">**NetworkInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-138">Comprimento da estrutura **NETWORKINFO** .</span><span class="sxs-lookup"><span data-stu-id="7cbe6-138">Length of the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-139">**ConversationStatsOffset**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-139">**ConversationStatsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-140">Este membro não é usado.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-140">This member is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-141">**ConversationStatsLength**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-141">**ConversationStatsLength**</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-142">Este membro não é usado.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-142">This member is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7cbe6-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cbe6-143">Requirements</span></span>



| <span data-ttu-id="7cbe6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cbe6-144">Requirement</span></span> | <span data-ttu-id="7cbe6-145">Valor</span><span class="sxs-lookup"><span data-stu-id="7cbe6-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbe6-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cbe6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7cbe6-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7cbe6-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7cbe6-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cbe6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7cbe6-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7cbe6-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7cbe6-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7cbe6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cbe6-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cbe6-151"><dt>Netmon.h</dt></span></span> </dl> |



 

 




