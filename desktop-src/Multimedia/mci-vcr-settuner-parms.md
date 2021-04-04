---
title: Estrutura de MCI_VCR_SETTUNER_PARMS (VCR. h)
description: A estrutura do MCI do \_ \_ setajuster de videocassetes \_ contém parâmetros para o \_ comando de setajuste MCI para gravadores de vídeo-fita.
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_SETTUNER_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644725"
---
# <a name="mci_vcr_settuner_parms-structure"></a><span data-ttu-id="6200c-104">\_Estrutura de \_ parâmetros de setajuster de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="6200c-104">MCI\_VCR\_SETTUNER\_PARMS structure</span></span>

<span data-ttu-id="6200c-105">A estrutura do **MCI do \_ \_ setajuster \_ de videocassetes** contém parâmetros para o comando de [**\_ setajuste MCI**](mci-settuner.md) para gravadores de vídeo-fita.</span><span class="sxs-lookup"><span data-stu-id="6200c-105">The **MCI\_VCR\_SETTUNER\_PARMS** structure contains parameters for the [**MCI\_SETTUNER**](mci-settuner.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="6200c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6200c-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a><span data-ttu-id="6200c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="6200c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6200c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="6200c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6200c-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="6200c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6200c-110">**dwChannel**</span><span class="sxs-lookup"><span data-stu-id="6200c-110">**dwChannel**</span></span>
</dt> <dd>

<span data-ttu-id="6200c-111">Novo número de canal.</span><span class="sxs-lookup"><span data-stu-id="6200c-111">New channel number.</span></span>

</dd> <dt>

<span data-ttu-id="6200c-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="6200c-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6200c-113">O sintonizador lógico que o comando do [**MCI \_ setajuste**](mci-settuner.md) afeta.</span><span class="sxs-lookup"><span data-stu-id="6200c-113">Logical tuner that the [**MCI\_SETTUNER**](mci-settuner.md) command affects.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6200c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6200c-114">Remarks</span></span>

<span data-ttu-id="6200c-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="6200c-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6200c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6200c-116">Requirements</span></span>



| <span data-ttu-id="6200c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6200c-117">Requirement</span></span> | <span data-ttu-id="6200c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6200c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6200c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6200c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6200c-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6200c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6200c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6200c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6200c-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6200c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6200c-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6200c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6200c-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="6200c-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6200c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6200c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6200c-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6200c-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6200c-127">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="6200c-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6200c-128">**setajuster do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="6200c-128">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
</dt> <dt>

<span data-ttu-id="6200c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6200c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

