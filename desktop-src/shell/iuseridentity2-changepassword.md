---
description: Não há suporte para ChangePassword e ele pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'Método IUserIdentity2:: ChangePassword (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967485"
---
# <a name="iuseridentity2changepassword-method"></a><span data-ttu-id="ccba5-104">Método IUserIdentity2:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="ccba5-104">IUserIdentity2::ChangePassword method</span></span>

<span data-ttu-id="ccba5-105">\[Não há suporte para **ChangePassword** e ele pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="ccba5-105">\[**ChangePassword** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ccba5-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="ccba5-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="ccba5-107">Define uma nova senha para a identidade.</span><span class="sxs-lookup"><span data-stu-id="ccba5-107">Sets a new password for the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccba5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccba5-108">Syntax</span></span>


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a><span data-ttu-id="ccba5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccba5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccba5-110">*szOldPass* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccba5-110">*szOldPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccba5-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="ccba5-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="ccba5-112">A cadeia de caracteres largos que contém a senha atualmente associada à identidade.</span><span class="sxs-lookup"><span data-stu-id="ccba5-112">The wide-character string that contains the password currently associated with the identity.</span></span>

</dd> <dt>

<span data-ttu-id="ccba5-113">_szNewPass \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccba5-113">_szNewPass\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccba5-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="ccba5-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="ccba5-115">A cadeia de caracteres largos que contém a nova senha a ser associada à identidade.</span><span class="sxs-lookup"><span data-stu-id="ccba5-115">The wide-character string that contains the new password to be associated with the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccba5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccba5-116">Return value</span></span>

<span data-ttu-id="ccba5-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ccba5-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ccba5-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ccba5-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ccba5-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccba5-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccba5-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccba5-120">Remarks</span></span>

<span data-ttu-id="ccba5-121">O valor de *szOldPass* deve corresponder à senha atual da identidade para *szNewPass* a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="ccba5-121">The value of *szOldPass* must match the current password of the identity for *szNewPass* to be applied.</span></span> <span data-ttu-id="ccba5-122">Um valor incorreto de *szOldPass* resultará em um valor de retorno de E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="ccba5-122">An incorrect value of *szOldPass* will result in a return value of E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccba5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccba5-123">Requirements</span></span>



| <span data-ttu-id="ccba5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccba5-124">Requirement</span></span> | <span data-ttu-id="ccba5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ccba5-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccba5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccba5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ccba5-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ccba5-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ccba5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccba5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ccba5-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ccba5-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ccba5-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ccba5-130">End of client support</span></span><br/>    | <span data-ttu-id="ccba5-131">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ccba5-131">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="ccba5-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ccba5-132">End of server support</span></span><br/>    | <span data-ttu-id="ccba5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ccba5-133">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="ccba5-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccba5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccba5-135"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccba5-135"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccba5-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="ccba5-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ccba5-137"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ccba5-137"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="ccba5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ccba5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccba5-139"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccba5-139"><dt>Msident.dll</dt></span></span> </dl> |



 

 




