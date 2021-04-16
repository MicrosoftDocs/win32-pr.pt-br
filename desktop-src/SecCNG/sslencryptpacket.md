---
description: Criptografa um pacote de protocolo SSL (Single protocolo SSL Protocol).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Função SslEncryptPacket (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750501"
---
# <a name="sslencryptpacket-function"></a><span data-ttu-id="3145d-103">Função SslEncryptPacket</span><span class="sxs-lookup"><span data-stu-id="3145d-103">SslEncryptPacket function</span></span>

<span data-ttu-id="3145d-104">A função **SslEncryptPacket** criptografa um único pacote de protocolo SSL (Single [*protocolo SSL Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="3145d-104">The **SslEncryptPacket** function encrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="3145d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3145d-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3145d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3145d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3145d-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3145d-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-108">O identificador da instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="3145d-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3145d-109">*HKEY* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3145d-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-110">O identificador para a chave que é usada para criptografar o pacote.</span><span class="sxs-lookup"><span data-stu-id="3145d-110">The handle to the key that is used to encrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="3145d-111">*pbInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3145d-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-112">Um ponteiro para o buffer que contém o pacote a ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="3145d-112">A pointer to the buffer that contains the packet to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="3145d-113">*cbInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3145d-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-114">O comprimento, em bytes, do buffer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="3145d-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3145d-115">*pbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3145d-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-116">Um ponteiro para um buffer para receber o pacote criptografado.</span><span class="sxs-lookup"><span data-stu-id="3145d-116">A pointer to a buffer to receive the encrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="3145d-117">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3145d-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-118">O comprimento, bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3145d-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3145d-119">*pcbResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3145d-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-120">O número de bytes gravados no buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3145d-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3145d-121">*SequenceNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3145d-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-122">O número de sequência que corresponde a este pacote.</span><span class="sxs-lookup"><span data-stu-id="3145d-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="3145d-123">*dwContentType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3145d-123">*dwContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-124">O tipo de conteúdo que corresponde a esse pacote, que especifica o protocolo de nível superior usado para processar o pacote incluído.</span><span class="sxs-lookup"><span data-stu-id="3145d-124">The content type that corresponds to this packet, which specifies the higher level protocol used to process the enclosed packet.</span></span>



| <span data-ttu-id="3145d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3145d-125">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="3145d-126">Significado</span><span class="sxs-lookup"><span data-stu-id="3145d-126">Meaning</span></span>                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <span data-ttu-id="3145d-127"><dt>**CT \_ ALTERAR \_ \_ especificação de codificação**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="3145d-127"><dt>**CT\_CHANGE\_CIPHER\_SPEC**</dt> <dt>20</dt></span></span> </dl> | <span data-ttu-id="3145d-128">Indica uma alteração na estratégia de codificação.</span><span class="sxs-lookup"><span data-stu-id="3145d-128">Indicates a change in the ciphering strategy.</span></span><br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <span data-ttu-id="3145d-129"><dt>**CT \_ ALERTA**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="3145d-129"><dt>**CT\_ALERT**</dt> <dt>21</dt></span></span> </dl>                                          | <span data-ttu-id="3145d-130">Indica que o pacote incluído contém um alerta.</span><span class="sxs-lookup"><span data-stu-id="3145d-130">Indicates that the enclosed packet contains an alert.</span></span><br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <span data-ttu-id="3145d-131"><dt>**CT \_ HANDSHAKE**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="3145d-131"><dt>**CT\_HANDSHAKE**</dt> <dt>22</dt></span></span> </dl>                              | <span data-ttu-id="3145d-132">Indica que o pacote incluído faz parte do protocolo de handshake.</span><span class="sxs-lookup"><span data-stu-id="3145d-132">Indicates that the enclosed packet is part of the handshake protocol.</span></span><br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <span data-ttu-id="3145d-133"><dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="3145d-133"><dt>**CT\_APPLICATIONDATA**</dt> <dt>23</dt></span></span> </dl>            | <span data-ttu-id="3145d-134">Indica que o pacote contém dados de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3145d-134">Indicates that the packet contains application data.</span></span><br/>                  |



 

</dd> <dt>

<span data-ttu-id="3145d-135">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3145d-135">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3145d-136">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3145d-136">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3145d-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3145d-137">Return value</span></span>

<span data-ttu-id="3145d-138">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="3145d-138">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3145d-139">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3145d-139">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="3145d-140">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3145d-140">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3145d-141">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3145d-141">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="3145d-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="3145d-142">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3145d-143"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="3145d-143"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="3145d-144">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="3145d-144">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3145d-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3145d-145">Requirements</span></span>



| <span data-ttu-id="3145d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3145d-146">Requirement</span></span> | <span data-ttu-id="3145d-147">Valor</span><span class="sxs-lookup"><span data-stu-id="3145d-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3145d-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3145d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3145d-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3145d-149">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3145d-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3145d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3145d-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3145d-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3145d-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3145d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="3145d-153"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="3145d-153"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3145d-154">DLL</span><span class="sxs-lookup"><span data-stu-id="3145d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3145d-155"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3145d-155"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

