---
description: Define a segurança de uma chave do registro aberta em um hive do registro offline.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Função ORSetKeySecurity (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769137"
---
# <a name="orsetkeysecurity-function"></a><span data-ttu-id="45827-103">Função ORSetKeySecurity</span><span class="sxs-lookup"><span data-stu-id="45827-103">ORSetKeySecurity function</span></span>

<span data-ttu-id="45827-104">Define a segurança de uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="45827-104">Sets the security of an open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="45827-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45827-105">Syntax</span></span>


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="45827-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45827-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45827-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="45827-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45827-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="45827-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="45827-109">*SecurityInformation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45827-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45827-110">Sinalizadores de bits que indicam o tipo de informações de segurança a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="45827-110">Bit flags that indicate the type of security information to set.</span></span> <span data-ttu-id="45827-111">Esse parâmetro pode ser uma combinação dos sinalizadores de bit de [ \_ informações de segurança](../secauthz/security-information.md) .</span><span class="sxs-lookup"><span data-stu-id="45827-111">This parameter can be a combination of the [SECURITY\_INFORMATION](../secauthz/security-information.md) bit flags.</span></span>

</dd> <dt>

<span data-ttu-id="45827-112">*pSecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45827-112">*pSecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45827-113">Um ponteiro para uma estrutura de [ \_ descritor de segurança](/windows/win32/api/winnt/ns-winnt-security_descriptor) que especifica os atributos de segurança a serem definidos para a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="45827-113">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that specifies the security attributes to set for the specified key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45827-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45827-114">Return value</span></span>

<span data-ttu-id="45827-115">Se a função for bem-sucedida, a função retornará êxito de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="45827-115">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="45827-116">Se a função falhar, ela retornará um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="45827-116">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="45827-117">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="45827-117">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="45827-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45827-118">Requirements</span></span>



| <span data-ttu-id="45827-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="45827-119">Requirement</span></span> | <span data-ttu-id="45827-120">Valor</span><span class="sxs-lookup"><span data-stu-id="45827-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45827-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="45827-121">Redistributable</span></span><br/> | <span data-ttu-id="45827-122">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="45827-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="45827-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45827-123">Header</span></span><br/>          | <dl> <span data-ttu-id="45827-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="45827-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="45827-125">DLL</span><span class="sxs-lookup"><span data-stu-id="45827-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="45827-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45827-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45827-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="45827-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45827-128">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="45827-128">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="45827-129">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="45827-129">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="45827-130">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="45827-130">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="45827-131">**ORGetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="45827-131">**ORGetKeySecurity**</span></span>](orgetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="45827-132">\_descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="45827-132">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="45827-133">informações de segurança \_</span><span class="sxs-lookup"><span data-stu-id="45827-133">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
