---
description: Envia uma mensagem para o controle especificado em uma caixa de diálogo.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: Função _SendDlgItemMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755636"
---
# <a name="_senddlgitemmessage-function"></a><span data-ttu-id="2d0a4-103">\_Função SendDlgItemMessage</span><span class="sxs-lookup"><span data-stu-id="2d0a4-103">\_SendDlgItemMessage function</span></span>

<span data-ttu-id="2d0a4-104">\[Essa função é um wrapper sobre a função **SendDlgItemMessage** .</span><span class="sxs-lookup"><span data-stu-id="2d0a4-104">\[This function is a wrapper over the **SendDlgItemMessage** function.</span></span> <span data-ttu-id="2d0a4-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="2d0a4-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="2d0a4-106">Os aplicativos devem chamar **SendDlgItemMessage** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="2d0a4-106">Applications should call **SendDlgItemMessage** directly.\]</span></span>

<span data-ttu-id="2d0a4-107">Envia uma mensagem para o controle especificado em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2d0a4-107">Sends a message to the specified control in a dialog box.</span></span> <span data-ttu-id="2d0a4-108">Consulte [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span><span class="sxs-lookup"><span data-stu-id="2d0a4-108">See [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0a4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d0a4-109">Syntax</span></span>


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="2d0a4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d0a4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d0a4-111">*...*</span><span class="sxs-lookup"><span data-stu-id="2d0a4-111">*...*</span></span> 
<span data-ttu-id="2d0a4-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2d0a4-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2d0a4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d0a4-113">Requirements</span></span>



| <span data-ttu-id="2d0a4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d0a4-114">Requirement</span></span> | <span data-ttu-id="2d0a4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2d0a4-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d0a4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="2d0a4-116">DLL</span></span><br/> | <dl> <span data-ttu-id="2d0a4-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d0a4-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d0a4-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d0a4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d0a4-119">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="2d0a4-119">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
