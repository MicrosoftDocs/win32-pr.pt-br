---
title: Estrutura de MCI_OVLY_WINDOW_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros da janela MCI OVLY \_ \_ contém informações de exibição de janela para o \_ comando de janela MCI para dispositivos de sobreposição de vídeo.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- Multimídia do Windows da estrutura de MCI_OVLY_WINDOW_PARMS
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917971"
---
# <a name="mci_ovly_window_parms-structure"></a><span data-ttu-id="52a2c-104">\_Estrutura de \_ parâmetros da janela OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="52a2c-104">MCI\_OVLY\_WINDOW\_PARMS structure</span></span>

<span data-ttu-id="52a2c-105">A estrutura de **\_ parâmetros da \_ janela \_ MCI OVLY** contém informações de exibição de janela para o comando de [**\_ janela MCI**](mci-window.md) para dispositivos de sobreposição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="52a2c-105">The **MCI\_OVLY\_WINDOW\_PARMS** structure contains window-display information for the [**MCI\_WINDOW**](mci-window.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a2c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52a2c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a><span data-ttu-id="52a2c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="52a2c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="52a2c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="52a2c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="52a2c-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="52a2c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="52a2c-110">**hWnd**</span><span class="sxs-lookup"><span data-stu-id="52a2c-110">**hWnd**</span></span>
</dt> <dd>

<span data-ttu-id="52a2c-111">Identificador para exibir janela.</span><span class="sxs-lookup"><span data-stu-id="52a2c-111">Handle to display window.</span></span>

</dd> <dt>

<span data-ttu-id="52a2c-112">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="52a2c-112">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="52a2c-113">Janela-comando de exibição.</span><span class="sxs-lookup"><span data-stu-id="52a2c-113">Window-display command.</span></span>

</dd> <dt>

<span data-ttu-id="52a2c-114">**lpstrText**</span><span class="sxs-lookup"><span data-stu-id="52a2c-114">**lpstrText**</span></span>
</dt> <dd>

<span data-ttu-id="52a2c-115">Legenda da janela.</span><span class="sxs-lookup"><span data-stu-id="52a2c-115">Window caption.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52a2c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="52a2c-116">Remarks</span></span>

<span data-ttu-id="52a2c-117">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="52a2c-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="52a2c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52a2c-118">Requirements</span></span>



| <span data-ttu-id="52a2c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a2c-119">Requirement</span></span> | <span data-ttu-id="52a2c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="52a2c-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52a2c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52a2c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52a2c-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52a2c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="52a2c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52a2c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52a2c-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52a2c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52a2c-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52a2c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="52a2c-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="52a2c-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a2c-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="52a2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a2c-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="52a2c-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="52a2c-129">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="52a2c-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="52a2c-130">**\_janela MCI**</span><span class="sxs-lookup"><span data-stu-id="52a2c-130">**MCI\_WINDOW**</span></span>](mci-window.md)
</dt> <dt>

<span data-ttu-id="52a2c-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52a2c-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

