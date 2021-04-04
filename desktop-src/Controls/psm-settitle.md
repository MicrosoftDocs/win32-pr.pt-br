---
title: Mensagem de PSM_SETTITLE (Prsht. h)
description: Define o título de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetTitle PropSheet.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- Controles de PSM_SETTITLE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918028"
---
# <a name="psm_settitle-message"></a><span data-ttu-id="ecc39-105">Mensagem de PSM \_ USERtitle</span><span class="sxs-lookup"><span data-stu-id="ecc39-105">PSM\_SETTITLE message</span></span>

<span data-ttu-id="ecc39-106">Define o título de uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ecc39-106">Sets the title of a property sheet.</span></span> <span data-ttu-id="ecc39-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetTitle PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .</span><span class="sxs-lookup"><span data-stu-id="ecc39-107">You can send this message explicitly or by using the [**PropSheet\_SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecc39-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecc39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecc39-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecc39-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecc39-110">Sinalizador que indica se deve incluir o prefixo "Propriedades para" ou o sufixo "Properties" (dependendo da versão) pela cadeia de título especificada.</span><span class="sxs-lookup"><span data-stu-id="ecc39-110">Flag that indicates whether to include the prefix "Properties for" or the suffix "Properties" (depending on the version) with the specified title string.</span></span> <span data-ttu-id="ecc39-111">Se esse valor for PSH \_ PROPTITLE, o prefixo ou sufixo será incluído.</span><span class="sxs-lookup"><span data-stu-id="ecc39-111">If this value is PSH\_PROPTITLE, the prefix or suffix is included.</span></span>

</dd> <dt>

<span data-ttu-id="ecc39-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecc39-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecc39-113">Ponteiro para um buffer que contém a cadeia de título.</span><span class="sxs-lookup"><span data-stu-id="ecc39-113">Pointer to a buffer that contains the title string.</span></span> <span data-ttu-id="ecc39-114">Se o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) desse parâmetro for **nulo**, a folha de propriedades carregará o recurso de cadeia de caracteres especificado em [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ecc39-114">If the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this parameter is **NULL**, the property sheet loads the string resource specified in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecc39-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ecc39-115">Return value</span></span>

<span data-ttu-id="ecc39-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ecc39-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecc39-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecc39-117">Remarks</span></span>

<span data-ttu-id="ecc39-118">Em um assistente Aero, essa mensagem pode ser usada para alterar o título de uma página interior dinamicamente; por exemplo, ao lidar com a notificação [ \_ SetActive PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc39-118">In an Aero Wizard, this message can be used to change the title of an interior page dynamically; for example, when handling the [PSN\_SETACTIVE](psn-setactive.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc39-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecc39-119">Requirements</span></span>



| <span data-ttu-id="ecc39-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecc39-120">Requirement</span></span> | <span data-ttu-id="ecc39-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ecc39-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc39-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecc39-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc39-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ecc39-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ecc39-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecc39-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc39-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ecc39-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ecc39-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ecc39-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecc39-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc39-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="ecc39-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ecc39-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ecc39-129">**PSM \_ SETTITLEW** (Unicode) e **PSM \_ settítuloa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ecc39-129">**PSM\_SETTITLEW** (Unicode) and **PSM\_SETTITLEA** (ANSI)</span></span><br/>              |



 

