---
description: Define o descritor de segurança associado ao compartilhamento DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Função NDdeSetShareSecurity (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796402"
---
# <a name="nddesetsharesecurity-function"></a><span data-ttu-id="0b480-103">Função NDdeSetShareSecurity</span><span class="sxs-lookup"><span data-stu-id="0b480-103">NDdeSetShareSecurity function</span></span>

<span data-ttu-id="0b480-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="0b480-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="0b480-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="0b480-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="0b480-106">Define o descritor de segurança associado ao compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="0b480-106">Sets the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="0b480-107">Isso é feito normalmente após a edição da DACL atribuída ao compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="0b480-107">This is done usually after editing the DACL assigned to the DDE share.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b480-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b480-108">Syntax</span></span>


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a><span data-ttu-id="0b480-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b480-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b480-110">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b480-110">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b480-111">O nome do servidor cujo DSDM deve ser modificado.</span><span class="sxs-lookup"><span data-stu-id="0b480-111">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="0b480-112">*lpszShareName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b480-112">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b480-113">O nome do compartilhamento cujo descritor de segurança deve ser modificado.</span><span class="sxs-lookup"><span data-stu-id="0b480-113">The name of the share whose security descriptor is to be modified.</span></span> <span data-ttu-id="0b480-114">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0b480-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0b480-115">*si* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b480-115">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b480-116">Um valor de [**\_ informações de segurança**](/windows/desktop/SecAuthZ/security-information) que identifica as informações de segurança a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="0b480-116">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that identifies the security information to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0b480-117">*PSD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b480-117">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b480-118">Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contém informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="0b480-118">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains security information.</span></span> <span data-ttu-id="0b480-119">Este parâmetro não pode ser **nulo** e deve apontar para um descritor de segurança válido.</span><span class="sxs-lookup"><span data-stu-id="0b480-119">This parameter cannot be **NULL** and should point to a valid security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b480-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b480-120">Return value</span></span>

<span data-ttu-id="0b480-121">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="0b480-121">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="0b480-122">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="0b480-122">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b480-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b480-123">Remarks</span></span>

<span data-ttu-id="0b480-124">Para modificar o [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associado a um compartilhamento DDE no DSDM, o usuário deve ter o privilégio apropriado; o criador de compartilhamento tem esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="0b480-124">To modify the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with a DDE share in the DSDM, the user must have appropriate privilege; the share creator has this privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b480-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b480-125">Requirements</span></span>



| <span data-ttu-id="0b480-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b480-126">Requirement</span></span> | <span data-ttu-id="0b480-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0b480-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b480-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b480-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0b480-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b480-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0b480-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b480-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0b480-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b480-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0b480-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0b480-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b480-133"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b480-133"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b480-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b480-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b480-135"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b480-135"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0b480-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0b480-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b480-137"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b480-137"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b480-138">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0b480-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0b480-139">**NDdeSetShareSecurityW** (Unicode) e **NDdeSetShareSecurityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0b480-139">**NDdeSetShareSecurityW** (Unicode) and **NDdeSetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="0b480-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b480-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b480-141">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="0b480-141">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="0b480-142">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="0b480-142">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="0b480-143">**informações de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="0b480-143">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="0b480-144">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="0b480-144">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)
</dt> </dl>

 

