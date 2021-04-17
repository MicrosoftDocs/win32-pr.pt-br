---
description: Contém dados de entrada para um \_ comando D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: Estrutura de D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813240"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a><span data-ttu-id="44b32-103">\_Estrutura D3DAUTHENTICATEDCHANNEL CONFIGURESHAREDRESOURCE</span><span class="sxs-lookup"><span data-stu-id="44b32-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE structure</span></span>

<span data-ttu-id="44b32-104">Contém dados de entrada para um comando [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="44b32-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) command.</span></span>

<span data-ttu-id="44b32-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="44b32-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="44b32-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44b32-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a><span data-ttu-id="44b32-107">Membros</span><span class="sxs-lookup"><span data-stu-id="44b32-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="44b32-108">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="44b32-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="44b32-109">Um [**D3DAUTHENTICATEDCHANNEL \_ configura \_**](d3dauthenticatedchannel-configure-input.md) a estrutura de entrada que contém o GUID de comando e outros dados.</span><span class="sxs-lookup"><span data-stu-id="44b32-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="44b32-110">**ProcessIdentiferType**</span><span class="sxs-lookup"><span data-stu-id="44b32-110">**ProcessIdentiferType**</span></span>
</dt> <dd>

<span data-ttu-id="44b32-111">Um valor de [**\_ PROCESSIDENTIFIERTYPE D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-processidentifiertype.md) que especifica o tipo de processo.</span><span class="sxs-lookup"><span data-stu-id="44b32-111">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span> <span data-ttu-id="44b32-112">Para especificar o processo de Gerenciador de Janelas da Área de Trabalho (DWM), defina esse membro como o **\_ DWM do ProcessId**.</span><span class="sxs-lookup"><span data-stu-id="44b32-112">To specify the Desktop Window Manager (DWM) process, set this member to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="44b32-113">Caso contrário, defina esse membro como **\_ identificador de processidtype** e defina o membro **ProcessHandle** como um identificador válido.</span><span class="sxs-lookup"><span data-stu-id="44b32-113">Otherwise, set this member to **PROCESSIDTYPE\_HANDLE** and set the **ProcessHandle** member to a valid handle.</span></span>

</dd> <dt>

<span data-ttu-id="44b32-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="44b32-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="44b32-115">Um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="44b32-115">A process handle.</span></span> <span data-ttu-id="44b32-116">Se o membro **ProcessIdentifier** for igual ao **\_ identificador PROCESSTIDTYPE**, o membro **ProcessHandle** especificará um identificador para um processo.</span><span class="sxs-lookup"><span data-stu-id="44b32-116">If the **ProcessIdentifier** member equals **PROCESSTIDTYPE\_HANDLE**, the **ProcessHandle** member specifies a handle to a process.</span></span> <span data-ttu-id="44b32-117">Caso contrário, o valor será ignorado.</span><span class="sxs-lookup"><span data-stu-id="44b32-117">Otherwise, the value is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="44b32-118">**AllowAccess**</span><span class="sxs-lookup"><span data-stu-id="44b32-118">**AllowAccess**</span></span>
</dt> <dd>

<span data-ttu-id="44b32-119">Se **for true**, o processo especificado terá acesso aos recursos compartilhados restritos.</span><span class="sxs-lookup"><span data-stu-id="44b32-119">If **TRUE**, the specified process has access to restricted shared resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44b32-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44b32-120">Requirements</span></span>



| <span data-ttu-id="44b32-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="44b32-121">Requirement</span></span> | <span data-ttu-id="44b32-122">Valor</span><span class="sxs-lookup"><span data-stu-id="44b32-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44b32-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44b32-123">Minimum supported client</span></span><br/> | <span data-ttu-id="44b32-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="44b32-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="44b32-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44b32-125">Minimum supported server</span></span><br/> | <span data-ttu-id="44b32-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="44b32-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="44b32-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44b32-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="44b32-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="44b32-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44b32-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="44b32-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b32-130">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="44b32-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="44b32-131">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="44b32-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




