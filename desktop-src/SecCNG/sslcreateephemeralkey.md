---
description: Cria uma chave efêmera para uso durante a autenticação que ocorre durante o handshake do protocolo de protocolo SSL (SSL).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Função SslCreateEphemeralKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747647"
---
# <a name="sslcreateephemeralkey-function"></a><span data-ttu-id="ac80d-103">Função SslCreateEphemeralKey</span><span class="sxs-lookup"><span data-stu-id="ac80d-103">SslCreateEphemeralKey function</span></span>

<span data-ttu-id="ac80d-104">A função **SslCreateEphemeralKey** cria uma chave efêmera para uso durante a autenticação que ocorre durante o handshake do [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="ac80d-104">The **SslCreateEphemeralKey** function creates an ephemeral key for use during the authentication that occurs during the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac80d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac80d-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ac80d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac80d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac80d-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-108">O identificador da instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="ac80d-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ac80d-109">*phEphemeralKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-109">*phEphemeralKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-110">O identificador da chave efêmera.</span><span class="sxs-lookup"><span data-stu-id="ac80d-110">The handle of the ephemeral key.</span></span>

</dd> <dt>

<span data-ttu-id="ac80d-111">*dwProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-112">Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="ac80d-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="ac80d-113">*dwCipherSuite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-114">Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="ac80d-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="ac80d-115">*dwKeyType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-115">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-116">Um dos valores do [**identificador do tipo de chave do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="ac80d-116">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="ac80d-117">Defina esse parâmetro como zero para os tipos de chave que não são ECC ( [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) ).</span><span class="sxs-lookup"><span data-stu-id="ac80d-117">Set this parameter to zero for key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="ac80d-118">*dwKeyBitLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-118">*dwKeyBitLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-119">O comprimento, em bits, da chave.</span><span class="sxs-lookup"><span data-stu-id="ac80d-119">The length, in bits, of the key.</span></span>

</dd> <dt>

<span data-ttu-id="ac80d-120">*pbParams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-120">*pbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-121">Um ponteiro para um buffer que contém parâmetros para a chave a ser criada.</span><span class="sxs-lookup"><span data-stu-id="ac80d-121">A pointer to a buffer to contain parameters for the key that is to be created.</span></span> <span data-ttu-id="ac80d-122">Se um conjunto de codificação de DHE [*(algoritmo de troca de chaves) Diffie-Hellman (efêmero)*](/windows/desktop/SecGloss/d-gly) não for usado, defina o parâmetro *pbParams* como **nulo** e o parâmetro *cbParams* como zero.</span><span class="sxs-lookup"><span data-stu-id="ac80d-122">If a [*Diffie-Hellman (ephemeral) key-exchange algorithm*](/windows/desktop/SecGloss/d-gly) (DHE) cipher suite is not used, set the *pbParams* parameter to **NULL** and the *cbParams* parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ac80d-123">*cbParams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-123">*cbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-124">O comprimento, em bytes, dos dados no buffer *pbParams* .</span><span class="sxs-lookup"><span data-stu-id="ac80d-124">The length, in bytes, of the data in the *pbParams* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ac80d-125">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80d-126">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ac80d-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac80d-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac80d-127">Return value</span></span>

<span data-ttu-id="ac80d-128">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ac80d-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ac80d-129">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ac80d-129">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="ac80d-130">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ac80d-130">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="ac80d-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac80d-131">Description</span></span>                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ac80d-132"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="ac80d-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="ac80d-133">Memória insuficiente para alocar o buffer.</span><span class="sxs-lookup"><span data-stu-id="ac80d-133">There is insufficient memory to allocate the buffer.</span></span><br/> |
| <dl> <span data-ttu-id="ac80d-134"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="ac80d-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="ac80d-135">O identificador *hSslProvider* não é válido.</span><span class="sxs-lookup"><span data-stu-id="ac80d-135">The *hSslProvider* handle is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="ac80d-136"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="ac80d-136"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="ac80d-137">Um dos parâmetros fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="ac80d-137">One of the supplied parameters is not valid.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="ac80d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac80d-138">Remarks</span></span>

<span data-ttu-id="ac80d-139">Ao usar um DHE Cipher Suite, a implementação SSL interna passa os parâmetros *p* e *g* do servidor para a função **SslCreateEphemeralKey** nos parâmetros *pbParams* e *cbParams* .</span><span class="sxs-lookup"><span data-stu-id="ac80d-139">When using a DHE cipher suite, the internal SSL implementation passes server *p* and *g* parameters to the **SslCreateEphemeralKey** function in the *pbParams* and *cbParams* parameters.</span></span>

<span data-ttu-id="ac80d-140">O formato dos dados no buffer *pbParams* é o mesmo usado ao definir a propriedade de parâmetros de [**\_ DH BCrypt \_**](cng-property-identifiers.md) e começa com uma estrutura de cabeçalho de [**\_ parâmetro BCrypt \_ DH \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="ac80d-140">The format of the data in the *pbParams* buffer is the same as that used when setting the [**BCRYPT\_DH\_PARAMETERS**](cng-property-identifiers.md) property, and it starts with a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac80d-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac80d-141">Requirements</span></span>



| <span data-ttu-id="ac80d-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac80d-142">Requirement</span></span> | <span data-ttu-id="ac80d-143">Valor</span><span class="sxs-lookup"><span data-stu-id="ac80d-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac80d-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac80d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ac80d-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-145">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ac80d-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac80d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ac80d-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac80d-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ac80d-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac80d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac80d-149"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac80d-149"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ac80d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ac80d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac80d-151"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac80d-151"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

