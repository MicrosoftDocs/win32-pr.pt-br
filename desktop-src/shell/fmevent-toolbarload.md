---
description: Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver carregando sua barra de ferramentas. Essa mensagem permite que uma DLL de extensão adicione um botão à barra de ferramentas do Gerenciador de arquivos.
title: Mensagem de FMEVENT_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169442"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="e0f57-104">\_Mensagem FMEVENT TOOLBARLOAD</span><span class="sxs-lookup"><span data-stu-id="e0f57-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="e0f57-105">Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver carregando sua barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e0f57-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="e0f57-106">Essa mensagem permite que uma DLL de extensão adicione um botão à barra de ferramentas do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e0f57-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0f57-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0f57-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f57-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0f57-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e0f57-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e0f57-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e0f57-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="e0f57-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="e0f57-111">O endereço de uma estrutura de [**\_ TOOLBARLOAD do FMS**](fms-toolbarload.md) .</span><span class="sxs-lookup"><span data-stu-id="e0f57-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="e0f57-112">Se a extensão DLL adicionar um botão à barra de ferramentas no Gerenciador de arquivos, a DLL deverá preencher a estrutura com informações sobre o botão.</span><span class="sxs-lookup"><span data-stu-id="e0f57-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f57-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0f57-113">Return value</span></span>

<span data-ttu-id="e0f57-114">Uma extensão DLL deve retornar **true** para adicionar o botão à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e0f57-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="e0f57-115">Se a DLL retornar **false**, o Gerenciador de arquivos não adicionará o botão.</span><span class="sxs-lookup"><span data-stu-id="e0f57-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f57-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0f57-116">Requirements</span></span>



| <span data-ttu-id="e0f57-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f57-117">Requirement</span></span> | <span data-ttu-id="e0f57-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e0f57-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f57-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0f57-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f57-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0f57-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e0f57-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0f57-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f57-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0f57-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0f57-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e0f57-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0f57-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0f57-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f57-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0f57-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f57-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="e0f57-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




