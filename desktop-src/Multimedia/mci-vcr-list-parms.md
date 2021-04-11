---
title: Estrutura de MCI_VCR_LIST_PARMS (VCR. h)
description: A estrutura de parâmetros da \_ lista de videocassetes MCI \_ \_ contém parâmetros para o comando de lista de MCI \_ para gravadores de vídeo-fita.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_LIST_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3e7a2eae67ebc7148b7ff424361f16554a435c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295879"
---
# <a name="mci_vcr_list_parms-structure"></a><span data-ttu-id="cf45f-104">\_Estrutura de \_ parâmetros da lista de VIDEOCASSETEs MCI \_</span><span class="sxs-lookup"><span data-stu-id="cf45f-104">MCI\_VCR\_LIST\_PARMS structure</span></span>

<span data-ttu-id="cf45f-105">A estrutura de parâmetros da **\_ \_ lista \_ de videocassetes MCI** contém parâmetros para o comando de [**\_ lista de MCI**](mci-list.md) para gravadores de vídeo-fita.</span><span class="sxs-lookup"><span data-stu-id="cf45f-105">The **MCI\_VCR\_LIST\_PARMS** structure contains parameters for the [**MCI\_LIST**](mci-list.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf45f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf45f-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a><span data-ttu-id="cf45f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cf45f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf45f-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="cf45f-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="cf45f-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="cf45f-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="cf45f-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="cf45f-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="cf45f-111">Buffer para informações retornadas.</span><span class="sxs-lookup"><span data-stu-id="cf45f-111">Buffer for returned information.</span></span>

</dd> <dt>

<span data-ttu-id="cf45f-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="cf45f-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="cf45f-113">Número de entradas de áudio ou vídeo do VCR.</span><span class="sxs-lookup"><span data-stu-id="cf45f-113">Number of VCR's video or audio inputs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf45f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf45f-114">Remarks</span></span>

<span data-ttu-id="cf45f-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="cf45f-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf45f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf45f-116">Requirements</span></span>



| <span data-ttu-id="cf45f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf45f-117">Requirement</span></span> | <span data-ttu-id="cf45f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cf45f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cf45f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf45f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf45f-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf45f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cf45f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf45f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf45f-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf45f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cf45f-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cf45f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf45f-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf45f-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf45f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf45f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf45f-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="cf45f-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cf45f-127">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="cf45f-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="cf45f-128">**lista de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="cf45f-128">**MCI\_LIST**</span></span>](mci-list.md)
</dt> <dt>

<span data-ttu-id="cf45f-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf45f-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

