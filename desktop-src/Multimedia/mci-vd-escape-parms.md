---
title: Estrutura de MCI_VD_ESCAPE_PARMS (Mciapi. h)
description: A estrutura de parâmetros de escape de VD do MCI \_ \_ \_ contém o comando enviado a um dispositivo para o \_ comando de escape MCI para dispositivos VIDEODISC.
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- Multimídia do Windows da estrutura de MCI_VD_ESCAPE_PARMS
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778548"
---
# <a name="mci_vd_escape_parms-structure"></a><span data-ttu-id="89fb3-104">\_Estrutura de \_ parâmetros de escape de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="89fb3-104">MCI\_VD\_ESCAPE\_PARMS structure</span></span>

<span data-ttu-id="89fb3-105">A estrutura de parâmetros de escape de VD do MCI contém o comando enviado a um dispositivo para o comando de [**\_ escape MCI**](mci-escape.md) para dispositivos VIDEODISC. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89fb3-105">The **MCI\_VD\_ESCAPE\_PARMS** structure contains the command sent to a device for the [**MCI\_ESCAPE**](mci-escape.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fb3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89fb3-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a><span data-ttu-id="89fb3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="89fb3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="89fb3-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="89fb3-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="89fb3-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="89fb3-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="89fb3-110">**lpstrCommand**</span><span class="sxs-lookup"><span data-stu-id="89fb3-110">**lpstrCommand**</span></span>
</dt> <dd>

<span data-ttu-id="89fb3-111">Comando a ser enviado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89fb3-111">Command to send to device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89fb3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="89fb3-112">Remarks</span></span>

<span data-ttu-id="89fb3-113">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="89fb3-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="89fb3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89fb3-114">Requirements</span></span>



| <span data-ttu-id="89fb3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="89fb3-115">Requirement</span></span> | <span data-ttu-id="89fb3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="89fb3-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="89fb3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89fb3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="89fb3-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89fb3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="89fb3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89fb3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="89fb3-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89fb3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="89fb3-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="89fb3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="89fb3-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="89fb3-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89fb3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="89fb3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89fb3-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="89fb3-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="89fb3-125">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="89fb3-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="89fb3-126">**\_escape MCI**</span><span class="sxs-lookup"><span data-stu-id="89fb3-126">**MCI\_ESCAPE**</span></span>](mci-escape.md)
</dt> <dt>

<span data-ttu-id="89fb3-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="89fb3-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

