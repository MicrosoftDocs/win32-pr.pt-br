---
title: Estrutura de MCI_VCR_SETAUDIO_PARMS (VCR. h)
description: A estrutura do MCI de \_ SetAudio de videocassetes \_ \_ contém parâmetros para o \_ comando de SetAudio do MCI para gravadores de vídeo-fita.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_SETAUDIO_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824222"
---
# <a name="mci_vcr_setaudio_parms-structure"></a><span data-ttu-id="967ac-104">\_Estrutura de \_ parâmetros de áudio \_ MCI de VCR</span><span class="sxs-lookup"><span data-stu-id="967ac-104">MCI\_VCR\_SETAUDIO\_PARMS structure</span></span>

<span data-ttu-id="967ac-105">A estrutura do **MCI de \_ \_ SetAudio \_ de videocassetes** contém parâmetros para o comando de [**\_ SetAudio do MCI**](mci-setaudio.md) para gravadores de vídeo-fita.</span><span class="sxs-lookup"><span data-stu-id="967ac-105">The **MCI\_VCR\_SETAUDIO\_PARMS** structure contains parameters for the [**MCI\_SETAUDIO**](mci-setaudio.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="967ac-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="967ac-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a><span data-ttu-id="967ac-107">Membros</span><span class="sxs-lookup"><span data-stu-id="967ac-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="967ac-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="967ac-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="967ac-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="967ac-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="967ac-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="967ac-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="967ac-111">Faixa de áudio.</span><span class="sxs-lookup"><span data-stu-id="967ac-111">Audio track.</span></span>

</dd> <dt>

<span data-ttu-id="967ac-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="967ac-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="967ac-113">Tipo de entrada ou entrada monitorada.</span><span class="sxs-lookup"><span data-stu-id="967ac-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="967ac-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="967ac-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="967ac-115">Entrada de áudio (do tipo especificado no membro **dwTo** ) a ser usado.</span><span class="sxs-lookup"><span data-stu-id="967ac-115">Audio input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="967ac-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="967ac-116">Remarks</span></span>

<span data-ttu-id="967ac-117">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="967ac-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="967ac-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="967ac-118">Requirements</span></span>



| <span data-ttu-id="967ac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="967ac-119">Requirement</span></span> | <span data-ttu-id="967ac-120">Valor</span><span class="sxs-lookup"><span data-stu-id="967ac-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="967ac-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="967ac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="967ac-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="967ac-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="967ac-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="967ac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="967ac-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="967ac-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="967ac-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="967ac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="967ac-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="967ac-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="967ac-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="967ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967ac-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="967ac-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="967ac-129">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="967ac-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="967ac-130">**\_áudio MCI**</span><span class="sxs-lookup"><span data-stu-id="967ac-130">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
</dt> <dt>

<span data-ttu-id="967ac-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="967ac-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

