---
description: Descriptografa um único pacote de protocolo SSL (Single protocolo SSL Protocol).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Função SslDecryptPacket (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921410"
---
# <a name="ssldecryptpacket-function"></a><span data-ttu-id="3e3f2-103">Função SslDecryptPacket</span><span class="sxs-lookup"><span data-stu-id="3e3f2-103">SslDecryptPacket function</span></span>

<span data-ttu-id="3e3f2-104">a função **SslDecryptPacket** descriptografa um único pacote de protocolo SSL (Single [*protocolo SSL Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="3e3f2-104">the **SslDecryptPacket** function decrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e3f2-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3e3f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e3f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e3f2-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-108">O identificador da instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f2-109">*HKEY* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-110">O identificador para a chave que é usada para descriptografar o pacote.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-110">The handle to the key that is used to decrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f2-111">*pbInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-112">Um ponteiro para o buffer que contém o pacote a ser descriptografado.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-112">A pointer to the buffer that contains the packet to be decrypted.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f2-113">*cbInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-114">O comprimento, em bytes, do buffer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="3e3f2-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f2-115">*pbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-116">Um ponteiro para um buffer que contém o pacote descriptografado.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-116">A pointer to a buffer to contain the decrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f2-117">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-118">O comprimento, bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3e3f2-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f2-119">*pcbResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-120">O número de bytes gravados no buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3e3f2-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f2-121">*SequenceNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-122">O número de sequência que corresponde a este pacote.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f2-123">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f2-124">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-124">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e3f2-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e3f2-125">Return value</span></span>

<span data-ttu-id="3e3f2-126">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3e3f2-127">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-127">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="3e3f2-128">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-128">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3e3f2-129">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3e3f2-129">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="3e3f2-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e3f2-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3e3f2-131"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="3e3f2-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="3e3f2-132">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-132">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e3f2-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e3f2-133">Remarks</span></span>

<span data-ttu-id="3e3f2-134">O comprimento do pacote pode ser zero, como quando uma mensagem "HelloRequest" é descriptografada.</span><span class="sxs-lookup"><span data-stu-id="3e3f2-134">The length of the packet can be zero, such as when a "HelloRequest" message is decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e3f2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e3f2-135">Requirements</span></span>



| <span data-ttu-id="3e3f2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e3f2-136">Requirement</span></span> | <span data-ttu-id="3e3f2-137">Valor</span><span class="sxs-lookup"><span data-stu-id="3e3f2-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e3f2-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e3f2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3e3f2-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e3f2-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e3f2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3e3f2-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e3f2-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e3f2-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e3f2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e3f2-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e3f2-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3e3f2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3e3f2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e3f2-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e3f2-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

