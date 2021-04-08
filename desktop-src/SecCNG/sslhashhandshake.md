---
description: Retorna um identificador para o hash de handshake.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Função SslHashHandshake (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922450"
---
# <a name="sslhashhandshake-function"></a><span data-ttu-id="efde9-103">Função SslHashHandshake</span><span class="sxs-lookup"><span data-stu-id="efde9-103">SslHashHandshake function</span></span>

<span data-ttu-id="efde9-104">A função **SslHashHandshake** retorna um identificador para o hash de handshake.</span><span class="sxs-lookup"><span data-stu-id="efde9-104">The **SslHashHandshake** function returns a handle to the handshake hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="efde9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efde9-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="efde9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efde9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efde9-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efde9-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde9-108">O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="efde9-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="efde9-109">*hHandshakeHash* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="efde9-109">*hHandshakeHash* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="efde9-110">O identificador para o objeto de hash.</span><span class="sxs-lookup"><span data-stu-id="efde9-110">The handle to the hash object.</span></span>

</dd> <dt>

<span data-ttu-id="efde9-111">*pbInput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="efde9-111">*pbInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efde9-112">O endereço de um buffer que contém os dados a serem armazenados em hash.</span><span class="sxs-lookup"><span data-stu-id="efde9-112">The address of a buffer that contains the data to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="efde9-113">*cbInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efde9-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde9-114">O tamanho, em bytes, do buffer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="efde9-114">The size, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="efde9-115">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efde9-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde9-116">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="efde9-116">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efde9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efde9-117">Return value</span></span>

<span data-ttu-id="efde9-118">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="efde9-118">If the function succeeds, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="efde9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="efde9-119">Remarks</span></span>

<span data-ttu-id="efde9-120">A função **SslHashHandshake** é uma das três funções usadas para gerar um hash a ser usado durante o HANDSHAKE de SSL.</span><span class="sxs-lookup"><span data-stu-id="efde9-120">The **SslHashHandshake** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="efde9-121">A função [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) é chamada para obter um identificador de hash.</span><span class="sxs-lookup"><span data-stu-id="efde9-121">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="efde9-122">A função **SslHashHandshake** é chamada qualquer número de vezes com o identificador de hash para adicionar dados ao hash.</span><span class="sxs-lookup"><span data-stu-id="efde9-122">The **SslHashHandshake** function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="efde9-123">A função [**SslComputeFinishedHash**](sslcomputefinishedhash.md) é chamada com o identificador de hash para obter o resumo dos dados com hash.</span><span class="sxs-lookup"><span data-stu-id="efde9-123">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="efde9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efde9-124">Requirements</span></span>



| <span data-ttu-id="efde9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="efde9-125">Requirement</span></span> | <span data-ttu-id="efde9-126">Valor</span><span class="sxs-lookup"><span data-stu-id="efde9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="efde9-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efde9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="efde9-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efde9-128">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="efde9-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efde9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="efde9-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efde9-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="efde9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="efde9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="efde9-132"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="efde9-132"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="efde9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="efde9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efde9-134"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efde9-134"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

