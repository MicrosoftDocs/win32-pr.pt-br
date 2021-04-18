---
description: Recupera uma cópia do descritor de segurança protegendo a chave do registro aberta especificada em um hive do registro offline.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Função ORGetKeySecurity (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750131"
---
# <a name="orgetkeysecurity-function"></a><span data-ttu-id="7f391-103">Função ORGetKeySecurity</span><span class="sxs-lookup"><span data-stu-id="7f391-103">ORGetKeySecurity function</span></span>

<span data-ttu-id="7f391-104">Recupera uma cópia do descritor de segurança protegendo a chave do registro aberta especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="7f391-104">Retrieves a copy of the security descriptor protecting the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f391-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f391-105">Syntax</span></span>


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="7f391-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f391-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f391-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7f391-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f391-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="7f391-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="7f391-109">*SecurityInformation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f391-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f391-110">Um valor de [ \_ informações de segurança](../secauthz/security-information.md) que indica as informações de segurança solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7f391-110">A [SECURITY\_INFORMATION](../secauthz/security-information.md) value that indicates the requested security information.</span></span>

</dd> <dt>

<span data-ttu-id="7f391-111">*pSecurityDescriptor* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7f391-111">*pSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f391-112">Um ponteiro para um buffer que recebe uma cópia do descritor de segurança solicitado.</span><span class="sxs-lookup"><span data-stu-id="7f391-112">A pointer to a buffer that receives a copy of the requested security descriptor.</span></span> <span data-ttu-id="7f391-113">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7f391-113">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7f391-114">*lpcbSecurityDescriptor* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7f391-114">*lpcbSecurityDescriptor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f391-115">Um ponteiro para uma variável que especifica o tamanho, em bytes, do buffer apontado pelo parâmetro *pSecurityDescriptor* .</span><span class="sxs-lookup"><span data-stu-id="7f391-115">A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the *pSecurityDescriptor* parameter.</span></span> <span data-ttu-id="7f391-116">Quando a função retorna, a variável contém o número de bytes gravados no buffer.</span><span class="sxs-lookup"><span data-stu-id="7f391-116">When the function returns, the variable contains the number of bytes written to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f391-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f391-117">Return value</span></span>

<span data-ttu-id="7f391-118">Se a função for bem-sucedida, a função retornará êxito de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="7f391-118">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="7f391-119">Se a função falhar, ela retornará um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="7f391-119">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="7f391-120">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="7f391-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="7f391-121">Se o buffer especificado pelo parâmetro *pSecurityDescriptor* for muito pequeno, a função retornará um \_ buffer insuficiente de erro \_ e o parâmetro *lpcbSecurityDescriptor* conterá o número de bytes necessários para o descritor de segurança solicitado.</span><span class="sxs-lookup"><span data-stu-id="7f391-121">If the buffer specified by the *pSecurityDescriptor* parameter is too small, the function returns ERROR\_INSUFFICIENT\_BUFFER and the *lpcbSecurityDescriptor* parameter contains the number of bytes required for the requested security descriptor.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f391-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f391-122">Requirements</span></span>



| <span data-ttu-id="7f391-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f391-123">Requirement</span></span> | <span data-ttu-id="7f391-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7f391-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f391-125">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7f391-125">Redistributable</span></span><br/> | <span data-ttu-id="7f391-126">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7f391-126">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="7f391-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f391-127">Header</span></span><br/>          | <dl> <span data-ttu-id="7f391-128"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f391-128"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f391-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7f391-129">DLL</span></span><br/>             | <dl> <span data-ttu-id="7f391-130"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f391-130"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f391-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f391-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f391-132">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="7f391-132">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="7f391-133">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="7f391-133">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="7f391-134">**ORSetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="7f391-134">**ORSetKeySecurity**</span></span>](orsetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="7f391-135">informações de segurança \_</span><span class="sxs-lookup"><span data-stu-id="7f391-135">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
