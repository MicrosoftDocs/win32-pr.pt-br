---
title: Mensagem de TB_SAVERESTORE (commctrl. h)
description: Envie esta mensagem para iniciar o salvamento ou a restauração de um estado da barra de ferramentas.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- Controles de TB_SAVERESTORE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824151"
---
# <a name="tb_saverestore-message"></a><span data-ttu-id="36c3f-104">TB de \_ mensagem SAVERESTORE</span><span class="sxs-lookup"><span data-stu-id="36c3f-104">TB\_SAVERESTORE message</span></span>

<span data-ttu-id="36c3f-105">Envie esta mensagem para iniciar o salvamento ou a restauração de um estado da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="36c3f-105">Send this message to initiate saving or restoring a toolbar state.</span></span>

## <a name="parameters"></a><span data-ttu-id="36c3f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36c3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36c3f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36c3f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36c3f-108">Sinalizador de salvar ou restaurar.</span><span class="sxs-lookup"><span data-stu-id="36c3f-108">Save or restore flag.</span></span> <span data-ttu-id="36c3f-109">Se esse parâmetro for **true**, as informações serão salvas.</span><span class="sxs-lookup"><span data-stu-id="36c3f-109">If this parameter is **TRUE**, the information is saved.</span></span> <span data-ttu-id="36c3f-110">Se for **false**, as informações serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="36c3f-110">If it is **FALSE**, the information is restored.</span></span>

</dd> <dt>

<span data-ttu-id="36c3f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36c3f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36c3f-112">Ponteiro para uma estrutura [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) que especifica a chave do registro, a subchave e o nome do valor das informações de estado da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="36c3f-112">Pointer to a [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) structure that specifies the registry key, subkey, and value name for the toolbar state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36c3f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36c3f-113">Return value</span></span>

<span data-ttu-id="36c3f-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="36c3f-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c3f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="36c3f-115">Remarks</span></span>

<span data-ttu-id="36c3f-116">Para a versão 4,72 e anterior, para usar essa mensagem para salvar ou restaurar uma barra de ferramentas, a janela pai do controle Toolbar deve implementar um manipulador para o código de notificação [tbn \_ GETBUTTONINFO](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="36c3f-116">For version 4.72 and earlier, to use this message to save or restore a toolbar, the parent window of the toolbar control must implement a handler for the [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification code.</span></span> <span data-ttu-id="36c3f-117">A barra de ferramentas emite essa notificação para recuperar informações sobre cada botão conforme ele é restaurado.</span><span class="sxs-lookup"><span data-stu-id="36c3f-117">The toolbar issues this notification to retrieve information about each button as it is restored.</span></span>

<span data-ttu-id="36c3f-118">A versão 5,80 inclui uma nova opção salvar/restaurar.</span><span class="sxs-lookup"><span data-stu-id="36c3f-118">Version 5.80 includes a new save/restore option.</span></span> <span data-ttu-id="36c3f-119">No início do processo e, como cada botão é salvo ou restaurado, seu aplicativo receberá uma notificação [tbn \_ Save](tbn-save.md) ou [tbn \_ Restore](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="36c3f-119">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification.</span></span> <span data-ttu-id="36c3f-120">Para usar essa opção, você deve implementar manipuladores de notificação para fornecer ao shell as informações de bitmap e estado necessárias para salvar ou restaurar com êxito o estado da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="36c3f-120">To use this option, you must implement notification handlers to provide the Shell with the bitmap and state information it needs to successfully save or restore the toolbar state.</span></span>

## <a name="requirements"></a><span data-ttu-id="36c3f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36c3f-121">Requirements</span></span>



| <span data-ttu-id="36c3f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36c3f-122">Requirement</span></span> | <span data-ttu-id="36c3f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="36c3f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36c3f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36c3f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36c3f-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36c3f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36c3f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36c3f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36c3f-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36c3f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36c3f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36c3f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="36c3f-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c3f-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="36c3f-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="36c3f-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="36c3f-131">**TB \_ SAVERESTOREW** (Unicode) e **TB \_ SAVERESTOREA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="36c3f-131">**TB\_SAVERESTOREW** (Unicode) and **TB\_SAVERESTOREA** (ANSI)</span></span><br/>             |



 

 





