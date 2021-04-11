---
title: Mensagem de LVM_SETGROUPINFO (commctrl. h)
description: Define informações do grupo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- Controles de LVM_SETGROUPINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008858"
---
# <a name="lvm_setgroupinfo-message"></a><span data-ttu-id="042de-104">\_Mensagem SETGROUPINFO LVM</span><span class="sxs-lookup"><span data-stu-id="042de-104">LVM\_SETGROUPINFO message</span></span>

<span data-ttu-id="042de-105">Define informações do grupo.</span><span class="sxs-lookup"><span data-stu-id="042de-105">Sets group information.</span></span> <span data-ttu-id="042de-106">Envie essa mensagem explicitamente ou usando a macro [**\_ SetGroupInfo do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .</span><span class="sxs-lookup"><span data-stu-id="042de-106">Send this message explicitly or by using the [**ListView\_SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="042de-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="042de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="042de-108">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="042de-108">*wParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="042de-109">ID que especifica o grupo cujas informações serão definidas.</span><span class="sxs-lookup"><span data-stu-id="042de-109">ID that specifies the group whose information is to be set.</span></span></dd> <dt>

<span data-ttu-id="042de-110">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="042de-110">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="042de-111">Ponteiro para uma estrutura [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) que contém as informações a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="042de-111">Pointer to a [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="042de-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="042de-112">Return value</span></span>

<span data-ttu-id="042de-113">Retorna a ID do grupo se for bem-sucedida ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="042de-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="042de-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="042de-114">Remarks</span></span>

<span data-ttu-id="042de-115">Para alterar uma ID de grupo de um grupo existente, adicione <b>LVGF_GROUPID</b> a <b>LVGROUP. Mask</b> e defina <b>LVGROUP. iGroupId</b> como a nova ID.</span><span class="sxs-lookup"><span data-stu-id="042de-115">To change a group ID of an existing group add <b>LVGF_GROUPID</b> to <b>LVGROUP.mask</b> and set <b>LVGROUP.iGroupId</b> to the new ID.</span></span> <span data-ttu-id="042de-116">A chamada falhará se <b>LVGROUP. iGroupId</b> contiver a ID de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="042de-116">The call will fail if <b>LVGROUP.iGroupId</b> contains ID of an existing group.</span></span>

<span data-ttu-id="042de-117">Para atualizar outras propriedades de um grupo existente (por exemplo, atualizar um alinhamento do texto do cabeçalho ou rodapé do grupo, <b>uAlign</b>) <b>LVGROUP. Mask</b> não deve conter <b>LVGF_GROUPID</b>, senão a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="042de-117">To update other properties of an existing group (e.g. update an alignment of the header or footer text for the group, <b>uAlign</b>) <b>LVGROUP.mask</b> must not contain <b>LVGF_GROUPID</b>, else the update will fail.</span></span>

> [!Note]  
> <span data-ttu-id="042de-118">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="042de-118">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="042de-119">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="042de-119">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="042de-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="042de-120">Requirements</span></span>



| <span data-ttu-id="042de-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="042de-121">Requirement</span></span> | <span data-ttu-id="042de-122">Valor</span><span class="sxs-lookup"><span data-stu-id="042de-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="042de-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="042de-123">Minimum supported client</span></span><br/> | <span data-ttu-id="042de-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="042de-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="042de-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="042de-125">Minimum supported server</span></span><br/> | <span data-ttu-id="042de-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="042de-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="042de-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="042de-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="042de-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="042de-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





