---
title: Estrutura de MCI_VCR_SETVIDEO_PARMS (VCR. h)
description: A estrutura de vídeo de VCR do MCI de \_ videocassete \_ \_ contém parâmetros para o comando do MCI \_ de vídeo para gravadores de vídeo-fita.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_SETVIDEO_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824702"
---
# <a name="mci_vcr_setvideo_parms-structure"></a><span data-ttu-id="a5fb8-104">\_Estrutura de \_ parâmetros de vídeo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a5fb8-104">MCI\_VCR\_SETVIDEO\_PARMS structure</span></span>

<span data-ttu-id="a5fb8-105">A estrutura de **vídeo de VCR do MCI de \_ videocassete \_ \_** contém parâmetros para o comando do MCI de vídeo para gravadores de vídeo-fita. [**\_**](mci-setvideo.md)</span><span class="sxs-lookup"><span data-stu-id="a5fb8-105">The **MCI\_VCR\_SETVIDEO\_PARMS** structure contains parameters for the [**MCI\_SETVIDEO**](mci-setvideo.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fb8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5fb8-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a><span data-ttu-id="a5fb8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a5fb8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5fb8-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="a5fb8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="a5fb8-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="a5fb8-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="a5fb8-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="a5fb8-111">Controle afetado.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-111">Affected track.</span></span>

</dd> <dt>

<span data-ttu-id="a5fb8-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="a5fb8-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="a5fb8-113">Tipo de entrada ou entrada monitorada.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="a5fb8-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="a5fb8-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="a5fb8-115">Entrada de vídeo (do tipo especificado no membro **dwTo** ) a ser usado.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-115">Video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5fb8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5fb8-116">Remarks</span></span>

<span data-ttu-id="a5fb8-117">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fb8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5fb8-118">Requirements</span></span>



| <span data-ttu-id="a5fb8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5fb8-119">Requirement</span></span> | <span data-ttu-id="a5fb8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a5fb8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a5fb8-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5fb8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5fb8-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a5fb8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a5fb8-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5fb8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5fb8-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a5fb8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a5fb8-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a5fb8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5fb8-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5fb8-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5fb8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5fb8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5fb8-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="a5fb8-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a5fb8-129">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="a5fb8-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="a5fb8-130">**VÍDEO do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="a5fb8-130">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
</dt> <dt>

<span data-ttu-id="a5fb8-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5fb8-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

