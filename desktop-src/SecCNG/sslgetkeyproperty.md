---
description: Recupera o valor de uma propriedade nomeada para um objeto de chave do provedor de protocolo SSL (protocolo SSL).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Função SslGetKeyProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753412"
---
# <a name="sslgetkeyproperty-function"></a><span data-ttu-id="95ebc-103">Função SslGetKeyProperty</span><span class="sxs-lookup"><span data-stu-id="95ebc-103">SslGetKeyProperty function</span></span>

<span data-ttu-id="95ebc-104">A função **SslGetKeyProperty** recupera o valor de uma propriedade nomeada para um objeto de chave do provedor de protocolo SSL ( [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="95ebc-104">The **SslGetKeyProperty** function retrieves the value of a named property for a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider key object.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ebc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95ebc-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="95ebc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95ebc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ebc-107">*HKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-107">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ebc-108">O identificador do provedor SSL.</span><span class="sxs-lookup"><span data-stu-id="95ebc-108">The handle of the SSL provider.</span></span>

</dd> <dt>

<span data-ttu-id="95ebc-109">*pszProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ebc-110">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome da propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="95ebc-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span> <span data-ttu-id="95ebc-111">Pode ser um dos [**identificadores de propriedade de armazenamento de chave**](key-storage-property-identifiers.md) predefinidos ou um identificador de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="95ebc-111">This can be one of the predefined [**Key Storage Property Identifiers**](key-storage-property-identifiers.md) or a custom property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="95ebc-112">*ppbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-112">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95ebc-113">Um ponteiro para um buffer que recebe o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="95ebc-113">A pointer to a buffer that receives the property value.</span></span> <span data-ttu-id="95ebc-114">O chamador da função deve liberar esse buffer chamando a função [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="95ebc-114">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="95ebc-115">*pcbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-115">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95ebc-116">O tamanho, em bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="95ebc-116">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="95ebc-117">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ebc-118">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="95ebc-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ebc-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95ebc-119">Return value</span></span>

<span data-ttu-id="95ebc-120">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="95ebc-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="95ebc-121">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="95ebc-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="95ebc-122">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="95ebc-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="95ebc-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="95ebc-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="95ebc-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="95ebc-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="95ebc-125"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="95ebc-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="95ebc-126">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="95ebc-126">One of the provided handles is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="95ebc-127"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="95ebc-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="95ebc-128">Um dos parâmetros fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="95ebc-128">One of the supplied parameters is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="95ebc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95ebc-129">Requirements</span></span>



| <span data-ttu-id="95ebc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="95ebc-130">Requirement</span></span> | <span data-ttu-id="95ebc-131">Valor</span><span class="sxs-lookup"><span data-stu-id="95ebc-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="95ebc-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95ebc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="95ebc-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-133">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="95ebc-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95ebc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="95ebc-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="95ebc-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95ebc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="95ebc-137"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="95ebc-137"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="95ebc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="95ebc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95ebc-139"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95ebc-139"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

