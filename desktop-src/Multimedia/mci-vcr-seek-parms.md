---
title: Estrutura de MCI_VCR_SEEK_PARMS (VCR. h)
description: A estrutura de parâmetros de busca de VCR do MCI \_ \_ \_ contém parâmetros para o \_ comando MCI Seek para gravadores de vídeo-fita.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_SEEK_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454909"
---
# <a name="mci_vcr_seek_parms-structure"></a><span data-ttu-id="84b72-104">\_Estrutura de \_ parâmetros de busca de VCR do MCI \_</span><span class="sxs-lookup"><span data-stu-id="84b72-104">MCI\_VCR\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="84b72-105">A estrutura de parâmetros de busca de VCR do MCI contém parâmetros para o comando [**MCI \_ Seek**](mci-seek.md) para gravadores de vídeo-fita. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84b72-105">The **MCI\_VCR\_SEEK\_PARMS** structure contains parameters for the [**MCI\_SEEK**](mci-seek.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b72-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84b72-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="84b72-107">Membros</span><span class="sxs-lookup"><span data-stu-id="84b72-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="84b72-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="84b72-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="84b72-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="84b72-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="84b72-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="84b72-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="84b72-111">Posição para a qual buscar.</span><span class="sxs-lookup"><span data-stu-id="84b72-111">Position to seek to.</span></span>

</dd> <dt>

<span data-ttu-id="84b72-112">**dwMark**</span><span class="sxs-lookup"><span data-stu-id="84b72-112">**dwMark**</span></span>
</dt> <dd>

<span data-ttu-id="84b72-113">Marca numerada a ser procurada.</span><span class="sxs-lookup"><span data-stu-id="84b72-113">Numbered mark to seek for.</span></span>

</dd> <dt>

<span data-ttu-id="84b72-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="84b72-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="84b72-115">Hora em que a busca começa.</span><span class="sxs-lookup"><span data-stu-id="84b72-115">Time when seek begins.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84b72-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="84b72-116">Remarks</span></span>

<span data-ttu-id="84b72-117">As posições são especificadas no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="84b72-117">Positions are specified in the current time format.</span></span>

<span data-ttu-id="84b72-118">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="84b72-118">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="84b72-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84b72-119">Requirements</span></span>



| <span data-ttu-id="84b72-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="84b72-120">Requirement</span></span> | <span data-ttu-id="84b72-121">Valor</span><span class="sxs-lookup"><span data-stu-id="84b72-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84b72-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84b72-122">Minimum supported client</span></span><br/> | <span data-ttu-id="84b72-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="84b72-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84b72-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84b72-124">Minimum supported server</span></span><br/> | <span data-ttu-id="84b72-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="84b72-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84b72-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="84b72-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="84b72-127"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="84b72-127"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b72-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="84b72-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b72-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="84b72-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="84b72-130">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="84b72-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="84b72-131">**busca de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="84b72-131">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="84b72-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84b72-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

