---
description: Descriptografa uma mensagem usando o Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Função DecryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090759"
---
# <a name="decryptmessage-kerberos-function"></a><span data-ttu-id="bfc50-103">Função DecryptMessage (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="bfc50-103">DecryptMessage (Kerberos) function</span></span>

<span data-ttu-id="bfc50-104">A função **DecryptMessage (Kerberos)** descriptografa uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bfc50-104">The **DecryptMessage (Kerberos)** function decrypts a message.</span></span> <span data-ttu-id="bfc50-105">Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.</span><span class="sxs-lookup"><span data-stu-id="bfc50-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="bfc50-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) e **DecryptMessage (Kerberos)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando.</span><span class="sxs-lookup"><span data-stu-id="bfc50-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) and **DecryptMessage (Kerberos)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="bfc50-107">Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="bfc50-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc50-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfc50-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="bfc50-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfc50-109">Parameters</span></span>

<span data-ttu-id="bfc50-110">*phContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bfc50-110">*phContext* \[in\]</span></span>

<span data-ttu-id="bfc50-111">Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para descriptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bfc50-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="bfc50-112">*PMessage* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bfc50-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="bfc50-113">Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="bfc50-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="bfc50-114">Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo \_ dados SecBuffer.</span><span class="sxs-lookup"><span data-stu-id="bfc50-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that may be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="bfc50-115">O buffer contém a mensagem criptografada.</span><span class="sxs-lookup"><span data-stu-id="bfc50-115">The buffer contains the encrypted message.</span></span> <span data-ttu-id="bfc50-116">A mensagem criptografada é descriptografada no local, substituindo o conteúdo original de seu buffer.</span><span class="sxs-lookup"><span data-stu-id="bfc50-116">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="bfc50-117">*MessageSeqNo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bfc50-117">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="bfc50-118">O número de sequência esperado pelo aplicativo de transporte, se houver.</span><span class="sxs-lookup"><span data-stu-id="bfc50-118">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="bfc50-119">Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="bfc50-119">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="bfc50-120">*pfQOP* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bfc50-120">*pfQOP* \[out\]</span></span>

<span data-ttu-id="bfc50-121">Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.</span><span class="sxs-lookup"><span data-stu-id="bfc50-121">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="bfc50-122">Esse parâmetro pode ser o sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfc50-122">This parameter can be the following flag.</span></span>

| <span data-ttu-id="bfc50-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bfc50-123">Value</span></span>                  | <span data-ttu-id="bfc50-124">Significado</span><span class="sxs-lookup"><span data-stu-id="bfc50-124">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="bfc50-125">SECQOP_WRAP_NO_ENCRYPT</span><span class="sxs-lookup"><span data-stu-id="bfc50-125">SECQOP_WRAP_NO_ENCRYPT</span></span> | <span data-ttu-id="bfc50-126">Ela não foi criptografada, mas um cabeçalho ou trailer foi produzido.</span><span class="sxs-lookup"><span data-stu-id="bfc50-126">he message was not encrypted, but a header or trailer was produced.</span></span> |

> [!NOTE]
> <span data-ttu-id="bfc50-127">KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</span><span class="sxs-lookup"><span data-stu-id="bfc50-127">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span>

## <a name="return-value"></a><span data-ttu-id="bfc50-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bfc50-128">Return value</span></span>

<span data-ttu-id="bfc50-129">Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bfc50-129">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="bfc50-130">Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="bfc50-130">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="bfc50-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bfc50-131">Return code</span></span>                     | <span data-ttu-id="bfc50-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfc50-132">Description</span></span>                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc50-133">**s \_ E \_ mensagem incompleta \_**</span><span class="sxs-lookup"><span data-stu-id="bfc50-133">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="bfc50-134">Os dados no buffer de entrada estão incompletos.</span><span class="sxs-lookup"><span data-stu-id="bfc50-134">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="bfc50-135">O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) novamente.</span><span class="sxs-lookup"><span data-stu-id="bfc50-135">The application needs to read more data from the server and call [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) again.</span></span> |
| <span data-ttu-id="bfc50-136">**s \_ E \_ fora \_ de \_ sequência**</span><span class="sxs-lookup"><span data-stu-id="bfc50-136">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="bfc50-137">A mensagem não foi recebida na sequência correta.</span><span class="sxs-lookup"><span data-stu-id="bfc50-137">The message was not received in the correct sequence.</span></span>                                                                                                                            |

## <a name="remarks"></a><span data-ttu-id="bfc50-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfc50-138">Remarks</span></span>

<span data-ttu-id="bfc50-139">Às vezes, um aplicativo lerá os dados da parte remota, tentará descriptografá-los usando **DecryptMessage (Kerberos)** e descobrirá que o **DecryptMessage (Kerberos)** foi bem-sucedido, mas os buffers de saída estão vazios.</span><span class="sxs-lookup"><span data-stu-id="bfc50-139">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Kerberos)**, and discover that **DecryptMessage (Kerberos)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="bfc50-140">Esse comportamento é normal e os aplicativos devem ser capazes de lidar com eles.</span><span class="sxs-lookup"><span data-stu-id="bfc50-140">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="bfc50-141">Para obter informações sobre a interoperação com o GSSAPI, consulte [interoperabilidade entre SSPI/Kerberos com GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span><span class="sxs-lookup"><span data-stu-id="bfc50-141">For information about interoperating with GSSAPI, see [SSPI/Kerberos Interoperability with GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span></span>

<span data-ttu-id="bfc50-142">**Windows XP:** Essa função também era conhecida como **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="bfc50-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="bfc50-143">Os aplicativos agora devem usar somente **DecryptMessage (Kerberos)** .</span><span class="sxs-lookup"><span data-stu-id="bfc50-143">Applications should now use **DecryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfc50-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfc50-144">Requirements</span></span>

| <span data-ttu-id="bfc50-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfc50-145">Requirement</span></span> | <span data-ttu-id="bfc50-146">Valor</span><span class="sxs-lookup"><span data-stu-id="bfc50-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bfc50-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfc50-147">Minimum supported client</span></span> | <span data-ttu-id="bfc50-148">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bfc50-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="bfc50-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfc50-149">Minimum supported server</span></span> | <span data-ttu-id="bfc50-150">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bfc50-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="bfc50-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bfc50-151">Header</span></span>                   | <span data-ttu-id="bfc50-152">SSPI. h (incluir Security. h)</span><span class="sxs-lookup"><span data-stu-id="bfc50-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="bfc50-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfc50-153">Library</span></span>                  | <span data-ttu-id="bfc50-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="bfc50-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="bfc50-155">DLL</span><span class="sxs-lookup"><span data-stu-id="bfc50-155">DLL</span></span>                      | <span data-ttu-id="bfc50-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="bfc50-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="bfc50-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfc50-157">See also</span></span>

- [<span data-ttu-id="bfc50-158">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="bfc50-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="bfc50-159">**EncryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="bfc50-159">**EncryptMessage (Kerberos)**</span></span>](encryptmessage--kerberos.md)
- [<span data-ttu-id="bfc50-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="bfc50-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="bfc50-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="bfc50-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
