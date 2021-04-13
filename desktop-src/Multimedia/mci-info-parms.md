---
title: Estrutura de MCI_INFO_PARMS (Mciapi. h)
description: A estrutura de parâmetros de informações do MCI \_ \_ contém informações para o comando de informações do MCI \_ .
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- Multimídia do Windows da estrutura de MCI_INFO_PARMS
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d23221d140aaf093525691d7127c8466f392b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455955"
---
# <a name="mci_info_parms-structure"></a><span data-ttu-id="8cb02-104">Estrutura de parâmetros de \_ informações MCI \_</span><span class="sxs-lookup"><span data-stu-id="8cb02-104">MCI\_INFO\_PARMS structure</span></span>

<span data-ttu-id="8cb02-105">A estrutura de **\_ \_ parâmetros de informações do MCI** contém informações para o comando de [**\_ informações do MCI**](mci-info.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb02-105">The **MCI\_INFO\_PARMS** structure contains information for the [**MCI\_INFO**](mci-info.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb02-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cb02-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="8cb02-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8cb02-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8cb02-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8cb02-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8cb02-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="8cb02-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8cb02-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="8cb02-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="8cb02-111">Buffer para cadeia de caracteres de retorno.</span><span class="sxs-lookup"><span data-stu-id="8cb02-111">Buffer for return string.</span></span>

</dd> <dt>

<span data-ttu-id="8cb02-112">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="8cb02-112">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="8cb02-113">Tamanho, em caracteres, da cadeia de caracteres de retorno.</span><span class="sxs-lookup"><span data-stu-id="8cb02-113">Size, in characters, of return string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cb02-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cb02-114">Remarks</span></span>

<span data-ttu-id="8cb02-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="8cb02-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb02-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cb02-116">Requirements</span></span>



| <span data-ttu-id="8cb02-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cb02-117">Requirement</span></span> | <span data-ttu-id="8cb02-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8cb02-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb02-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cb02-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb02-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8cb02-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8cb02-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cb02-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb02-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8cb02-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8cb02-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8cb02-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cb02-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cb02-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cb02-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cb02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb02-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="8cb02-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8cb02-127">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="8cb02-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8cb02-128">**informações do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="8cb02-128">**MCI\_INFO**</span></span>](mci-info.md)
</dt> <dt>

<span data-ttu-id="8cb02-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8cb02-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

