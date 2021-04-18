---
title: Estrutura de MCI_OVLY_OPEN_PARMS (mmsystem. h)
description: A \_ estrutura MCI OVLY \_ Open \_ parms contém informações para o \_ comando MCI Open para dispositivos de sobreposição de vídeo.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- Multimídia do Windows da estrutura de MCI_OVLY_OPEN_PARMS
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454606"
---
# <a name="mci_ovly_open_parms-structure"></a><span data-ttu-id="54141-104">\_Estrutura de \_ \_ parâmetros abertos do MCI OVLY</span><span class="sxs-lookup"><span data-stu-id="54141-104">MCI\_OVLY\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="54141-105">A estrutura **MCI \_ OVLY \_ Open \_ parms** contém informações para o comando [**MCI \_ Open**](mci-open.md) para dispositivos de sobreposição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="54141-105">The **MCI\_OVLY\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="54141-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54141-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="54141-107">Membros</span><span class="sxs-lookup"><span data-stu-id="54141-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="54141-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="54141-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="54141-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="54141-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="54141-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="54141-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="54141-111">Identificador retornado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54141-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="54141-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="54141-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="54141-113">Nome ou identificador de constante do tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54141-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="54141-114">(O nome do dispositivo normalmente é obtido do registro ou do arquivo de SYSTEM.INI.) Se esse membro for uma constante, ele poderá ser um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="54141-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="54141-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="54141-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="54141-116">Nome do elemento do dispositivo (geralmente um caminho).</span><span class="sxs-lookup"><span data-stu-id="54141-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="54141-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="54141-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="54141-118">Alias de dispositivo opcional.</span><span class="sxs-lookup"><span data-stu-id="54141-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="54141-119">**dwStyle**</span><span class="sxs-lookup"><span data-stu-id="54141-119">**dwStyle**</span></span>
</dt> <dd>

<span data-ttu-id="54141-120">Estilo da janela.</span><span class="sxs-lookup"><span data-stu-id="54141-120">Window style.</span></span>

</dd> <dt>

<span data-ttu-id="54141-121">**hWndParent**</span><span class="sxs-lookup"><span data-stu-id="54141-121">**hWndParent**</span></span>
</dt> <dd>

<span data-ttu-id="54141-122">Identificador da janela pai.</span><span class="sxs-lookup"><span data-stu-id="54141-122">Handle to parent window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54141-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="54141-123">Remarks</span></span>

<span data-ttu-id="54141-124">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="54141-124">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="54141-125">Você pode usar a estrutura [**MCI \_ Open \_ parms**](mci-open-parms.md) no lugar do **MCI \_ OVLY \_ Open \_ parms** se não estiver usando os membros de dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="54141-125">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure in place of **MCI\_OVLY\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="54141-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54141-126">Requirements</span></span>



| <span data-ttu-id="54141-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="54141-127">Requirement</span></span> | <span data-ttu-id="54141-128">Valor</span><span class="sxs-lookup"><span data-stu-id="54141-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54141-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54141-129">Minimum supported client</span></span><br/> | <span data-ttu-id="54141-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54141-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="54141-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54141-131">Minimum supported server</span></span><br/> | <span data-ttu-id="54141-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54141-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54141-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="54141-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="54141-134"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="54141-134"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54141-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="54141-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54141-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="54141-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="54141-137">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="54141-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="54141-138">**MCI \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="54141-138">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

[<span data-ttu-id="54141-139">**\_parâmetros de abertura do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="54141-139">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> <dt>

<span data-ttu-id="54141-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="54141-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

