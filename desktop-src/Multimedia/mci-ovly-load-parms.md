---
title: Estrutura de MCI_OVLY_LOAD_PARMS (mmsystem. h)
description: A \_ estrutura de parâmetros de carga OVLY do MCI \_ \_ contém informações para o \_ comando de carregamento MCI para dispositivos de sobreposição de vídeo.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- Multimídia do Windows da estrutura de MCI_OVLY_LOAD_PARMS
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008838"
---
# <a name="mci_ovly_load_parms-structure"></a><span data-ttu-id="0a358-104">\_Estrutura de \_ parâmetros de carga OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a358-104">MCI\_OVLY\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="0a358-105">A estrutura de **\_ \_ \_ parâmetros de carga OVLY do MCI** contém informações para o comando de [**\_ carregamento MCI**](mci-load.md) para dispositivos de sobreposição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0a358-105">The **MCI\_OVLY\_LOAD\_PARMS** structure contains information for the [**MCI\_LOAD**](mci-load.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a358-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a358-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="0a358-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0a358-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a358-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="0a358-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0a358-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="0a358-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0a358-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="0a358-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="0a358-111">Nome do arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="0a358-111">Name of file to load.</span></span>

</dd> <dt>

<span data-ttu-id="0a358-112">**RC**</span><span class="sxs-lookup"><span data-stu-id="0a358-112">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="0a358-113">Identifica a área do buffer de vídeo a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="0a358-113">Identifies the area of the video buffer to update.</span></span> <span data-ttu-id="0a358-114">As estruturas [Rect](/previous-versions//ms536136(v=vs.85)) são tratadas de forma diferente no MCI do que em outras partes do Windows; no MCI, **RC. Right** contém a largura do retângulo e **RC. Bottom** contém sua altura.</span><span class="sxs-lookup"><span data-stu-id="0a358-114">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a358-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a358-115">Remarks</span></span>

<span data-ttu-id="0a358-116">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="0a358-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a358-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a358-117">Requirements</span></span>



| <span data-ttu-id="0a358-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a358-118">Requirement</span></span> | <span data-ttu-id="0a358-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0a358-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a358-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a358-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0a358-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0a358-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0a358-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a358-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0a358-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0a358-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a358-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0a358-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a358-125"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a358-125"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a358-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a358-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a358-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0a358-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0a358-128">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="0a358-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0a358-129">**\_carga MCI**</span><span class="sxs-lookup"><span data-stu-id="0a358-129">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="0a358-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a358-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0a358-131">[RECT](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a358-131">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

