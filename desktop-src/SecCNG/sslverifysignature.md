---
description: Verifica a assinatura especificada usando o hash fornecido e a chave pública.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Função SslVerifySignature (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826991"
---
# <a name="sslverifysignature-function"></a><span data-ttu-id="ccd6f-103">Função SslVerifySignature</span><span class="sxs-lookup"><span data-stu-id="ccd6f-103">SslVerifySignature function</span></span>

<span data-ttu-id="ccd6f-104">A função **SslVerifySignature** verifica a assinatura especificada usando o [*hash*](/windows/desktop/SecGloss/h-gly) fornecido e a [*chave pública*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="ccd6f-104">The **SslVerifySignature** function verifies the specified signature by using the supplied [*hash*](/windows/desktop/SecGloss/h-gly) and the [*public key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd6f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccd6f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ccd6f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccd6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd6f-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd6f-108">O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="ccd6f-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ccd6f-109">*hPublicKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-109">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd6f-110">O identificador para a chave pública.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-110">The handle to the public key.</span></span>

</dd> <dt>

<span data-ttu-id="ccd6f-111">*pbHashValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-111">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd6f-112">Um ponteiro para um buffer que contém o hash a ser usado para verificar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-112">A pointer to a buffer that contains the hash to use to verify the signature.</span></span>

</dd> <dt>

<span data-ttu-id="ccd6f-113">*cbHashValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-113">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd6f-114">O tamanho, em bytes, do buffer *pbHashValue* .</span><span class="sxs-lookup"><span data-stu-id="ccd6f-114">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ccd6f-115">*pbSignature* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-115">*pbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd6f-116">Um ponteiro para um buffer que contém a assinatura a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-116">A pointer to a buffer that contains the signature to verify.</span></span>

</dd> <dt>

<span data-ttu-id="ccd6f-117">*cbSignature* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-117">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd6f-118">O tamanho, em bytes, do buffer *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="ccd6f-118">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ccd6f-119">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd6f-120">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd6f-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccd6f-121">Return value</span></span>

<span data-ttu-id="ccd6f-122">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ccd6f-123">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="ccd6f-124">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="ccd6f-125">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ccd6f-125">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="ccd6f-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccd6f-126">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ccd6f-127"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="ccd6f-127"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="ccd6f-128">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-128">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ccd6f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccd6f-129">Remarks</span></span>

<span data-ttu-id="ccd6f-130">A função **SslVerifySignature** não é chamada atualmente pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-130">The **SslVerifySignature** function is not currently called by Windows.</span></span> <span data-ttu-id="ccd6f-131">Essa função é uma parte necessária da interface do provedor SSL e deve ser totalmente implementada para garantir a compatibilidade com o futuro.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-131">This function is a required part of the SSL Provider interface and should be fully implemented to ensure forward compatibility.</span></span>

<span data-ttu-id="ccd6f-132">As implementações atuais do lado do servidor da conexão do [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS chamam a função [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) durante a autenticação do cliente para processar a mensagem de verificação de certificado.</span><span class="sxs-lookup"><span data-stu-id="ccd6f-132">Current implementations of the server side of the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) connection call the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) function during the client authentication to process the certificate verify message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd6f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccd6f-133">Requirements</span></span>



| <span data-ttu-id="ccd6f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd6f-134">Requirement</span></span> | <span data-ttu-id="ccd6f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd6f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd6f-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccd6f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd6f-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ccd6f-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccd6f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd6f-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccd6f-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ccd6f-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccd6f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd6f-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd6f-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ccd6f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ccd6f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccd6f-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccd6f-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

