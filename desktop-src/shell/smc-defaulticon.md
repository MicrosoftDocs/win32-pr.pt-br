---
description: Retorna o ícone padrão para o item especificado pela estrutura SMDATA que o acompanha.
title: Mensagem de SMC_DEFAULTICON (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10edab26c87dae4b1c9d2d5f06390fc608ba1edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989026"
---
# <a name="smc_defaulticon-message"></a><span data-ttu-id="d6e52-103">\_Mensagem de DEFAULTicon do SMC</span><span class="sxs-lookup"><span data-stu-id="d6e52-103">SMC\_DEFAULTICON message</span></span>

<span data-ttu-id="d6e52-104">Retorna o ícone padrão para o item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="d6e52-104">Return the default icon for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a><span data-ttu-id="d6e52-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6e52-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e52-106">*pwszIcon*</span><span class="sxs-lookup"><span data-stu-id="d6e52-106">*pwszIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="d6e52-107">Um ponteiro para uma cadeia de caracteres que recebe o caminho totalmente qualificado do arquivo que contém o ícone padrão.</span><span class="sxs-lookup"><span data-stu-id="d6e52-107">A pointer to a string that receives the fully qualified path of the file that contains the default icon.</span></span>

</dd> <dt>

<span data-ttu-id="d6e52-108">*iIcon*</span><span class="sxs-lookup"><span data-stu-id="d6e52-108">*iIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="d6e52-109">Um ponteiro para um inteiro que recebe o índice do ícone no arquivo especificado por *pwszIcon*.</span><span class="sxs-lookup"><span data-stu-id="d6e52-109">A pointer to an integer that receives the index of the icon in the file specified by *pwszIcon*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e52-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6e52-110">Return value</span></span>

<span data-ttu-id="d6e52-111">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d6e52-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6e52-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6e52-112">Remarks</span></span>

<span data-ttu-id="d6e52-113">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="d6e52-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e52-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6e52-114">Requirements</span></span>



| <span data-ttu-id="d6e52-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6e52-115">Requirement</span></span> | <span data-ttu-id="d6e52-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d6e52-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e52-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6e52-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e52-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6e52-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d6e52-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6e52-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e52-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6e52-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6e52-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d6e52-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6e52-122"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e52-122"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6e52-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="d6e52-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6e52-124"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6e52-124"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




