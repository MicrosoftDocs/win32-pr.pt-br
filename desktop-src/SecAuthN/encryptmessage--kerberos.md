---
description: Criptografa uma mensagem para fornecer privacidade usando o Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Função EncryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171272"
---
# <a name="encryptmessage-kerberos-function"></a><span data-ttu-id="48308-103">Função EncryptMessage (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="48308-103">EncryptMessage (Kerberos) function</span></span>

<span data-ttu-id="48308-104">A função **EncryptMessage (Kerberos)** criptografa uma mensagem para fornecer [*privacidade*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="48308-104">The **EncryptMessage (Kerberos)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="48308-105">**EncryptMessage (Kerberos)** permite que um aplicativo escolha entre [*algoritmos de criptografia*](../secgloss/c-gly.md) com suporte no mecanismo escolhido.</span><span class="sxs-lookup"><span data-stu-id="48308-105">**EncryptMessage (Kerberos)** allows an application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="48308-106">A função **EncryptMessage (Kerberos)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="48308-106">The **EncryptMessage (Kerberos)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="48308-107">Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um [*hash*](../secgloss/h-gly.md) de integridade que pode ser verificado.</span><span class="sxs-lookup"><span data-stu-id="48308-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

> [!Note]  
> <span data-ttu-id="48308-108">**EncryptMessage (Kerberos)** e [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando.</span><span class="sxs-lookup"><span data-stu-id="48308-108">**EncryptMessage (Kerberos)** and [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="48308-109">Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="48308-109">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="48308-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48308-110">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a><span data-ttu-id="48308-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48308-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48308-112">*phContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48308-112">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48308-113">Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para criptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="48308-113">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="48308-114">*fQOP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48308-114">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48308-115">Sinalizadores específicos do pacote que indicam a qualidade da proteção.</span><span class="sxs-lookup"><span data-stu-id="48308-115">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="48308-116">Um [*pacote de segurança*](../secgloss/s-gly.md) pode usar esse parâmetro para habilitar a seleção de [*algoritmos criptográficos*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="48308-116">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="48308-117">Esse parâmetro pode ser o sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="48308-117">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="48308-118">Valor</span><span class="sxs-lookup"><span data-stu-id="48308-118">Value</span></span></th><th><span data-ttu-id="48308-119">Significado</span><span class="sxs-lookup"><span data-stu-id="48308-119">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="48308-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="48308-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="48308-121">Produz um cabeçalho ou um trailer, mas não criptografa a mensagem.</span><span class="sxs-lookup"><span data-stu-id="48308-121">Produce a header or trailer but do not encrypt the message.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="48308-122">KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</span><span class="sxs-lookup"><span data-stu-id="48308-122">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

</dd> <dt>

<span data-ttu-id="48308-123">*PMessage* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="48308-123">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48308-124">Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="48308-124">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="48308-125">Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo \_ dados SecBuffer.</span><span class="sxs-lookup"><span data-stu-id="48308-125">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="48308-126">Esse buffer contém a mensagem a ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="48308-126">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="48308-127">A mensagem é criptografada no local, substituindo o conteúdo original da estrutura.</span><span class="sxs-lookup"><span data-stu-id="48308-127">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="48308-128">A função não processa buffers com o \_ atributo ReadOnly SECBUFFER.</span><span class="sxs-lookup"><span data-stu-id="48308-128">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="48308-129">O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Kerberos**](querycontextattributes--kerberos.md) \_ attr tamanhos de fluxo SECPKG \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="48308-129">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="48308-130">Os aplicativos que não usam SSL devem fornecer um [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo \_ preenchimento SecBuffer.</span><span class="sxs-lookup"><span data-stu-id="48308-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="48308-131">*MessageSeqNo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48308-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48308-132">O número de sequência que o aplicativo de transporte atribuiu à mensagem.</span><span class="sxs-lookup"><span data-stu-id="48308-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="48308-133">Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="48308-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48308-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48308-134">Return value</span></span>

<span data-ttu-id="48308-135">Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48308-135">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="48308-136">Se a função falhar, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="48308-136">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="48308-137">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="48308-137">Return code</span></span>                                                                                                    | <span data-ttu-id="48308-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="48308-138">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48308-139"><dt>**s \_ E \_ buffer \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="48308-139"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="48308-140">O buffer de saída é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="48308-140">The output buffer is too small.</span></span> <span data-ttu-id="48308-141">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="48308-141">For more information, see Remarks.</span></span>                                                                                                                                                                 |
| <dl> <span data-ttu-id="48308-142"><dt>**o \_ contexto s E \_ \_ expirou**</dt></span><span class="sxs-lookup"><span data-stu-id="48308-142"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="48308-143">O aplicativo está fazendo referência a um contexto que já foi fechado.</span><span class="sxs-lookup"><span data-stu-id="48308-143">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="48308-144">Um aplicativo escrito corretamente não deve receber esse erro.</span><span class="sxs-lookup"><span data-stu-id="48308-144">A properly written application should not receive this error.</span></span>                                                                                               |
| <dl> <span data-ttu-id="48308-145"><dt>**s \_ E \_ sistema de criptografia \_ \_ inválidos**</dt></span><span class="sxs-lookup"><span data-stu-id="48308-145"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="48308-146">Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="48308-146">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span>                                                                                                         |
| <dl> <span data-ttu-id="48308-147"><dt>**s \_ E \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48308-147"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="48308-148">Não há memória suficiente disponível para concluir a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="48308-148">There is not enough memory available to complete the requested action.</span></span>                                                                                                                                                             |
| <dl> <span data-ttu-id="48308-149"><dt>**s \_ E \_ \_ identificador inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="48308-149"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="48308-150">Um identificador de contexto inválido foi especificado no parâmetro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="48308-150">A context handle that is not valid was specified in the *phContext* parameter.</span></span>                                                                                                                                                     |
| <dl> <span data-ttu-id="48308-151"><dt>**s \_ E \_ \_ token inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="48308-151"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="48308-152">Nenhum \_ buffer de tipo de dados SECBUFFER foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="48308-152">No SECBUFFER\_DATA type buffer was found.</span></span>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="48308-153"><dt>**s \_ E \_ QOP \_ não \_ têm suporte**</dt></span><span class="sxs-lookup"><span data-stu-id="48308-153"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="48308-154">Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="48308-154">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="48308-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="48308-155">Remarks</span></span>

<span data-ttu-id="48308-156">A função **EncryptMessage (Kerberos)** criptografa uma mensagem com base na mensagem e na [*chave de sessão*](../secgloss/s-gly.md) de um [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="48308-156">The **EncryptMessage (Kerberos)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="48308-157">Se o aplicativo de transporte criou o [*contexto de segurança*](../secgloss/s-gly.md) para dar suporte à detecção de sequência e o chamador fornecer um número de sequência, a função incluirá essas informações com a mensagem criptografada.</span><span class="sxs-lookup"><span data-stu-id="48308-157">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="48308-158">A inclusão dessas informações protege contra reprodução, inserção e supressão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="48308-158">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="48308-159">O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.</span><span class="sxs-lookup"><span data-stu-id="48308-159">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

> [!Note]  
> <span data-ttu-id="48308-160">Esses buffers devem ser fornecidos na ordem mostrada.</span><span class="sxs-lookup"><span data-stu-id="48308-160">These buffers must be supplied in the order shown.</span></span>

| <span data-ttu-id="48308-161">Tipo de buffer</span><span class="sxs-lookup"><span data-stu-id="48308-161">Buffer type</span></span>                           | <span data-ttu-id="48308-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="48308-162">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48308-163">< de cabeçalho de \_ fluxo de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="48308-163">SECBUFFER\_STREAM\_HEADER<</span></span>  | <span data-ttu-id="48308-164">Usado internamente.</span><span class="sxs-lookup"><span data-stu-id="48308-164">Used internally.</span></span> <span data-ttu-id="48308-165">Nenhuma inicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="48308-165">No initialization required.</span></span>                                                                       |
| <span data-ttu-id="48308-166">dados do SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="48308-166">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="48308-167">Contém a mensagem de [*texto sem formatação*](../secgloss/s-gly.md) a ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="48308-167">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span> |
| <span data-ttu-id="48308-168">\_trailer de fluxo de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="48308-168">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="48308-169">Usado internamente.</span><span class="sxs-lookup"><span data-stu-id="48308-169">Used internally.</span></span> <span data-ttu-id="48308-170">Nenhuma inicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="48308-170">No initialization required.</span></span>                                                                        |
| <span data-ttu-id="48308-171">SECBUFFER \_ vazio</span><span class="sxs-lookup"><span data-stu-id="48308-171">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="48308-172">Usado internamente.</span><span class="sxs-lookup"><span data-stu-id="48308-172">Used internally.</span></span> <span data-ttu-id="48308-173">Nenhuma inicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="48308-173">No initialization required.</span></span> <span data-ttu-id="48308-174">O tamanho pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="48308-174">Size can be zero.</span></span>                                                      |

<span data-ttu-id="48308-175">Para um desempenho ideal, as estruturas *PMessage* devem ser alocadas da memória contígua.</span><span class="sxs-lookup"><span data-stu-id="48308-175">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="48308-176">**Windows XP:** Essa função também era conhecida como **SealMessage**.</span><span class="sxs-lookup"><span data-stu-id="48308-176">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="48308-177">Os aplicativos agora devem usar somente **EncryptMessage (Kerberos)** .</span><span class="sxs-lookup"><span data-stu-id="48308-177">Applications should now use **EncryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="48308-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48308-178">Requirements</span></span>

| <span data-ttu-id="48308-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="48308-179">Requirement</span></span> | <span data-ttu-id="48308-180">Valor</span><span class="sxs-lookup"><span data-stu-id="48308-180">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="48308-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48308-181">Minimum supported client</span></span> | <span data-ttu-id="48308-182">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="48308-182">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="48308-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48308-183">Minimum supported server</span></span> | <span data-ttu-id="48308-184">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48308-184">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="48308-185">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48308-185">Header</span></span>                   | <span data-ttu-id="48308-186">SSPI. h (incluir Security. h)</span><span class="sxs-lookup"><span data-stu-id="48308-186">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="48308-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48308-187">Library</span></span>                  | <span data-ttu-id="48308-188">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="48308-188">Secur32.lib</span></span>                               |
| <span data-ttu-id="48308-189">DLL</span><span class="sxs-lookup"><span data-stu-id="48308-189">DLL</span></span>                      | <span data-ttu-id="48308-190">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="48308-190">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="48308-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="48308-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48308-192">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="48308-192">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="48308-193">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="48308-193">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="48308-194">**DecryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="48308-194">**DecryptMessage (Kerberos)**</span></span>](decryptmessage--kerberos.md)
</dt> <dt>

[<span data-ttu-id="48308-195">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="48308-195">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="48308-196">**QueryContextAttributes (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="48308-196">**QueryContextAttributes (Kerberos)**</span></span>](querycontextattributes--kerberos.md)
</dt> <dt>

[<span data-ttu-id="48308-197">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="48308-197">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="48308-198">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="48308-198">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
