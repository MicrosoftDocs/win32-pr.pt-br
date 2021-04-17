---
title: Estrutura de MCI_SYSINFO_PARMS (Mciapi. h)
description: A estrutura de parâmetros do sysinfo do MCI \_ \_ contém informações para o comando do sysinfo do MCI \_ .
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- Multimídia do Windows da estrutura de MCI_SYSINFO_PARMS
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760818"
---
# <a name="mci_sysinfo_parms-structure"></a><span data-ttu-id="efc91-104">Estrutura de parâmetros do \_ sysinfo do MCI \_</span><span class="sxs-lookup"><span data-stu-id="efc91-104">MCI\_SYSINFO\_PARMS structure</span></span>

<span data-ttu-id="efc91-105">A estrutura de **\_ \_ parâmetros do sysinfo do MCI** contém informações para o comando do [**\_ sysinfo do MCI**](mci-sysinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="efc91-105">The **MCI\_SYSINFO\_PARMS** structure contains information for the [**MCI\_SYSINFO**](mci-sysinfo.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc91-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efc91-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="efc91-107">Membros</span><span class="sxs-lookup"><span data-stu-id="efc91-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="efc91-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="efc91-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="efc91-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="efc91-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="efc91-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="efc91-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="efc91-111">Ponteiro para um buffer fornecido pelo usuário para a cadeia de caracteres de retorno.</span><span class="sxs-lookup"><span data-stu-id="efc91-111">Pointer to a user-supplied buffer for the return string.</span></span> <span data-ttu-id="efc91-112">Ele também é usado para retornar um valor **DWORD** quando o sinalizador de quantidade do sysinfo do MCI \_ \_ é usado.</span><span class="sxs-lookup"><span data-stu-id="efc91-112">It is also used to return a **DWORD** value when the MCI\_SYSINFO\_QUANTITY flag is used.</span></span>

</dd> <dt>

<span data-ttu-id="efc91-113">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="efc91-113">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="efc91-114">Tamanho, em bytes, do buffer de retorno.</span><span class="sxs-lookup"><span data-stu-id="efc91-114">Size, in bytes, of return buffer.</span></span>

</dd> <dt>

<span data-ttu-id="efc91-115">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="efc91-115">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="efc91-116">Número que indica a posição do dispositivo na tabela do dispositivo MCI ou na lista de dispositivos abertos se o \_ sinalizador de abertura do sysinfo do MCI \_ estiver definido.</span><span class="sxs-lookup"><span data-stu-id="efc91-116">Number indicating the device position in the MCI device table or in the list of open devices if the MCI\_SYSINFO\_OPEN flag is set.</span></span>

</dd> <dt>

<span data-ttu-id="efc91-117">**wDeviceType**</span><span class="sxs-lookup"><span data-stu-id="efc91-117">**wDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="efc91-118">Tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efc91-118">Type of device.</span></span> <span data-ttu-id="efc91-119">Esse membro pode ser um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="efc91-119">This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efc91-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="efc91-120">Remarks</span></span>

<span data-ttu-id="efc91-121">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="efc91-121">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="efc91-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efc91-122">Requirements</span></span>



| <span data-ttu-id="efc91-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc91-123">Requirement</span></span> | <span data-ttu-id="efc91-124">Valor</span><span class="sxs-lookup"><span data-stu-id="efc91-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="efc91-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efc91-125">Minimum supported client</span></span><br/> | <span data-ttu-id="efc91-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="efc91-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="efc91-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efc91-127">Minimum supported server</span></span><br/> | <span data-ttu-id="efc91-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="efc91-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="efc91-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="efc91-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="efc91-130"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="efc91-130"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc91-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="efc91-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc91-132">**MCI**</span><span class="sxs-lookup"><span data-stu-id="efc91-132">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="efc91-133">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="efc91-133">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="efc91-134">**SysInfo do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="efc91-134">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
</dt> <dt>

<span data-ttu-id="efc91-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="efc91-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

