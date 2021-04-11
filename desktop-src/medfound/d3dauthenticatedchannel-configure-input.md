---
description: 'Contém dados de entrada para o método IDirect3DAuthenticatedChannel9:: Configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: Estrutura de D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164205"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a><span data-ttu-id="0d1ed-103">D3DAUTHENTICATEDCHANNEL \_ Configurar a \_ estrutura de entrada</span><span class="sxs-lookup"><span data-stu-id="0d1ed-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT structure</span></span>

<span data-ttu-id="0d1ed-104">Contém dados de entrada para o método [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="0d1ed-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d1ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d1ed-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a><span data-ttu-id="0d1ed-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0d1ed-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d1ed-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="0d1ed-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="0d1ed-108">Uma [**estrutura \_ OMAC do D3D**](d3d-omac.md) que contém um Message Authentication Code (Mac) dos dados.</span><span class="sxs-lookup"><span data-stu-id="0d1ed-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="0d1ed-109">O driver usa o MAC de CBC One-key baseado em AES (OMAC) para calcular esse valor para o bloco de dados que aparece após esse membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="0d1ed-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="0d1ed-110">**Configuratype**</span><span class="sxs-lookup"><span data-stu-id="0d1ed-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="0d1ed-111">Um GUID que especifica o comando.</span><span class="sxs-lookup"><span data-stu-id="0d1ed-111">A GUID that specifies the command.</span></span> <span data-ttu-id="0d1ed-112">Para obter uma lista de valores, consulte [proteção de conteúdo comandos](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="0d1ed-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d1ed-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="0d1ed-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="0d1ed-114">Um identificador para o canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="0d1ed-114">A handle to the authenticated channel.</span></span> <span data-ttu-id="0d1ed-115">Para obter o identificador, chame [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="0d1ed-115">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="0d1ed-116">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0d1ed-116">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="0d1ed-117">O número de sequência da consulta.</span><span class="sxs-lookup"><span data-stu-id="0d1ed-117">The query sequence number.</span></span> <span data-ttu-id="0d1ed-118">No início da sessão, gere um número aleatório de 32 bits de segurança criptograficamente seguro para usar como o número de sequência inicial.</span><span class="sxs-lookup"><span data-stu-id="0d1ed-118">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="0d1ed-119">Para cada comando, aumente o número de sequência em 1.</span><span class="sxs-lookup"><span data-stu-id="0d1ed-119">For each command, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d1ed-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d1ed-120">Requirements</span></span>



| <span data-ttu-id="0d1ed-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d1ed-121">Requirement</span></span> | <span data-ttu-id="0d1ed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0d1ed-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1ed-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d1ed-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1ed-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0d1ed-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0d1ed-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d1ed-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1ed-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="0d1ed-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d1ed-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d1ed-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1ed-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d1ed-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d1ed-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d1ed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1ed-130">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="0d1ed-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="0d1ed-131">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="0d1ed-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




