---
description: Recupera o valor de uma propriedade de provedor especificada.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Função SslGetProviderProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829663"
---
# <a name="sslgetproviderproperty-function"></a><span data-ttu-id="d1138-103">Função SslGetProviderProperty</span><span class="sxs-lookup"><span data-stu-id="d1138-103">SslGetProviderProperty function</span></span>

<span data-ttu-id="d1138-104">A função **SslGetProviderProperty** recupera o valor de uma propriedade de provedor especificada.</span><span class="sxs-lookup"><span data-stu-id="d1138-104">The **SslGetProviderProperty** function retrieves the value of a specified provider property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1138-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1138-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d1138-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1138-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1138-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1138-108">O identificador do provedor de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL) para o qual recuperar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="d1138-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider for which to retrieve the property.</span></span>

</dd> <dt>

<span data-ttu-id="d1138-109">*pszProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1138-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1138-110">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome da propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="d1138-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d1138-111">*ppbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d1138-111">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1138-112">O endereço de um buffer que recebe o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d1138-112">The address of a buffer that receives the property value.</span></span>

<span data-ttu-id="d1138-113">O chamador da função deve liberar esse buffer chamando a função [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d1138-113">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d1138-114">*pcbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d1138-114">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1138-115">O tamanho, em bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="d1138-115">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d1138-116">*ppEnumState* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d1138-116">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1138-117">O endereço de um ponteiro **void** que recebe informações de estado de enumeração que são usadas em chamadas subsequentes para essa função.</span><span class="sxs-lookup"><span data-stu-id="d1138-117">The address of a **VOID** pointer that receives enumeration state information that is used in subsequent calls to this function.</span></span> <span data-ttu-id="d1138-118">Essas informações só têm significado para o provedor SSL e são opacas para o chamador.</span><span class="sxs-lookup"><span data-stu-id="d1138-118">This information only has meaning to the SSL provider and is opaque to the caller.</span></span> <span data-ttu-id="d1138-119">O provedor SSL usa essas informações para determinar qual item está em seguida na enumeração.</span><span class="sxs-lookup"><span data-stu-id="d1138-119">The SSL provider uses this information to determine which item is next in the enumeration.</span></span> <span data-ttu-id="d1138-120">Se a variável apontada por esse parâmetro contiver **NULL**, a enumeração será iniciada desde o início.</span><span class="sxs-lookup"><span data-stu-id="d1138-120">If the variable pointed to by this parameter contains **NULL**, the enumeration is started from the beginning.</span></span>

<span data-ttu-id="d1138-121">O chamador da função deve liberar essa memória chamando a função [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d1138-121">The caller of the function must free this memory by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d1138-122">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1138-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1138-123">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d1138-123">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1138-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1138-124">Return value</span></span>

<span data-ttu-id="d1138-125">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="d1138-125">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="d1138-126">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d1138-126">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="d1138-127">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="d1138-127">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="d1138-128">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d1138-128">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="d1138-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1138-129">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1138-130"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="d1138-130"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="d1138-131">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="d1138-131">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="d1138-132"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="d1138-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="d1138-133">O identificador *hSslProvider* não é válido.</span><span class="sxs-lookup"><span data-stu-id="d1138-133">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="d1138-134"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="d1138-134"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="d1138-135">Um dos parâmetros fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="d1138-135">One of the supplied parameters is not valid.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="d1138-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1138-136">Requirements</span></span>



| <span data-ttu-id="d1138-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1138-137">Requirement</span></span> | <span data-ttu-id="d1138-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d1138-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1138-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1138-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d1138-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1138-140">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d1138-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1138-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d1138-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1138-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d1138-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1138-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1138-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1138-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="d1138-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d1138-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1138-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1138-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

