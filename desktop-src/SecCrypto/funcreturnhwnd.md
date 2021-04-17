---
description: Usado por um CSP (provedor de serviços de criptografia) para obter o identificador de janela que o CSP deve usar como pai ou proprietário de qualquer interface do usuário que é exibida.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: Ponteiro de função CRYPT_RETURN_HWND (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755048"
---
# <a name="crypt_return_hwnd-function-pointer"></a><span data-ttu-id="44db4-103">\_Ponteiro de \_ função HWND de retorno cript</span><span class="sxs-lookup"><span data-stu-id="44db4-103">CRYPT\_RETURN\_HWND function pointer</span></span>

<span data-ttu-id="44db4-104">A função de retorno de chamada **FuncReturnhWnd** é usada por um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para obter o identificador de janela que o CSP deve usar como pai ou proprietário de qualquer interface do usuário que é exibida.</span><span class="sxs-lookup"><span data-stu-id="44db4-104">The **FuncReturnhWnd** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to obtain the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="44db4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44db4-105">Syntax</span></span>


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a><span data-ttu-id="44db4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44db4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44db4-107">*phWnd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="44db4-107">*phWnd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="44db4-108">O endereço de uma variável **HWND** que recebe o identificador de janela pai.</span><span class="sxs-lookup"><span data-stu-id="44db4-108">The address of an **HWND** variable that receives the parent window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44db4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44db4-109">Return value</span></span>

<span data-ttu-id="44db4-110">Esse ponteiro de função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="44db4-110">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="44db4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44db4-111">Requirements</span></span>



| <span data-ttu-id="44db4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="44db4-112">Requirement</span></span> | <span data-ttu-id="44db4-113">Valor</span><span class="sxs-lookup"><span data-stu-id="44db4-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44db4-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44db4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="44db4-115">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="44db4-115">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44db4-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44db4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="44db4-117">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44db4-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="44db4-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44db4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="44db4-119"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="44db4-119"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44db4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="44db4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44db4-121">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="44db4-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="44db4-122">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="44db4-122">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
