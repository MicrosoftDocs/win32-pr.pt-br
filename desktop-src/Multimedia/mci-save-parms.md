---
title: Estrutura de MCI_SAVE_PARMS (Mciapi. h)
description: A \_ estrutura de salvar parâmetros do MCI \_ contém as informações de nome de arquivo para o \_ comando MCI Save.
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- Multimídia do Windows da estrutura de MCI_SAVE_PARMS
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758606"
---
# <a name="mci_save_parms-structure"></a><span data-ttu-id="da42c-104">Estrutura de parâmetros de \_ salvamento de MCI \_</span><span class="sxs-lookup"><span data-stu-id="da42c-104">MCI\_SAVE\_PARMS structure</span></span>

<span data-ttu-id="da42c-105">A estrutura de **\_ Salvar \_ parâmetros do MCI** contém as informações de nome de arquivo para o comando [**MCI \_ Save**](mci-save.md) .</span><span class="sxs-lookup"><span data-stu-id="da42c-105">The **MCI\_SAVE\_PARMS** structure contains the filename information for the [**MCI\_SAVE**](mci-save.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="da42c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da42c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a><span data-ttu-id="da42c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="da42c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="da42c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="da42c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="da42c-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="da42c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="da42c-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="da42c-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="da42c-111">Nome do arquivo a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="da42c-111">Name of file to save.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da42c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="da42c-112">Remarks</span></span>

<span data-ttu-id="da42c-113">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="da42c-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="da42c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da42c-114">Requirements</span></span>



| <span data-ttu-id="da42c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="da42c-115">Requirement</span></span> | <span data-ttu-id="da42c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="da42c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da42c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da42c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="da42c-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="da42c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="da42c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da42c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="da42c-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="da42c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="da42c-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="da42c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="da42c-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="da42c-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da42c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="da42c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da42c-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="da42c-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="da42c-125">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="da42c-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="da42c-126">**\_salvar MCI**</span><span class="sxs-lookup"><span data-stu-id="da42c-126">**MCI\_SAVE**</span></span>](mci-save.md)
</dt> <dt>

<span data-ttu-id="da42c-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="da42c-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

