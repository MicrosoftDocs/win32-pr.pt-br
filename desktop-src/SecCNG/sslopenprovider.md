---
description: Abre um identificador para o provedor de protocolo do protocolo de protocolo SSL especificado (SSL).
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Função SslOpenProvider (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164394"
---
# <a name="sslopenprovider-function"></a><span data-ttu-id="85bd0-103">Função SslOpenProvider</span><span class="sxs-lookup"><span data-stu-id="85bd0-103">SslOpenProvider function</span></span>

<span data-ttu-id="85bd0-104">A função **SslOpenProvider** abre um identificador para o provedor de protocolo do [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) especificado (SSL).</span><span class="sxs-lookup"><span data-stu-id="85bd0-104">The **SslOpenProvider** function opens a handle to the specified [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="85bd0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85bd0-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="85bd0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85bd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85bd0-107">*phSslProvider* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85bd0-107">*phSslProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85bd0-108">O endereço de um **\_ \_ identificador de Prov de NCRYPT** no qual gravar o identificador do provedor.</span><span class="sxs-lookup"><span data-stu-id="85bd0-108">The address of an **NCRYPT\_PROV\_HANDLE** in which to write the provider handle.</span></span>

<span data-ttu-id="85bd0-109">Quando terminar de usar o identificador, você deverá liberá-lo chamando a função [**SslFreeObject**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="85bd0-109">When you have finished using the handle, you should free it by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="85bd0-110">*pszProviderName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85bd0-110">*pszProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85bd0-111">Um ponteiro para uma cadeia de caracteres Unicode que contém o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="85bd0-111">A pointer to a Unicode string that contains the provider name.</span></span> <span data-ttu-id="85bd0-112">Se o valor desse parâmetro for **NULL**, um identificador para o **provedor do \_ MS \_ Schannel** será retornado.</span><span class="sxs-lookup"><span data-stu-id="85bd0-112">If the value of this parameter is **NULL**, a handle to the **MS\_SCHANNEL\_PROVIDER** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="85bd0-113">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85bd0-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85bd0-114">Esse parâmetro é reservado para uso futuro e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="85bd0-114">This parameter is reserved for future use, and it must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85bd0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85bd0-115">Return value</span></span>

<span data-ttu-id="85bd0-116">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="85bd0-116">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="85bd0-117">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="85bd0-117">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="85bd0-118">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="85bd0-118">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="85bd0-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="85bd0-119">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="85bd0-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="85bd0-120">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85bd0-121"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="85bd0-121"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="85bd0-122">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="85bd0-122">One of the provided handles is not valid.</span></span><br/>                      |
| <dl> <span data-ttu-id="85bd0-123"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="85bd0-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="85bd0-124">O parâmetro *phSslProvider* ou *ppProviderList* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="85bd0-124">The *phSslProvider* or *ppProviderList* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="85bd0-125"><dt>**Status \_ do SEM \_**</dt> <dt>0xC0000017L</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="85bd0-125"><dt>**STATUS\_NO\_MEMORY**</dt> <dt>0xC0000017L</dt></span></span> </dl>      | <span data-ttu-id="85bd0-126">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="85bd0-126">Not enough memory is available to allocate necessary buffers.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="85bd0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85bd0-127">Requirements</span></span>



| <span data-ttu-id="85bd0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="85bd0-128">Requirement</span></span> | <span data-ttu-id="85bd0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="85bd0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="85bd0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85bd0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="85bd0-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85bd0-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="85bd0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85bd0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="85bd0-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85bd0-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85bd0-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85bd0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="85bd0-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="85bd0-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="85bd0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="85bd0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85bd0-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85bd0-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

