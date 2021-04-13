---
title: Mensagem de HKM_SETHOTKEY (commctrl. h)
description: Define a combinação de teclas de acesso para um controle de tecla quente.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- Controles de HKM_SETHOTKEY de mensagens do Windows
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499332"
---
# <a name="hkm_sethotkey-message"></a><span data-ttu-id="ab865-104">Mensagem HKM setde \_ atalho</span><span class="sxs-lookup"><span data-stu-id="ab865-104">HKM\_SETHOTKEY message</span></span>

<span data-ttu-id="ab865-105">Define a combinação de teclas de acesso para um controle de tecla quente.</span><span class="sxs-lookup"><span data-stu-id="ab865-105">Sets the hot key combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab865-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab865-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab865-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab865-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab865-108">O [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) do [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é o código de chave virtual da tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="ab865-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="ab865-109">O [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) do **LOWORD** é o modificador de chave que indica as chaves que definem uma combinação de teclas de acesso.</span><span class="sxs-lookup"><span data-stu-id="ab865-109">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that indicates the keys that define a hot key combination.</span></span> <span data-ttu-id="ab865-110">Para obter uma lista de valores de sinalizador modificadores, consulte a descrição da mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="ab865-110">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="ab865-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab865-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab865-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ab865-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab865-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab865-113">Return value</span></span>

<span data-ttu-id="ab865-114">Sempre retorna zero.</span><span class="sxs-lookup"><span data-stu-id="ab865-114">Always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab865-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab865-115">Requirements</span></span>



| <span data-ttu-id="ab865-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab865-116">Requirement</span></span> | <span data-ttu-id="ab865-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ab865-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab865-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab865-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ab865-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab865-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab865-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab865-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ab865-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab865-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab865-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab865-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab865-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab865-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

