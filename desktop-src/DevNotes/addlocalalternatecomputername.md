---
description: Adiciona um nome de rede local alternativo para o computador do qual ele é chamado.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: Função AddLocalAlternateComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751558"
---
# <a name="addlocalalternatecomputername-function"></a><span data-ttu-id="0215e-103">Função AddLocalAlternateComputerName</span><span class="sxs-lookup"><span data-stu-id="0215e-103">AddLocalAlternateComputerName function</span></span>

<span data-ttu-id="0215e-104">Adiciona um nome de rede local alternativo para o computador do qual ele é chamado.</span><span class="sxs-lookup"><span data-stu-id="0215e-104">Adds an alternate local network name for the computer from which it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="0215e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0215e-105">Syntax</span></span>


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0215e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0215e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0215e-107">*lpDnsFQHostname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0215e-107">*lpDnsFQHostname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0215e-108">O nome alternativo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0215e-108">The alternate name to be added.</span></span> <span data-ttu-id="0215e-109">O nome deve estar no formato **ComputerNameDnsFullyQualified** , conforme definido na enumeração [**de \_ \_ formato de nome do computador**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) , e a função [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) deve ser capaz de validá-lo com seu formato definido como **DnsNameHostnameFull**.</span><span class="sxs-lookup"><span data-stu-id="0215e-109">The name must be in the **ComputerNameDnsFullyQualified** format as defined in the [**COMPUTER\_NAME\_FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) enumeration, and the [**DnsValidateName\_W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) function must be able to validate it with its format set to **DnsNameHostnameFull**.</span></span>

</dd> <dt>

<span data-ttu-id="0215e-110">*ulFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0215e-110">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0215e-111">Esse parâmetro é reservado e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="0215e-111">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0215e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0215e-112">Return value</span></span>

<span data-ttu-id="0215e-113">Se a função for bem-sucedida, a função retornará **\_ êxito de erro**.</span><span class="sxs-lookup"><span data-stu-id="0215e-113">If the function succeeds, the function returns **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="0215e-114">Se a função falhar, ela retornará um código de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0215e-114">If the function fails, it returns a nonzero error code.</span></span> <span data-ttu-id="0215e-115">Entre os códigos de erro que ele retorna estão os seguintes:</span><span class="sxs-lookup"><span data-stu-id="0215e-115">Among the error codes that it returns are the following:</span></span>



| <span data-ttu-id="0215e-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0215e-116">Return code</span></span>                                                                                               | <span data-ttu-id="0215e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0215e-117">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0215e-118"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0215e-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="0215e-119">Indica que o parâmetro *lpDnsFQHostname* não aponta para um nome DNS válido ou que o parâmetro *ulFlags* não é igual a zero.</span><span class="sxs-lookup"><span data-stu-id="0215e-119">Indicates that the *lpDnsFQHostname* parameter does not point to a valid DNS name, or that the *ulFlags* parameter is not equal to zero.</span></span><br/> |
| <dl> <span data-ttu-id="0215e-120"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0215e-120"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="0215e-121">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="0215e-121">There is not enough memory to complete the operation.</span></span><br/>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="0215e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0215e-122">Requirements</span></span>



| <span data-ttu-id="0215e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0215e-123">Requirement</span></span> | <span data-ttu-id="0215e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0215e-124">Value</span></span> |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0215e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0215e-125">Library</span></span><br/>                | <dl> <span data-ttu-id="0215e-126"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0215e-126"><dt>Kernel32.lib</dt></span></span> </dl>               |
| <span data-ttu-id="0215e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0215e-127">DLL</span></span><br/>                    | <dl> <span data-ttu-id="0215e-128"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0215e-128"><dt>Kernel32.dll</dt></span></span> </dl>               |
| <span data-ttu-id="0215e-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0215e-129">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="0215e-130">**AddLocalAlternateComputerNameW** (Unicode) e **AddLocalAlternateComputerNameA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0215e-130">**AddLocalAlternateComputerNameW** (Unicode) and **AddLocalAlternateComputerNameA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0215e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0215e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0215e-132">**\_formato do nome do computador \_**</span><span class="sxs-lookup"><span data-stu-id="0215e-132">**COMPUTER\_NAME\_FORMAT**</span></span>](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[<span data-ttu-id="0215e-133">**DnsValidateName \_ W**</span><span class="sxs-lookup"><span data-stu-id="0215e-133">**DnsValidateName\_W**</span></span>](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
