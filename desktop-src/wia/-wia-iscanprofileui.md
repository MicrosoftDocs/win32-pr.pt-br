---
description: A interface IScanProfileUI permite que os aplicativos exibam uma caixa de diálogo para que os usuários possam criar, modificar e excluir perfis de verificação.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Interface IScanProfileUI (Scanprofileui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798519"
---
# <a name="iscanprofileui-interface"></a><span data-ttu-id="b2e56-103">Interface IScanProfileUI</span><span class="sxs-lookup"><span data-stu-id="b2e56-103">IScanProfileUI interface</span></span>

<span data-ttu-id="b2e56-104">A interface **IScanProfileUI** permite que os aplicativos exibam uma caixa de diálogo para que os usuários possam criar, modificar e excluir perfis de verificação.</span><span class="sxs-lookup"><span data-stu-id="b2e56-104">The **IScanProfileUI** interface enables applications to display a dialog box so that users can create, modify, and delete scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="b2e56-105">Membros</span><span class="sxs-lookup"><span data-stu-id="b2e56-105">Members</span></span>

<span data-ttu-id="b2e56-106">A interface **IScanProfileUI** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b2e56-106">The **IScanProfileUI** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b2e56-107">**IScanProfileUI** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b2e56-107">**IScanProfileUI** also has these types of members:</span></span>

-   [<span data-ttu-id="b2e56-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2e56-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b2e56-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2e56-109">Methods</span></span>

<span data-ttu-id="b2e56-110">A interface **IScanProfileUI** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b2e56-110">The **IScanProfileUI** interface has these methods.</span></span>



| <span data-ttu-id="b2e56-111">Método</span><span class="sxs-lookup"><span data-stu-id="b2e56-111">Method</span></span>                                                             | <span data-ttu-id="b2e56-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2e56-112">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2e56-113">**ScanProfileDialog**</span><span class="sxs-lookup"><span data-stu-id="b2e56-113">**ScanProfileDialog**</span></span>](-wia-iscanprofileui-scanprofiledialog.md) | <span data-ttu-id="b2e56-114">Exibe uma caixa de diálogo que permite aos usuários criar, modificar e excluir perfis de verificação.</span><span class="sxs-lookup"><span data-stu-id="b2e56-114">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2e56-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2e56-115">Remarks</span></span>

<span data-ttu-id="b2e56-116">A caixa de diálogo é modal; o usuário não pode alternar para a janela pai até que a caixa de diálogo seja fechada.</span><span class="sxs-lookup"><span data-stu-id="b2e56-116">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e56-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2e56-117">Requirements</span></span>



| <span data-ttu-id="b2e56-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e56-118">Requirement</span></span> | <span data-ttu-id="b2e56-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b2e56-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e56-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2e56-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e56-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2e56-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b2e56-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2e56-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e56-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2e56-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2e56-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2e56-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2e56-125"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e56-125"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="b2e56-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="b2e56-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b2e56-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b2e56-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e56-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2e56-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e56-129">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="b2e56-129">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="b2e56-130">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="b2e56-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
