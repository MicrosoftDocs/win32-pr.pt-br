---
description: Formata uma cadeia de caracteres de mensagem.
ms.assetid: e5513b0d-5f93-4bcd-a011-eb4a6fab91e1
title: Função _FormatMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _FormatMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 27cbcfb0d69d0b4dec72834bfc8f69a9f97048ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751559"
---
# <a name="_formatmessage-function"></a><span data-ttu-id="8e960-103">\_Função FormatMessage</span><span class="sxs-lookup"><span data-stu-id="8e960-103">\_FormatMessage function</span></span>

<span data-ttu-id="8e960-104">\[Essa função é um wrapper sobre a função **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="8e960-104">\[This function is a wrapper over the **FormatMessage** function.</span></span> <span data-ttu-id="8e960-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="8e960-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="8e960-106">Os aplicativos devem chamar **FormatMessage** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="8e960-106">Applications should call **FormatMessage** directly.\]</span></span>

<span data-ttu-id="8e960-107">Formata uma cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8e960-107">Formats a message string.</span></span> <span data-ttu-id="8e960-108">Consulte [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage).</span><span class="sxs-lookup"><span data-stu-id="8e960-108">See [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e960-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e960-109">Syntax</span></span>


```C++
DWORD _FormatMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="8e960-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e960-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e960-111">*...*</span><span class="sxs-lookup"><span data-stu-id="8e960-111">*...*</span></span> 
<span data-ttu-id="8e960-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8e960-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8e960-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e960-113">Requirements</span></span>



| <span data-ttu-id="8e960-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e960-114">Requirement</span></span> | <span data-ttu-id="8e960-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8e960-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e960-116">DLL</span><span class="sxs-lookup"><span data-stu-id="8e960-116">DLL</span></span><br/> | <dl> <span data-ttu-id="8e960-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e960-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e960-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e960-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e960-119">**FormatMessage**</span><span class="sxs-lookup"><span data-stu-id="8e960-119">**FormatMessage**</span></span>](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> </dl>

 

 
