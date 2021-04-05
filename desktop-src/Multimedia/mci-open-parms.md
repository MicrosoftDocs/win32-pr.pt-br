---
title: Estrutura de MCI_OPEN_PARMS (Mciapi. h)
description: A \_ estrutura MCI Open \_ parms contém informações para o \_ comando MCI Open.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- Multimídia do Windows da estrutura de MCI_OPEN_PARMS
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658f97a9b2677347c9818265c1f05c2115c95fdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085444"
---
# <a name="mci_open_parms-structure"></a><span data-ttu-id="024bd-104">\_Estrutura de parâmetros abertos do MCI \_</span><span class="sxs-lookup"><span data-stu-id="024bd-104">MCI\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="024bd-105">A estrutura **MCI \_ Open \_ parms** contém informações para o comando [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="024bd-105">The **MCI\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="024bd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="024bd-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="024bd-107">Membros</span><span class="sxs-lookup"><span data-stu-id="024bd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="024bd-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="024bd-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="024bd-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="024bd-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="024bd-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="024bd-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="024bd-111">Identificador retornado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="024bd-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="024bd-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="024bd-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="024bd-113">Nome ou identificador de constante do tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="024bd-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="024bd-114">(O nome do dispositivo normalmente é obtido do registro ou do arquivo de SYSTEM.INI.) Se esse membro for uma constante, ele poderá ser um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="024bd-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="024bd-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="024bd-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="024bd-116">Elemento Device (geralmente um caminho).</span><span class="sxs-lookup"><span data-stu-id="024bd-116">Device element (often a path).</span></span>

</dd> <dt>

<span data-ttu-id="024bd-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="024bd-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="024bd-118">Alias de dispositivo opcional.</span><span class="sxs-lookup"><span data-stu-id="024bd-118">Optional device alias.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="024bd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="024bd-119">Remarks</span></span>

<span data-ttu-id="024bd-120">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="024bd-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="024bd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="024bd-121">Requirements</span></span>



| <span data-ttu-id="024bd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="024bd-122">Requirement</span></span> | <span data-ttu-id="024bd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="024bd-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="024bd-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="024bd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="024bd-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="024bd-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="024bd-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="024bd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="024bd-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="024bd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="024bd-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="024bd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="024bd-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="024bd-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024bd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="024bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024bd-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="024bd-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="024bd-132">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="024bd-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="024bd-133">**MCI \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="024bd-133">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="024bd-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="024bd-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

