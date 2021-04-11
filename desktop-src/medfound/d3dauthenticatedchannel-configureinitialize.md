---
description: Contém dados de entrada para um \_ comando de inicialização D3DAUTHENTICATEDCONFIGURE.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: Estrutura de D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010319"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a><span data-ttu-id="bad6a-103">\_Estrutura D3DAUTHENTICATEDCHANNEL CONFIGUREINITIALIZE</span><span class="sxs-lookup"><span data-stu-id="bad6a-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE structure</span></span>

<span data-ttu-id="bad6a-104">Contém dados de entrada para um comando de [**\_ inicialização D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="bad6a-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) command.</span></span>

<span data-ttu-id="bad6a-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="bad6a-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="bad6a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bad6a-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a><span data-ttu-id="bad6a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="bad6a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bad6a-108">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="bad6a-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="bad6a-109">Um [**D3DAUTHENTICATEDCHANNEL \_ configura \_**](d3dauthenticatedchannel-configure-input.md) a estrutura de entrada que contém o GUID de comando e outros dados.</span><span class="sxs-lookup"><span data-stu-id="bad6a-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="bad6a-110">**StartSequenceQuery**</span><span class="sxs-lookup"><span data-stu-id="bad6a-110">**StartSequenceQuery**</span></span>
</dt> <dd>

<span data-ttu-id="bad6a-111">O número de sequência inicial para consultas.</span><span class="sxs-lookup"><span data-stu-id="bad6a-111">The initial sequence number for queries.</span></span>

</dd> <dt>

<span data-ttu-id="bad6a-112">**StartSequenceConfigure**</span><span class="sxs-lookup"><span data-stu-id="bad6a-112">**StartSequenceConfigure**</span></span>
</dt> <dd>

<span data-ttu-id="bad6a-113">O número de sequência inicial para comandos.</span><span class="sxs-lookup"><span data-stu-id="bad6a-113">The initial sequence number for commands.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bad6a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bad6a-114">Remarks</span></span>

<span data-ttu-id="bad6a-115">Os membros **StartSequenceQuery** e **StartSequenceConfigure** contêm um número aleatório de 32 bits de segurança criptograficamente seguro.</span><span class="sxs-lookup"><span data-stu-id="bad6a-115">The **StartSequenceQuery** and **StartSequenceConfigure** members each contain a cryptographically secure 32-bit random number.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad6a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bad6a-116">Requirements</span></span>



| <span data-ttu-id="bad6a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad6a-117">Requirement</span></span> | <span data-ttu-id="bad6a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bad6a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bad6a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bad6a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bad6a-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bad6a-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bad6a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bad6a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bad6a-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bad6a-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bad6a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bad6a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bad6a-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad6a-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad6a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bad6a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad6a-126">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="bad6a-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="bad6a-127">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="bad6a-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




