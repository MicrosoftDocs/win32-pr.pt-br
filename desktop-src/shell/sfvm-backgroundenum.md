---
description: 'Permite que o objeto de retorno de chamada solicite a enumeração em um thread em segundo plano. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_BACKGROUNDENUM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989043"
---
# <a name="sfvm_backgroundenum-message"></a><span data-ttu-id="d736d-104">\_Mensagem SFVM BACKGROUNDENUM</span><span class="sxs-lookup"><span data-stu-id="d736d-104">SFVM\_BACKGROUNDENUM message</span></span>

<span data-ttu-id="d736d-105">Permite que o objeto de retorno de chamada solicite a enumeração em um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d736d-105">Allows the callback object to request enumeration on a background thread.</span></span> <span data-ttu-id="d736d-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="d736d-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a><span data-ttu-id="d736d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d736d-107">Parameters</span></span>

<span data-ttu-id="d736d-108">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d736d-108">This message has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d736d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d736d-109">Remarks</span></span>

<span data-ttu-id="d736d-110">Em resposta a essa notificação, retorne S \_ OK para habilitar a enumeração em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d736d-110">In response to this notification, return S\_OK to enable background enumeration.</span></span> <span data-ttu-id="d736d-111">Por padrão, o objeto de pasta do sistema exibirá a animação "lanterna" enquanto a enumeração estiver ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="d736d-111">By default, the system folder object will display the "flashlight" animation while the enumeration is taking place.</span></span> <span data-ttu-id="d736d-112">Para especificar uma animação personalizada, manipule [**SFVM \_ getanimation**](sfvm-getanimation.md).</span><span class="sxs-lookup"><span data-stu-id="d736d-112">To specify a custom animation, handle [**SFVM\_GETANIMATION**](sfvm-getanimation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d736d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d736d-113">Requirements</span></span>



| <span data-ttu-id="d736d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d736d-114">Requirement</span></span> | <span data-ttu-id="d736d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d736d-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d736d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d736d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d736d-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d736d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d736d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d736d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d736d-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d736d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d736d-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d736d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d736d-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d736d-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
