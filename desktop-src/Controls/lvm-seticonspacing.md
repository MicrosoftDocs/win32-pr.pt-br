---
title: Mensagem de LVM_SETICONSPACING (commctrl. h)
description: Define o espaçamento entre os ícones nos controles de exibição de lista que têm o \_ estilo de ícone LVS. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetIconSpacing do ListView.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- Controles de LVM_SETICONSPACING de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824168"
---
# <a name="lvm_seticonspacing-message"></a><span data-ttu-id="1193e-105">\_Mensagem SETICONSPACING LVM</span><span class="sxs-lookup"><span data-stu-id="1193e-105">LVM\_SETICONSPACING message</span></span>

<span data-ttu-id="1193e-106">Define o espaçamento entre os ícones nos controles de exibição de lista que têm o estilo de [**\_ ícone LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1193e-106">Sets the spacing between icons in list-view controls that have the [**LVS\_ICON**](list-view-window-styles.md) style.</span></span> <span data-ttu-id="1193e-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetIconSpacing do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .</span><span class="sxs-lookup"><span data-stu-id="1193e-107">You can send this message explicitly or by using the [**ListView\_SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1193e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1193e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1193e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1193e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1193e-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1193e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1193e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1193e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1193e-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a distância, em pixels, para definir entre ícones no eixo x.</span><span class="sxs-lookup"><span data-stu-id="1193e-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the distance, in pixels, to set between icons on the x-axis.</span></span> <span data-ttu-id="1193e-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a distância, em pixels, para definir entre ícones no eixo y.</span><span class="sxs-lookup"><span data-stu-id="1193e-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the distance, in pixels, to set between icons on the y-axis.</span></span> <span data-ttu-id="1193e-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="1193e-114">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1193e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1193e-115">Return value</span></span>

<span data-ttu-id="1193e-116">Retorna um valor **DWORD** que contém a distância do eixo x anterior na palavra inferior e a distância anterior do eixo y na palavra alta.</span><span class="sxs-lookup"><span data-stu-id="1193e-116">Returns a **DWORD** value that contains the previous x-axis distance in the low word, and the previous y-axis distance in the high word.</span></span>

## <a name="remarks"></a><span data-ttu-id="1193e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1193e-117">Remarks</span></span>

<span data-ttu-id="1193e-118">Os valores para *lParam* são relativos ao canto superior esquerdo de um bitmap de ícone.</span><span class="sxs-lookup"><span data-stu-id="1193e-118">Values for *lParam* are relative to the upper-left corner of an icon bitmap.</span></span> <span data-ttu-id="1193e-119">Portanto, para definir o espaçamento entre ícones que não se sobrepõem, os valores de *lParam* devem incluir o tamanho do ícone, além da quantidade de espaço vazio desejado entre os ícones.</span><span class="sxs-lookup"><span data-stu-id="1193e-119">Therefore, to set spacing between icons that do not overlap, the *lParam* values must include the size of the icon, plus the amount of empty space desired between icons.</span></span> <span data-ttu-id="1193e-120">Os valores que não incluem a largura do ícone resultarão em sobreposições.</span><span class="sxs-lookup"><span data-stu-id="1193e-120">Values that do not include the width of the icon will result in overlaps.</span></span>

<span data-ttu-id="1193e-121">Ao definir o espaçamento de ícone, os valores de *lParam* devem ser definidos como 4 ou maiores.</span><span class="sxs-lookup"><span data-stu-id="1193e-121">When defining the icon spacing, the *lParam* values must set to 4 or larger.</span></span> <span data-ttu-id="1193e-122">Valores menores não produzirão o layout desejado.</span><span class="sxs-lookup"><span data-stu-id="1193e-122">Smaller values will not yield the desired layout.</span></span> <span data-ttu-id="1193e-123">Para redefinir os ícones para o espaçamento padrão, defina os valores de *lParam* como-1.</span><span class="sxs-lookup"><span data-stu-id="1193e-123">To reset the icons to the default spacing, set the *lParam* values to -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1193e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1193e-124">Requirements</span></span>



| <span data-ttu-id="1193e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1193e-125">Requirement</span></span> | <span data-ttu-id="1193e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1193e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1193e-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1193e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1193e-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1193e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1193e-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1193e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1193e-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1193e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1193e-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1193e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1193e-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1193e-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

