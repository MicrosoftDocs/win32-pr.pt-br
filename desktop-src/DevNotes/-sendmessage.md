---
description: Envia a mensagem especificada para uma janela ou Windows.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: Função _SendMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748930"
---
# <a name="_sendmessage-function"></a><span data-ttu-id="53931-103">\_Função SendMessage</span><span class="sxs-lookup"><span data-stu-id="53931-103">\_SendMessage function</span></span>

<span data-ttu-id="53931-104">\[Essa função é um wrapper sobre a função **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="53931-104">\[This function is a wrapper over the **SendMessage** function.</span></span> <span data-ttu-id="53931-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="53931-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="53931-106">Os aplicativos devem chamar **SendMessage** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="53931-106">Applications should call **SendMessage** directly.\]</span></span>

<span data-ttu-id="53931-107">Envia a mensagem especificada para uma janela ou Windows.</span><span class="sxs-lookup"><span data-stu-id="53931-107">Sends the specified message to a window or windows.</span></span> <span data-ttu-id="53931-108">Consulte [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="53931-108">See [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="53931-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53931-109">Syntax</span></span>


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="53931-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53931-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53931-111">*...*</span><span class="sxs-lookup"><span data-stu-id="53931-111">*...*</span></span> 
<span data-ttu-id="53931-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="53931-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="53931-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53931-113">Requirements</span></span>



| <span data-ttu-id="53931-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="53931-114">Requirement</span></span> | <span data-ttu-id="53931-115">Valor</span><span class="sxs-lookup"><span data-stu-id="53931-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53931-116">DLL</span><span class="sxs-lookup"><span data-stu-id="53931-116">DLL</span></span><br/> | <dl> <span data-ttu-id="53931-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53931-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53931-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="53931-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53931-119">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="53931-119">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
