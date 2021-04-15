---
title: Estrutura de MCI_WAVE_OPEN_PARMS (Mciapi. h)
description: A \_ estrutura MCI \_ Open \_ parms de Wave contém informações para o \_ comando MCI Open para dispositivos de forma de onda-áudio.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- Multimídia do Windows da estrutura de MCI_WAVE_OPEN_PARMS
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760817"
---
# <a name="mci_wave_open_parms-structure"></a><span data-ttu-id="86ffb-104">\_Estrutura de \_ \_ parâmetros abertos do MCI Wave</span><span class="sxs-lookup"><span data-stu-id="86ffb-104">MCI\_WAVE\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="86ffb-105">A **estrutura \_ MCI \_ Open \_ parms de Wave** contém informações para o comando [**MCI \_ Open**](mci-open.md) para dispositivos de forma de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="86ffb-105">The **MCI\_WAVE\_OPEN\_PARMS** structure contains information for [**MCI\_OPEN**](mci-open.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ffb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86ffb-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="86ffb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="86ffb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="86ffb-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="86ffb-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="86ffb-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="86ffb-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="86ffb-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="86ffb-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="86ffb-111">Indentificador retornou ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="86ffb-111">Indentifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="86ffb-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="86ffb-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="86ffb-113">Nome ou identificador de constante do tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86ffb-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="86ffb-114">(O nome do dispositivo normalmente é obtido do registro ou do arquivo de SYSTEM.INI.) Esse membro pode ser um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="86ffb-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="86ffb-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="86ffb-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="86ffb-116">Nome do elemento do dispositivo (geralmente um caminho).</span><span class="sxs-lookup"><span data-stu-id="86ffb-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="86ffb-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="86ffb-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="86ffb-118">Alias de dispositivo opcional.</span><span class="sxs-lookup"><span data-stu-id="86ffb-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="86ffb-119">**dwBufferSeconds**</span><span class="sxs-lookup"><span data-stu-id="86ffb-119">**dwBufferSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="86ffb-120">Tamanho do buffer, em segundos.</span><span class="sxs-lookup"><span data-stu-id="86ffb-120">Buffer length, in seconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86ffb-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="86ffb-121">Remarks</span></span>

<span data-ttu-id="86ffb-122">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="86ffb-122">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="86ffb-123">Você pode usar a estrutura [**MCI \_ Open \_ parms**](mci-open-parms.md) em vez **de \_ \_ \_ parâmetros de abertura Wave MCI** se não estiver usando os membros de dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="86ffb-123">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure instead of **MCI\_WAVE\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ffb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86ffb-124">Requirements</span></span>



| <span data-ttu-id="86ffb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ffb-125">Requirement</span></span> | <span data-ttu-id="86ffb-126">Valor</span><span class="sxs-lookup"><span data-stu-id="86ffb-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="86ffb-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86ffb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="86ffb-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="86ffb-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="86ffb-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86ffb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="86ffb-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="86ffb-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="86ffb-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="86ffb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="86ffb-132"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="86ffb-132"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ffb-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="86ffb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ffb-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="86ffb-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="86ffb-135">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="86ffb-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="86ffb-136">**MCI \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="86ffb-136">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="86ffb-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86ffb-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="86ffb-138">**\_parâmetros de abertura do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="86ffb-138">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> </dl>

 

