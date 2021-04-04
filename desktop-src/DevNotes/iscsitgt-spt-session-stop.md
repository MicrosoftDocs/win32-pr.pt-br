---
description: Usado com o IOCTL \_ da \_ miniporta SCSI do IOCTL e o \_ código de controle do 0x101 (CTLCODE ISCSITGT \_ SPT \_ Session \_ end) para interromper uma sessão.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Estrutura de ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "103837716"
---
# <a name="iscsitgt_spt_session_stop-structure"></a><span data-ttu-id="0a4fc-103">\_Estrutura de \_ interrupção de sessão ISCSITGT SPT \_</span><span class="sxs-lookup"><span data-stu-id="0a4fc-103">ISCSITGT\_SPT\_SESSION\_STOP structure</span></span>

<span data-ttu-id="0a4fc-104">\[A estrutura a seguir está disponível para uso no Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-104">\[The following structure is available for use in Windows Server 2012 R2.</span></span> <span data-ttu-id="0a4fc-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="0a4fc-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="0a4fc-106">Usado com o IOCTL da [**\_ \_ miniporta SCSI**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) do IOCTL e o \_ código de controle do 0x101 (CTLCODE ISCSITGT \_ SPT \_ Session \_ end) para interromper uma sessão.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-106">Used with the [**IOCTL\_SCSI\_MINIPORT**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL and the CTLCODE\_ISCSITGT\_SPT\_SESSION\_END (0x101) control code to stop a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4fc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a4fc-107">Syntax</span></span>


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a><span data-ttu-id="0a4fc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0a4fc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a4fc-109">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="0a4fc-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="0a4fc-110">Cabeçalho obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-110">Mandatory header.</span></span>

</dd> <dt>

<span data-ttu-id="0a4fc-111">**ITNexusHandle**</span><span class="sxs-lookup"><span data-stu-id="0a4fc-111">**ITNexusHandle**</span></span>
</dt> <dd>

<span data-ttu-id="0a4fc-112">Um identificador opaco que representa uma sessão.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-112">An opaque handle representing a session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a4fc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a4fc-113">Requirements</span></span>



| <span data-ttu-id="0a4fc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a4fc-114">Requirement</span></span> | <span data-ttu-id="0a4fc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0a4fc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0a4fc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a4fc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4fc-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0a4fc-117">None supported</span></span><br/>                               |
| <span data-ttu-id="0a4fc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a4fc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4fc-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="0a4fc-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0a4fc-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0a4fc-120">End of client support</span></span><br/>    | <span data-ttu-id="0a4fc-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0a4fc-121">None supported</span></span><br/>                               |
| <span data-ttu-id="0a4fc-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="0a4fc-122">End of server support</span></span><br/>    | <span data-ttu-id="0a4fc-123">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0a4fc-123">Windows Server 2012 R2</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0a4fc-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a4fc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4fc-125">Passagem de destino iSCSI</span><span class="sxs-lookup"><span data-stu-id="0a4fc-125">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="0a4fc-126">**\_controle de e/s SRB \_**</span><span class="sxs-lookup"><span data-stu-id="0a4fc-126">**SRB\_IO\_CONTROL**</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
