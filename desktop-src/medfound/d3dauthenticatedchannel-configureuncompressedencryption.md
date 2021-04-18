---
description: Contém dados de entrada para o \_ comando D3DAUTHENTICATEDCONFIGURE ENCRYPTIONWHENACCESSIBLE.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: Estrutura de D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c8ea4360ff7f2bbcf2c03040671013473e9873a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807175"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a><span data-ttu-id="5b8c7-103">\_Estrutura D3DAUTHENTICATEDCHANNEL CONFIGUREUNCOMPRESSEDENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="5b8c7-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION structure</span></span>

<span data-ttu-id="5b8c7-104">Contém dados de entrada para o comando [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .</span><span class="sxs-lookup"><span data-stu-id="5b8c7-104">Contains input data for the [**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) command.</span></span>

<span data-ttu-id="5b8c7-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="5b8c7-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b8c7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b8c7-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a><span data-ttu-id="5b8c7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5b8c7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b8c7-108">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="5b8c7-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="5b8c7-109">Um [**D3DAUTHENTICATEDCHANNEL \_ configura \_**](d3dauthenticatedchannel-configure-input.md) a estrutura de entrada que contém o GUID de comando e outros dados.</span><span class="sxs-lookup"><span data-stu-id="5b8c7-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="5b8c7-110">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="5b8c7-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="5b8c7-111">Um GUID que especifica o tipo de criptografia a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="5b8c7-111">A GUID that specifies the type of encryption to apply.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b8c7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b8c7-112">Requirements</span></span>



| <span data-ttu-id="5b8c7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b8c7-113">Requirement</span></span> | <span data-ttu-id="5b8c7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5b8c7-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b8c7-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b8c7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5b8c7-116">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5b8c7-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5b8c7-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b8c7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5b8c7-118">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5b8c7-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5b8c7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b8c7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b8c7-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b8c7-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b8c7-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b8c7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b8c7-122">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="5b8c7-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="5b8c7-123">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="5b8c7-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




