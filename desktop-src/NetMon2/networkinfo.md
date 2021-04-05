---
description: A estrutura NETWORKINFO descreve uma NIC.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Estrutura NETWORKINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663365"
---
# <a name="networkinfo-structure"></a><span data-ttu-id="ce485-103">Estrutura NETWORKINFO</span><span class="sxs-lookup"><span data-stu-id="ce485-103">NETWORKINFO structure</span></span>

<span data-ttu-id="ce485-104">A estrutura NETWORKINFO descreve uma NIC.</span><span class="sxs-lookup"><span data-stu-id="ce485-104">The NETWORKINFO structure describes a NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce485-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce485-105">Syntax</span></span>


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a><span data-ttu-id="ce485-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ce485-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce485-107">**PermanentAddr**</span><span class="sxs-lookup"><span data-stu-id="ce485-107">**PermanentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-108">Endereço MAC permanente.</span><span class="sxs-lookup"><span data-stu-id="ce485-108">Permanent MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="ce485-109">**CurrentAddr**</span><span class="sxs-lookup"><span data-stu-id="ce485-109">**CurrentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-110">Endereço MAC atual.</span><span class="sxs-lookup"><span data-stu-id="ce485-110">Current MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="ce485-111">**OtherAddress**</span><span class="sxs-lookup"><span data-stu-id="ce485-111">**OtherAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-112">Outro endereço que dá suporte a isso (por exemplo, IP, IPX).</span><span class="sxs-lookup"><span data-stu-id="ce485-112">Other address that support this (for example IP, IPX).</span></span>

</dd> <dt>

<span data-ttu-id="ce485-113">**LinkSpeed**</span><span class="sxs-lookup"><span data-stu-id="ce485-113">**LinkSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-114">Velocidade do link, em Mbps.</span><span class="sxs-lookup"><span data-stu-id="ce485-114">Link speed, in Mbps.</span></span>

</dd> <dt>

<span data-ttu-id="ce485-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="ce485-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-116">Tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="ce485-116">Media type.</span></span>

</dd> <dt>

<span data-ttu-id="ce485-117">**MaxFrameSize**</span><span class="sxs-lookup"><span data-stu-id="ce485-117">**MaxFrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-118">Tamanho máximo de quadro permitido.</span><span class="sxs-lookup"><span data-stu-id="ce485-118">Maximum frame size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="ce485-119">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="ce485-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-120">Esse parâmetro pode ser um dos seguintes sinalizadores informativos:</span><span class="sxs-lookup"><span data-stu-id="ce485-120">This parameter can be one of the following informational flags:</span></span>



| <span data-ttu-id="ce485-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ce485-121">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="ce485-122">Significado</span><span class="sxs-lookup"><span data-stu-id="ce485-122">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <span data-ttu-id="ce485-123"><dt>**NETWORKINFO \_ flags \_ pmode \_ não \_ suportado**</dt></span><span class="sxs-lookup"><span data-stu-id="ce485-123"><dt>**NETWORKINFO\_FLAGS\_PMODE\_NOT\_SUPPORTED**</dt></span></span> </dl>    | <span data-ttu-id="ce485-124">A placa de rede não dá suporte ao modo promíscuo, o que significa que ele capturará apenas o tráfego que é difundido por natureza ou apenas envolve o computador local.</span><span class="sxs-lookup"><span data-stu-id="ce485-124">The network card does not support promiscuous mode, meaning that it will only capture traffic which is broadcast in nature or only involves the local machine.</span></span><br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <span data-ttu-id="ce485-125"><dt>**\_RAS de sinalizadores NETWORKINFO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce485-125"><dt>**NETWORKINFO\_FLAGS\_RAS**</dt></span></span> </dl>                                                      | <span data-ttu-id="ce485-126">Essa é uma placa de rede virtual que é uma conexão RAS (servidor de acesso remoto) por meio de um modem ou outra placa de rede.</span><span class="sxs-lookup"><span data-stu-id="ce485-126">This is a virtual network card that is a RAS (Remote Access Server) connection through a modem or another network card.</span></span><br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <span data-ttu-id="ce485-127"><dt>**\_ \_ cartão remoto de sinalizadores NETWORKINFO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce485-127"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_CARD**</dt></span></span> </dl>                             | <span data-ttu-id="ce485-128">A placa de rede não está no computador local, mas está sendo capturada em um computador remoto no Bequest do computador local.</span><span class="sxs-lookup"><span data-stu-id="ce485-128">The network card is not on the local computer, but is capturing on a remote machine at the bequest of the local computer.</span></span><br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <span data-ttu-id="ce485-129"><dt>**\_ \_ nal remoto de sinalizadores NETWORKINFO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce485-129"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL**</dt></span></span> </dl>                                | <span data-ttu-id="ce485-130">Substituí Não use.</span><span class="sxs-lookup"><span data-stu-id="ce485-130">Obsolete; do not use.</span></span><br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <span data-ttu-id="ce485-131"><dt>**NETWORKINFO \_ sinalizadores \_ remotos de \_ nal \_ conectados**</dt></span><span class="sxs-lookup"><span data-stu-id="ce485-131"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ce485-132">Substituí Não use.</span><span class="sxs-lookup"><span data-stu-id="ce485-132">Obsolete; do not use.</span></span><br/>                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="ce485-133">**TimestampScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="ce485-133">**TimestampScaleFactor**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-134">Por exemplo, um valor de 1 indica 1/1 ms, 10 indica 1/10 ms, 100 indica 1/100 ms e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ce485-134">For example, a value of 1 indicates 1/1 ms, 10 indicates 1/10 ms, 100 indicates 1/100 ms, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="ce485-135">**NodeName**</span><span class="sxs-lookup"><span data-stu-id="ce485-135">**NodeName**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-136">Nome da estação de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ce485-136">Name of remote workstation.</span></span>

</dd> <dt>

<span data-ttu-id="ce485-137">**PModeSupported**</span><span class="sxs-lookup"><span data-stu-id="ce485-137">**PModeSupported**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-138">Indicador de suporte de modo P NIC.</span><span class="sxs-lookup"><span data-stu-id="ce485-138">NIC P-mode support indicator.</span></span>

</dd> <dt>

<span data-ttu-id="ce485-139">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ce485-139">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="ce485-140">Campo de comentário do adaptador.</span><span class="sxs-lookup"><span data-stu-id="ce485-140">Adapter comment field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce485-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce485-141">Requirements</span></span>



| <span data-ttu-id="ce485-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce485-142">Requirement</span></span> | <span data-ttu-id="ce485-143">Valor</span><span class="sxs-lookup"><span data-stu-id="ce485-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce485-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce485-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ce485-145">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ce485-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ce485-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce485-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ce485-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ce485-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ce485-148">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ce485-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce485-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce485-149"><dt>Netmon.h</dt></span></span> </dl> |



 

 




