---
description: Despacha mensagens enviadas de entrada, verifica a fila de mensagens de thread de uma mensagem postada e recupera a mensagem (se houver alguma).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: Função _PeekMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749532"
---
# <a name="_peekmessage-function"></a><span data-ttu-id="bfd29-103">\_Função PeekMessage</span><span class="sxs-lookup"><span data-stu-id="bfd29-103">\_PeekMessage function</span></span>

<span data-ttu-id="bfd29-104">\[Essa função é um wrapper sobre a função **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="bfd29-104">\[This function is a wrapper over the **PeekMessage** function.</span></span> <span data-ttu-id="bfd29-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="bfd29-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="bfd29-106">Os aplicativos devem chamar **PeekMessage** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="bfd29-106">Applications should call **PeekMessage** directly.\]</span></span>

<span data-ttu-id="bfd29-107">Despacha mensagens enviadas de entrada, verifica a fila de mensagens de thread de uma mensagem postada e recupera a mensagem (se houver alguma).</span><span class="sxs-lookup"><span data-stu-id="bfd29-107">Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).</span></span> <span data-ttu-id="bfd29-108">Consulte [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="bfd29-108">See [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd29-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfd29-109">Syntax</span></span>


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="bfd29-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfd29-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfd29-111">*...*</span><span class="sxs-lookup"><span data-stu-id="bfd29-111">*...*</span></span> 
<span data-ttu-id="bfd29-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bfd29-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bfd29-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfd29-113">Requirements</span></span>



| <span data-ttu-id="bfd29-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfd29-114">Requirement</span></span> | <span data-ttu-id="bfd29-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bfd29-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd29-116">DLL</span><span class="sxs-lookup"><span data-stu-id="bfd29-116">DLL</span></span><br/> | <dl> <span data-ttu-id="bfd29-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfd29-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd29-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfd29-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd29-119">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="bfd29-119">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
