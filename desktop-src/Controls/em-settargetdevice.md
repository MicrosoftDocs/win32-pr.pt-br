---
title: Mensagem de EM_SETTARGETDEVICE (RichEdit. h)
description: Define o dispositivo de destino e a largura da linha usada para \ 0034; o que você vê é o que você obtém \ 0034; (WYSIWYG) em um controle de edição com formatação.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- Controles de EM_SETTARGETDEVICE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085734"
---
# <a name="em_settargetdevice-message"></a><span data-ttu-id="b19ea-104">\_Mensagem em SETTARGETDEVICE</span><span class="sxs-lookup"><span data-stu-id="b19ea-104">EM\_SETTARGETDEVICE message</span></span>

<span data-ttu-id="b19ea-105">Define o dispositivo de destino e a largura da linha usada para a formatação "o que você vê é o que você obtém" (WYSIWYG) em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="b19ea-105">Sets the target device and line width used for "what you see is what you get" (WYSIWYG) formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b19ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b19ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b19ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b19ea-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b19ea-108">HDC para o dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="b19ea-108">HDC for the target device.</span></span>

</dd> <dt>

<span data-ttu-id="b19ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b19ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b19ea-110">Largura da linha a ser usada para formatação.</span><span class="sxs-lookup"><span data-stu-id="b19ea-110">Line width to use for formatting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b19ea-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b19ea-111">Return value</span></span>

<span data-ttu-id="b19ea-112">O valor de retorno será zero se a operação falhar ou for diferente de zero se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="b19ea-112">The return value is zero if the operation fails, or nonzero if it succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="b19ea-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b19ea-113">Remarks</span></span>

<span data-ttu-id="b19ea-114">O HDC para a impressora padrão pode ser obtido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b19ea-114">The HDC for the default printer can be obtained as follows.</span></span>


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



<span data-ttu-id="b19ea-115">Se *lParam* for zero, nenhuma quebra de linha será criada.</span><span class="sxs-lookup"><span data-stu-id="b19ea-115">If *lParam* is zero, no line breaks are created.</span></span>

## <a name="requirements"></a><span data-ttu-id="b19ea-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b19ea-116">Requirements</span></span>



| <span data-ttu-id="b19ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b19ea-117">Requirement</span></span> | <span data-ttu-id="b19ea-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b19ea-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b19ea-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b19ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b19ea-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b19ea-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b19ea-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b19ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b19ea-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b19ea-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b19ea-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b19ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b19ea-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b19ea-124"><dt>Richedit.h</dt></span></span> </dl> |



 

 





