---
title: Mensagem de LVM_GETGROUPINFO (commctrl. h)
description: Obtém informações do grupo.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- Controles de LVM_GETGROUPINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009201"
---
# <a name="lvm_getgroupinfo-message"></a><span data-ttu-id="31ba6-104">\_Mensagem GETGROUPINFO LVM</span><span class="sxs-lookup"><span data-stu-id="31ba6-104">LVM\_GETGROUPINFO message</span></span>

<span data-ttu-id="31ba6-105">Obtém informações do grupo.</span><span class="sxs-lookup"><span data-stu-id="31ba6-105">Gets group information.</span></span>

## <a name="parameters"></a><span data-ttu-id="31ba6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31ba6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ba6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31ba6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="31ba6-108">Uma ID que especifica o grupo cujas informações são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="31ba6-108">An ID that specifies the group whose information is retrieved.</span></span></dd> <dt>

<span data-ttu-id="31ba6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31ba6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="31ba6-110">Um ponteiro de uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que recebe as informações recuperadas.</span><span class="sxs-lookup"><span data-stu-id="31ba6-110">A pointer an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that receives the retrieved information.</span></span> <span data-ttu-id="31ba6-111">Defina o membro **cbSize** dessa estrutura como sizeof (LVGROUP).</span><span class="sxs-lookup"><span data-stu-id="31ba6-111">Set the **cbSize** member of this structure to sizeof(LVGROUP).</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ba6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31ba6-112">Return value</span></span>

<span data-ttu-id="31ba6-113">Retorna a ID do grupo se for bem-sucedida ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="31ba6-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ba6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="31ba6-114">Remarks</span></span>

<span data-ttu-id="31ba6-115">Antes de tentar recuperar o cabeçalho de um grupo, primeiro verifique se o grupo não tem o \_ estilo NOheader LBGS.</span><span class="sxs-lookup"><span data-stu-id="31ba6-115">Before attempting to retrieve the header for a group, first ensure that the group does not have the LBGS\_NOHEADER style.</span></span>

> [!Note]  
> <span data-ttu-id="31ba6-116">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="31ba6-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="31ba6-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31ba6-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="31ba6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31ba6-118">Requirements</span></span>



| <span data-ttu-id="31ba6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="31ba6-119">Requirement</span></span> | <span data-ttu-id="31ba6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="31ba6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31ba6-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31ba6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="31ba6-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31ba6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31ba6-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31ba6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="31ba6-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31ba6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31ba6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31ba6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ba6-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31ba6-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





