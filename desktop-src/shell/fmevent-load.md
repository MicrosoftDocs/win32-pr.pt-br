---
description: Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver carregando a DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Mensagem de FMEVENT_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967939"
---
# <a name="fmevent_load-message"></a><span data-ttu-id="37903-103">FMEVENT \_ carregar mensagem</span><span class="sxs-lookup"><span data-stu-id="37903-103">FMEVENT\_LOAD message</span></span>

<span data-ttu-id="37903-104">Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver carregando a DLL.</span><span class="sxs-lookup"><span data-stu-id="37903-104">Sent to an extension DLL when File Manager is loading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="37903-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37903-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37903-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37903-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37903-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="37903-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="37903-108">*lpfmsld*</span><span class="sxs-lookup"><span data-stu-id="37903-108">*lpfmsld*</span></span> 
</dt> <dd>

<span data-ttu-id="37903-109">O endereço de uma estrutura de [**\_ carga do FMS**](fms-load.md) que especifica o valor delta do item de menu.</span><span class="sxs-lookup"><span data-stu-id="37903-109">The address of an [**FMS\_LOAD**](fms-load.md) structure that specifies the menu item delta value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37903-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37903-110">Return value</span></span>

<span data-ttu-id="37903-111">Uma extensão DLL deve retornar **true** para continuar carregando a dll.</span><span class="sxs-lookup"><span data-stu-id="37903-111">An extension DLL must return **TRUE** to continue loading the DLL.</span></span> <span data-ttu-id="37903-112">Se a DLL retornar **false**, o Gerenciador de arquivos chamará a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e encerrará qualquer comunicação com a extensão dll.</span><span class="sxs-lookup"><span data-stu-id="37903-112">If the DLL returns **FALSE**, File Manager calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function and ends any communication with the extension DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="37903-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="37903-113">Remarks</span></span>

<span data-ttu-id="37903-114">Um aplicativo deve preencher os membros **dwSize**, **szMenuName** e **HMENU** na estrutura de [**\_ carga do FMS**](fms-load.md) .</span><span class="sxs-lookup"><span data-stu-id="37903-114">An application should fill the **dwSize**, **szMenuName**, and **hMenu** members in the [**FMS\_LOAD**](fms-load.md) structure.</span></span> <span data-ttu-id="37903-115">Ele também deve salvar o valor do membro **wMenuDelta** e usá-lo para identificar itens de menu ao modificar o menu.</span><span class="sxs-lookup"><span data-stu-id="37903-115">It should also save the value of the **wMenuDelta** member and use it to identify menu items when modifying the menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="37903-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37903-116">Requirements</span></span>



| <span data-ttu-id="37903-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37903-117">Requirement</span></span> | <span data-ttu-id="37903-118">Valor</span><span class="sxs-lookup"><span data-stu-id="37903-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37903-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37903-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37903-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="37903-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="37903-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37903-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37903-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="37903-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37903-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="37903-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="37903-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="37903-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37903-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="37903-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37903-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="37903-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
