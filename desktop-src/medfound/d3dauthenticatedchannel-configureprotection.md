---
description: Contém dados de entrada para um \_ comando de proteção D3DAUTHENTICATEDCONFIGURE.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: Estrutura de D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fc1daee7bfd9320539a03974ab431c4ba588d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826734"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a><span data-ttu-id="f746b-103">\_Estrutura D3DAUTHENTICATEDCHANNEL CONFIGUREPROTECTION</span><span class="sxs-lookup"><span data-stu-id="f746b-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREPROTECTION structure</span></span>

<span data-ttu-id="f746b-104">Contém dados de entrada para um comando de [**\_ proteção D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="f746b-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_PROTECTION**](d3dauthenticatedconfigure-protection.md) command.</span></span>

<span data-ttu-id="f746b-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="f746b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="f746b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f746b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a><span data-ttu-id="f746b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f746b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f746b-108">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="f746b-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="f746b-109">Um [**D3DAUTHENTICATEDCHANNEL \_ configura \_**](d3dauthenticatedchannel-configure-input.md) a estrutura de entrada que contém o GUID de comando e outros dados.</span><span class="sxs-lookup"><span data-stu-id="f746b-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="f746b-110">**Proteções**</span><span class="sxs-lookup"><span data-stu-id="f746b-110">**Protections**</span></span>
</dt> <dd>

<span data-ttu-id="f746b-111">Uma estrutura de [**\_ \_ sinalizadores de proteção D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) que especifica o nível de proteção.</span><span class="sxs-lookup"><span data-stu-id="f746b-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f746b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f746b-112">Requirements</span></span>



| <span data-ttu-id="f746b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f746b-113">Requirement</span></span> | <span data-ttu-id="f746b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f746b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f746b-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f746b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f746b-116">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f746b-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f746b-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f746b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f746b-118">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f746b-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f746b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f746b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f746b-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f746b-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f746b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f746b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f746b-122">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f746b-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="f746b-123">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="f746b-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




