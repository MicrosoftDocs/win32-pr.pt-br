---
description: Recupera o descritor de segurança associado ao compartilhamento DDE. Isso é feito normalmente para edição.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Função NDdeGetShareSecurity (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837056"
---
# <a name="nddegetsharesecurity-function"></a><span data-ttu-id="74ffc-104">Função NDdeGetShareSecurity</span><span class="sxs-lookup"><span data-stu-id="74ffc-104">NDdeGetShareSecurity function</span></span>

<span data-ttu-id="74ffc-105">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="74ffc-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="74ffc-106">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="74ffc-107">Recupera o descritor de segurança associado ao compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="74ffc-107">Retrieves the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="74ffc-108">Isso é feito normalmente para edição.</span><span class="sxs-lookup"><span data-stu-id="74ffc-108">This is done usually for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ffc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74ffc-109">Syntax</span></span>


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a><span data-ttu-id="74ffc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74ffc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ffc-111">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ffc-112">O nome do servidor no qual o DSDM reside.</span><span class="sxs-lookup"><span data-stu-id="74ffc-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="74ffc-113">*lpszShareName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ffc-114">O nome do compartilhamento cujo descritor de segurança deve ser recuperado do DSDM.</span><span class="sxs-lookup"><span data-stu-id="74ffc-114">The name of the share whose security descriptor is to be retrieved from the DSDM.</span></span> <span data-ttu-id="74ffc-115">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="74ffc-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74ffc-116">*si* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-116">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ffc-117">Um valor de [**\_ informações de segurança**](/windows/desktop/SecAuthZ/security-information) que especifica as informações de segurança a serem recuperadas do descritor de segurança associado ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="74ffc-117">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that specifies the security information to be retrieved from the security descriptor associated with the share.</span></span>

</dd> <dt>

<span data-ttu-id="74ffc-118">*PSD* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-118">*pSD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74ffc-119">Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que recebe o descritor de segurança auto-relativo.</span><span class="sxs-lookup"><span data-stu-id="74ffc-119">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that receives the self-relative security descriptor.</span></span> <span data-ttu-id="74ffc-120">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="74ffc-120">This parameter can be **NULL**.</span></span> <span data-ttu-id="74ffc-121">Se esse parâmetro for **NULL**, o DSDM determinará o tamanho das informações de segurança solicitadas e retornará o número de bytes necessários no parâmetro *lpcbsdRequired* juntamente com o \_ código de erro NDDE buf \_ muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="74ffc-121">If this parameter is **NULL**, the DSDM determines the size of the requested security information and returns the number of bytes needed in the *lpcbsdRequired* parameter along with the NDDE\_BUF\_TOO\_SMALL error code.</span></span>

</dd> <dt>

<span data-ttu-id="74ffc-122">*cbSD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-122">*cbSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ffc-123">O tamanho do buffer *PSD* .</span><span class="sxs-lookup"><span data-stu-id="74ffc-123">The size of the *pSD* buffer.</span></span> <span data-ttu-id="74ffc-124">Esse parâmetro deverá ser zero se o *PSD* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="74ffc-124">This parameter must be zero if *pSD* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74ffc-125">*lpcbsdRequired* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-125">*lpcbsdRequired* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74ffc-126">Um ponteiro para a variável que recebe o tamanho real do descritor de segurança recuperado.</span><span class="sxs-lookup"><span data-stu-id="74ffc-126">A pointer to the variable that receives the actual size of the retrieved security descriptor.</span></span> <span data-ttu-id="74ffc-127">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="74ffc-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ffc-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74ffc-128">Return value</span></span>

<span data-ttu-id="74ffc-129">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="74ffc-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="74ffc-130">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="74ffc-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="74ffc-131">Se o parâmetro *PSD* era **nulo**, ele retornará NDDE \_ buf \_ muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="74ffc-131">If the *pSD* parameter was **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="74ffc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74ffc-132">Requirements</span></span>



| <span data-ttu-id="74ffc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="74ffc-133">Requirement</span></span> | <span data-ttu-id="74ffc-134">Valor</span><span class="sxs-lookup"><span data-stu-id="74ffc-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74ffc-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74ffc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="74ffc-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="74ffc-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74ffc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="74ffc-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="74ffc-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="74ffc-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="74ffc-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="74ffc-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="74ffc-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="74ffc-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74ffc-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="74ffc-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74ffc-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="74ffc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="74ffc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74ffc-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74ffc-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="74ffc-145">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="74ffc-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74ffc-146">**NDdeGetShareSecurityW** (Unicode) e **NDdeGetShareSecurityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74ffc-146">**NDdeGetShareSecurityW** (Unicode) and **NDdeGetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="74ffc-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="74ffc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ffc-148">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="74ffc-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="74ffc-149">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="74ffc-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="74ffc-150">**informações de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="74ffc-150">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="74ffc-151">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="74ffc-151">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> </dl>

 

