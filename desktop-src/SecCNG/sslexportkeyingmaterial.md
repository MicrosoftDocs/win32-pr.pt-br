---
description: Exporta o material de chave de acordo com o padrão RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Função SslExportKeyingMaterial (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663357"
---
# <a name="sslexportkeyingmaterial-function"></a><span data-ttu-id="19eed-103">Função SslExportKeyingMaterial</span><span class="sxs-lookup"><span data-stu-id="19eed-103">SslExportKeyingMaterial function</span></span>

<span data-ttu-id="19eed-104">Exporta o material de chave de acordo com o [padrão RFC 5705](https://tools.ietf.org/html/rfc5705).</span><span class="sxs-lookup"><span data-stu-id="19eed-104">Exports keying material per the [RFC 5705 standard](https://tools.ietf.org/html/rfc5705).</span></span> <span data-ttu-id="19eed-105">Essa função usa a função TLS pseudoaleatória para produzir um buffer de bytes de material de chave.</span><span class="sxs-lookup"><span data-stu-id="19eed-105">This function uses the TLS pseudorandom function to produce a byte buffer of keying material.</span></span> <span data-ttu-id="19eed-106">Ele usa uma referência para o segredo mestre, o rótulo ASCII de desambiguação, valores aleatórios de cliente e servidor e, opcionalmente, os dados de contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="19eed-106">It takes a reference to the master secret, the disambiguating ASCII label, client and server random values, and optionally the application context data.</span></span>

## <a name="syntax"></a><span data-ttu-id="19eed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19eed-107">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="19eed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19eed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19eed-109">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19eed-109">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-110">O identificador da instância do provedor de protocolo TLS.</span><span class="sxs-lookup"><span data-stu-id="19eed-110">The handle of the TLS protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-111">*hMasterKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19eed-111">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-112">O identificador do objeto de chave mestra que será usado para criar o material de chaveamento para br exportado.</span><span class="sxs-lookup"><span data-stu-id="19eed-112">The handle of the master key object that will be used to create the keying material to br exported.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-113">*sLabel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19eed-113">*sLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-114">uma cadeia de caracteres de rótulo ASCII terminada por NUL.</span><span class="sxs-lookup"><span data-stu-id="19eed-114">a NUL-terminated ASCII label string.</span></span> <span data-ttu-id="19eed-115">O Schannel removerá o caractere de terminação do NUL antes de passá-lo para a função pseudoaleatória.</span><span class="sxs-lookup"><span data-stu-id="19eed-115">Schannel will remove the terminating NUL character before passing it to the pseudorandom function.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-116">*pbRandoms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19eed-116">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-117">Um ponteiro para um buffer que contém uma concatenação do *cliente \_ aleatório* e os *valores \_ aleatórios do servidor* da conexão TLS.</span><span class="sxs-lookup"><span data-stu-id="19eed-117">A pointer to a buffer that contains a concatenation of the *client\_random* and *server\_random* values of the TLS connection.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-118">*cbRandoms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19eed-118">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-119">O comprimento, em bytes, do buffer *pbRandoms* .</span><span class="sxs-lookup"><span data-stu-id="19eed-119">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-120">*pbContextValue* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="19eed-120">*pbContextValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-121">Um ponteiro para um buffer que contém o contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="19eed-121">A pointer to a buffer that contains the application context.</span></span> <span data-ttu-id="19eed-122">Se *pbContextValue* for **nulo**, *cbContextValue* deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="19eed-122">If *pbContextValue* is **NULL**, *cbContextValue* must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-123">*cbContextValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19eed-123">*cbContextValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-124">O comprimento, em bytes, do buffer *pbContextValue* .</span><span class="sxs-lookup"><span data-stu-id="19eed-124">The length, in bytes, of the *pbContextValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-125">*pbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="19eed-125">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-126">O endereço de um buffer que recebe o material de chave exportado.</span><span class="sxs-lookup"><span data-stu-id="19eed-126">The address of a buffer that receives the exported keying material.</span></span> <span data-ttu-id="19eed-127">O parâmetro *cbOutput* contém o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="19eed-127">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="19eed-128">Esse valor não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="19eed-128">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-129">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19eed-129">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-130">O comprimento, em bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="19eed-130">The length, in bytes, of the *pbOutput* buffer.</span></span> <span data-ttu-id="19eed-131">Deve ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="19eed-131">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="19eed-132">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19eed-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19eed-133">Não usado.</span><span class="sxs-lookup"><span data-stu-id="19eed-133">Not used.</span></span> <span data-ttu-id="19eed-134">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="19eed-134">Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19eed-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19eed-135">Return value</span></span>

<span data-ttu-id="19eed-136">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="19eed-136">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="19eed-137">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="19eed-137">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="19eed-138">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="19eed-138">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="19eed-139">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="19eed-139">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="19eed-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="19eed-140">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="19eed-141"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="19eed-141"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="19eed-142">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="19eed-142">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19eed-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19eed-143">Requirements</span></span>



| <span data-ttu-id="19eed-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="19eed-144">Requirement</span></span> | <span data-ttu-id="19eed-145">Valor</span><span class="sxs-lookup"><span data-stu-id="19eed-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19eed-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19eed-146">Minimum supported client</span></span><br/> | <span data-ttu-id="19eed-147">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="19eed-147">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="19eed-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19eed-148">Minimum supported server</span></span><br/> | <span data-ttu-id="19eed-149">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="19eed-149">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19eed-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19eed-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="19eed-151"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="19eed-151"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="19eed-152">DLL</span><span class="sxs-lookup"><span data-stu-id="19eed-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19eed-153"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19eed-153"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




