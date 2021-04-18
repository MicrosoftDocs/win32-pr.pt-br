---
description: Computa o bloco de chave usado pelo protocolo EAP (Extensible Authentication Protocol).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Função SslComputeEapKeyBlock (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756866"
---
# <a name="sslcomputeeapkeyblock-function"></a><span data-ttu-id="b7094-103">Função SslComputeEapKeyBlock</span><span class="sxs-lookup"><span data-stu-id="b7094-103">SslComputeEapKeyBlock function</span></span>

<span data-ttu-id="b7094-104">A função **SslComputeEapKeyBlock** computa o bloco de chave usado pelo EAP (Extensible Authentication Protocol).</span><span class="sxs-lookup"><span data-stu-id="b7094-104">The **SslComputeEapKeyBlock** function computes the key block used by the Extensible Authentication Protocol (EAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7094-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7094-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b7094-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7094-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7094-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7094-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7094-108">O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="b7094-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="b7094-109">*hMasterKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7094-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7094-110">O identificador do objeto de [*chave mestra*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="b7094-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="b7094-111">*pbRandoms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7094-111">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7094-112">Um ponteiro para um buffer que contém uma concatenação do cliente \_ aleatório e os \_ valores aleatórios do servidor da sessão SSL.</span><span class="sxs-lookup"><span data-stu-id="b7094-112">A pointer to a buffer that contains a concatenation of the client\_random and server\_random values of the SSL session.</span></span>

</dd> <dt>

<span data-ttu-id="b7094-113">*cbRandoms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7094-113">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7094-114">O comprimento, em bytes, do buffer *pbRandoms* .</span><span class="sxs-lookup"><span data-stu-id="b7094-114">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b7094-115">*pbOutput* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7094-115">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7094-116">O endereço de um buffer que recebe o BLOB de chave.</span><span class="sxs-lookup"><span data-stu-id="b7094-116">The address of a buffer that receives the key BLOB.</span></span> <span data-ttu-id="b7094-117">O parâmetro *cbOutput* contém o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="b7094-117">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="b7094-118">Se esse parâmetro for **NULL**, essa função coloca o tamanho necessário, em bytes, no **DWORD** apontado pelo parâmetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="b7094-118">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b7094-119">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7094-119">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7094-120">O comprimento, em bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="b7094-120">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b7094-121">*pcbResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b7094-121">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7094-122">Um ponteiro para um valor **DWORD** que especifica o comprimento, em bytes, do hash gravado no buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="b7094-122">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b7094-123">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7094-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7094-124">Defina como **\_ sinalizador de \_ servidor \_ de SSL NCRYPT** para indicar que esta é uma chamada de servidor.</span><span class="sxs-lookup"><span data-stu-id="b7094-124">Set to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7094-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7094-125">Return value</span></span>

<span data-ttu-id="b7094-126">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b7094-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="b7094-127">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b7094-127">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="b7094-128">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b7094-128">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="b7094-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7094-129">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="b7094-130"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="b7094-130"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="b7094-131">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="b7094-131">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b7094-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7094-132">Requirements</span></span>



| <span data-ttu-id="b7094-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7094-133">Requirement</span></span> | <span data-ttu-id="b7094-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b7094-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7094-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7094-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b7094-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7094-136">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7094-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7094-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b7094-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7094-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b7094-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7094-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7094-140"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7094-140"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="b7094-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b7094-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7094-142"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7094-142"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

