---
description: Contém a resposta a uma \_ consulta D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: Estrutura de D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089759"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a><span data-ttu-id="a8c6d-103">Estrutura de saída do D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_</span><span class="sxs-lookup"><span data-stu-id="a8c6d-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT structure</span></span>

<span data-ttu-id="a8c6d-104">Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c6d-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="a8c6d-105">Para enviar essa consulta, chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="a8c6d-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c6d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8c6d-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="a8c6d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a8c6d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8c6d-108">**Saída**</span><span class="sxs-lookup"><span data-stu-id="a8c6d-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="a8c6d-109">Uma estrutura de [**\_ \_ saída de consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contém um Message Authentication Code (Mac) e outros dados.</span><span class="sxs-lookup"><span data-stu-id="a8c6d-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="a8c6d-110">**ProcessIndex**</span><span class="sxs-lookup"><span data-stu-id="a8c6d-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a8c6d-111">O índice do processo na lista de processos.</span><span class="sxs-lookup"><span data-stu-id="a8c6d-111">The index of the process in the list of processes.</span></span>

</dd> <dt>

<span data-ttu-id="a8c6d-112">**ProcessIdentifer**</span><span class="sxs-lookup"><span data-stu-id="a8c6d-112">**ProcessIdentifer**</span></span>
</dt> <dd>

<span data-ttu-id="a8c6d-113">Um valor de [**\_ PROCESSIDENTIFIERTYPE D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-processidentifiertype.md) que especifica o tipo de processo.</span><span class="sxs-lookup"><span data-stu-id="a8c6d-113">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span>

</dd> <dt>

<span data-ttu-id="a8c6d-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="a8c6d-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a8c6d-115">Um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="a8c6d-115">A process handle.</span></span> <span data-ttu-id="a8c6d-116">Se o membro **ProcessIdentifier** for igual ao **\_ identificador processidtype**, o membro **ProcessHandle** conterá um identificador válido para um processo.</span><span class="sxs-lookup"><span data-stu-id="a8c6d-116">If the **ProcessIdentifier** member equals **PROCESSIDTYPE\_HANDLE**, the **ProcessHandle** member contains a valid handle to a process.</span></span> <span data-ttu-id="a8c6d-117">Caso contrário, esse membro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="a8c6d-117">Otherwise, this member is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8c6d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8c6d-118">Remarks</span></span>

<span data-ttu-id="a8c6d-119">O processo de Gerenciador de Janelas da Área de Trabalho (DWM) é identificado pela definição de **ProcessIdentifier** igual a **processidtype \_ DWM**.</span><span class="sxs-lookup"><span data-stu-id="a8c6d-119">The Desktop Window Manager (DWM) process is identified by setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="a8c6d-120">Outros processos são identificados definindo o identificador de processo em **ProcessHandle** e definindo **ProcessIdentifier** igual ao **\_ identificador processidtype**.</span><span class="sxs-lookup"><span data-stu-id="a8c6d-120">Other processes are identified by setting the process handle in **ProcessHandle** and setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_HANDLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c6d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8c6d-121">Requirements</span></span>



| <span data-ttu-id="a8c6d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8c6d-122">Requirement</span></span> | <span data-ttu-id="a8c6d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a8c6d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c6d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8c6d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c6d-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a8c6d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a8c6d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8c6d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c6d-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a8c6d-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a8c6d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8c6d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8c6d-129"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8c6d-129"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8c6d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8c6d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c6d-131">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a8c6d-131">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a8c6d-132">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a8c6d-132">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




