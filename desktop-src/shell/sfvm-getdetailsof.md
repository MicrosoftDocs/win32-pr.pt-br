---
description: SFVM \_ GETDETAILSOF pode ser alterado ou indisponível.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: Mensagem de SFVM_GETDETAILSOF (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968067"
---
# <a name="sfvm_getdetailsof-message"></a><span data-ttu-id="1e573-103">\_Mensagem SFVM GETDETAILSOF</span><span class="sxs-lookup"><span data-stu-id="1e573-103">SFVM\_GETDETAILSOF message</span></span>

<span data-ttu-id="1e573-104">\[**SFVM \_ O GETDETAILSOF** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1e573-104">\[**SFVM\_GETDETAILSOF** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1e573-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="1e573-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="1e573-106">Permite que o objeto de retorno de chamada forneça os detalhes de um item em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="1e573-106">Allows the callback object to provide the details for an item in a Shell folder.</span></span> <span data-ttu-id="1e573-107">Use somente se uma chamada para [**IShellFolder2:: GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) falhar e não houver nenhum método [**IShellDetails:: GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) disponível para chamar.</span><span class="sxs-lookup"><span data-stu-id="1e573-107">Use only if a call to [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fails and there is no [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) method available to call.</span></span> <span data-ttu-id="1e573-108">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="1e573-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a><span data-ttu-id="1e573-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e573-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e573-110">*IColumn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e573-110">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e573-111">A ID de base zero da coluna.</span><span class="sxs-lookup"><span data-stu-id="1e573-111">The zero-based ID of the column.</span></span>

</dd> <dt>

<span data-ttu-id="1e573-112">*pDi* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1e573-112">*pDi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e573-113">Um ponteiro para uma estrutura [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) preenchida com as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="1e573-113">A pointer to a [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) structure filled with the requested information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e573-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e573-114">Requirements</span></span>



| <span data-ttu-id="1e573-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e573-115">Requirement</span></span> | <span data-ttu-id="1e573-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1e573-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1e573-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e573-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1e573-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1e573-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1e573-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e573-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1e573-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e573-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1e573-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1e573-121">End of client support</span></span><br/>    | <span data-ttu-id="1e573-122">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="1e573-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="1e573-123">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1e573-123">End of server support</span></span><br/>    | <span data-ttu-id="1e573-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e573-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="1e573-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e573-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e573-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e573-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
