---
description: Exibe uma caixa de diálogo que permite aos usuários criar, modificar e excluir perfis de verificação.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'Método IScanProfileUI:: ScanProfileDialog (Scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169539"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a><span data-ttu-id="80c79-103">Método IScanProfileUI:: ScanProfileDialog</span><span class="sxs-lookup"><span data-stu-id="80c79-103">IScanProfileUI::ScanProfileDialog method</span></span>

<span data-ttu-id="80c79-104">Exibe uma caixa de diálogo que permite aos usuários criar, modificar e excluir perfis de verificação.</span><span class="sxs-lookup"><span data-stu-id="80c79-104">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c79-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80c79-105">Syntax</span></span>


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="80c79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80c79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c79-107">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80c79-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c79-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="80c79-108">Type: **HWND**</span></span>

<span data-ttu-id="80c79-109">O identificador da janela pai que é proprietária da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="80c79-109">The handle of the parent window that owns the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80c79-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80c79-110">Return value</span></span>

<span data-ttu-id="80c79-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="80c79-111">Type: **HRESULT**</span></span>

<span data-ttu-id="80c79-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="80c79-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80c79-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80c79-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80c79-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="80c79-114">Remarks</span></span>

<span data-ttu-id="80c79-115">A caixa de diálogo é modal; o usuário não pode alternar para a janela pai até que a caixa de diálogo seja fechada.</span><span class="sxs-lookup"><span data-stu-id="80c79-115">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

<span data-ttu-id="80c79-116">Os valores do `<ProfileName>` elemento e do `<WiaItem>` elemento podem ser alterados na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="80c79-116">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed in the dialog box.</span></span> <span data-ttu-id="80c79-117">O `<Default>` elemento pode ser adicionado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="80c79-117">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="80c79-118">Nenhuma outra alteração no perfil de verificação pode ser feita na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="80c79-118">No other changes to the scan profile can be made in the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="80c79-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80c79-119">Requirements</span></span>



| <span data-ttu-id="80c79-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c79-120">Requirement</span></span> | <span data-ttu-id="80c79-121">Valor</span><span class="sxs-lookup"><span data-stu-id="80c79-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c79-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c79-122">Minimum supported client</span></span><br/> | <span data-ttu-id="80c79-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80c79-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="80c79-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c79-124">Minimum supported server</span></span><br/> | <span data-ttu-id="80c79-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80c79-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80c79-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80c79-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="80c79-127"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="80c79-127"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="80c79-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="80c79-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80c79-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80c79-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80c79-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="80c79-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c79-131">**IScanProfileUI**</span><span class="sxs-lookup"><span data-stu-id="80c79-131">**IScanProfileUI**</span></span>](-wia-iscanprofileui.md)
</dt> <dt>

[<span data-ttu-id="80c79-132">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="80c79-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




