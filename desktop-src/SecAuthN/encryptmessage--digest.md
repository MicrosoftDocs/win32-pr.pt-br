---
description: Criptografa uma mensagem para fornecer privacidade usando Digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Função EncryptMessage (Digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773921"
---
# <a name="encryptmessage-digest-function"></a><span data-ttu-id="d2140-103">Função EncryptMessage (Digest)</span><span class="sxs-lookup"><span data-stu-id="d2140-103">EncryptMessage (Digest) function</span></span>

<span data-ttu-id="d2140-104">A função **EncryptMessage (Digest)** criptografa uma mensagem para fornecer [*privacidade*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d2140-104">The **EncryptMessage (Digest)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="d2140-105">**EncryptMessage (Digest)** permite que o aplicativo escolha entre [*algoritmos de criptografia*](../secgloss/c-gly.md) com suporte no mecanismo escolhido.</span><span class="sxs-lookup"><span data-stu-id="d2140-105">**EncryptMessage (Digest)** allows the application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="d2140-106">A função **EncryptMessage (Digest)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="d2140-106">The **EncryptMessage (Digest)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="d2140-107">Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um [*hash*](../secgloss/h-gly.md) de integridade que pode ser verificado.</span><span class="sxs-lookup"><span data-stu-id="d2140-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

<span data-ttu-id="d2140-108">Essa função está disponível apenas como um mecanismo SASL.</span><span class="sxs-lookup"><span data-stu-id="d2140-108">This function is available as a SASL mechanism only.</span></span>

> [!Note]  
> <span data-ttu-id="d2140-109">**EncryptMessage (Digest)** e [**DecryptMessage (Digest)**](decryptmessage--digest.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ) se um thread estiver Criptografando e o outro estiver descriptografando.</span><span class="sxs-lookup"><span data-stu-id="d2140-109">**EncryptMessage (Digest)** and [**DecryptMessage (Digest)**](decryptmessage--digest.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="d2140-110">Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d2140-110">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d2140-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2140-111">Syntax</span></span>


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a><span data-ttu-id="d2140-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2140-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2140-113">*phContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2140-113">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2140-114">Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para criptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2140-114">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="d2140-115">*fQOP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2140-115">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2140-116">Sinalizadores específicos do pacote que indicam a qualidade da proteção.</span><span class="sxs-lookup"><span data-stu-id="d2140-116">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="d2140-117">Um [*pacote de segurança*](../secgloss/s-gly.md) pode usar esse parâmetro para habilitar a seleção de [*algoritmos criptográficos*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d2140-117">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="d2140-118">Ao usar o SSP de resumo, esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="d2140-118">When using the Digest SSP, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2140-119">*PMessage* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d2140-119">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2140-120">Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="d2140-120">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="d2140-121">Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo \_ dados SecBuffer.</span><span class="sxs-lookup"><span data-stu-id="d2140-121">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="d2140-122">Esse buffer contém a mensagem a ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="d2140-122">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="d2140-123">A mensagem é criptografada no local, substituindo o conteúdo original da estrutura.</span><span class="sxs-lookup"><span data-stu-id="d2140-123">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="d2140-124">A função não processa buffers com o \_ atributo ReadOnly SECBUFFER.</span><span class="sxs-lookup"><span data-stu-id="d2140-124">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="d2140-125">O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG de \_ fluxo de attr) \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d2140-125">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="d2140-126">Ao usar o SSP de resumo, deve haver um segundo buffer do tipo SECBUFFER \_ Padding ou \_ os dados de buffer de s \_ para manter as informações de [*assinatura*](../secgloss/d-gly.md#_security_digital_signature_gly) .</span><span class="sxs-lookup"><span data-stu-id="d2140-126">When using the Digest SSP, there must be a second buffer of type SECBUFFER\_PADDING or SEC\_BUFFER\_DATA to hold [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) information.</span></span> <span data-ttu-id="d2140-127">Para obter o tamanho do buffer de saída, chame a função [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) e especifique os \_ tamanhos de attr SECPKG \_ .</span><span class="sxs-lookup"><span data-stu-id="d2140-127">To get the size of the output buffer, call the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specify SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="d2140-128">A função retornará uma estrutura [**de \_ tamanhos de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="d2140-128">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="d2140-129">O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="d2140-129">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

<span data-ttu-id="d2140-130">Os aplicativos que não usam SSL devem fornecer um [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo \_ preenchimento SecBuffer.</span><span class="sxs-lookup"><span data-stu-id="d2140-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="d2140-131">*MessageSeqNo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2140-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2140-132">O número de sequência que o aplicativo de transporte atribuiu à mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2140-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="d2140-133">Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="d2140-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

<span data-ttu-id="d2140-134">Ao usar o SSP de resumo, esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="d2140-134">When using the Digest SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="d2140-135">O SSP de resumo gerencia a numeração de sequência internamente.</span><span class="sxs-lookup"><span data-stu-id="d2140-135">The Digest SSP manages sequence numbering internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2140-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2140-136">Return value</span></span>

<span data-ttu-id="d2140-137">Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2140-137">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="d2140-138">Se a função falhar, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="d2140-138">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="d2140-139">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d2140-139">Return code</span></span>                                                                                                    | <span data-ttu-id="d2140-140">Description</span><span class="sxs-lookup"><span data-stu-id="d2140-140">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2140-141"><dt>**s \_ E \_ buffer \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-141"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="d2140-142">O buffer de saída é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="d2140-142">The output buffer is too small.</span></span> <span data-ttu-id="d2140-143">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="d2140-143">For more information, see Remarks.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="d2140-144"><dt>**o \_ contexto s E \_ \_ expirou**</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-144"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="d2140-145">O aplicativo está fazendo referência a um contexto que já foi fechado.</span><span class="sxs-lookup"><span data-stu-id="d2140-145">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="d2140-146">Um aplicativo escrito corretamente não deve receber esse erro.</span><span class="sxs-lookup"><span data-stu-id="d2140-146">A properly written application should not receive this error.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d2140-147"><dt>**s \_ E \_ sistema de criptografia \_ \_ inválidos**</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-147"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="d2140-148">Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d2140-148">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="d2140-149"><dt>**s \_ E \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-149"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="d2140-150">Não há memória suficiente disponível para concluir a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="d2140-150">There is not enough memory available to complete the requested action.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="d2140-151"><dt>**s \_ E \_ \_ identificador inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-151"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="d2140-152">Um identificador de contexto inválido foi especificado no parâmetro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="d2140-152">A context handle that is not valid was specified in the *phContext* parameter.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="d2140-153"><dt>**s \_ E \_ \_ token inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-153"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="d2140-154">Nenhum \_ buffer de tipo de dados SECBUFFER foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="d2140-154">No SECBUFFER\_DATA type buffer was found.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="d2140-155"><dt>**s \_ E \_ QOP \_ não \_ têm suporte**</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-155"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="d2140-156">Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d2140-156">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2140-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2140-157">Remarks</span></span>

<span data-ttu-id="d2140-158">A função **EncryptMessage (Digest)** criptografa uma mensagem com base na mensagem e na [*chave de sessão*](../secgloss/s-gly.md) de um [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d2140-158">The **EncryptMessage (Digest)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="d2140-159">Se o aplicativo de transporte criou o [*contexto de segurança*](../secgloss/s-gly.md) para dar suporte à detecção de sequência e o chamador fornecer um número de sequência, a função incluirá essas informações com a mensagem criptografada.</span><span class="sxs-lookup"><span data-stu-id="d2140-159">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="d2140-160">A inclusão dessas informações protege contra reprodução, inserção e supressão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d2140-160">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="d2140-161">O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.</span><span class="sxs-lookup"><span data-stu-id="d2140-161">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

<span data-ttu-id="d2140-162">Ao usar o SSP de resumo, obtenha o tamanho do buffer de saída chamando a função [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) e especificando os \_ tamanhos de attr SECPKG \_ .</span><span class="sxs-lookup"><span data-stu-id="d2140-162">When you use the Digest SSP, get the size of the output buffer by calling the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specifying SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="d2140-163">A função retornará uma estrutura [**de \_ tamanhos de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="d2140-163">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="d2140-164">O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="d2140-164">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

> [!Note]  
> <span data-ttu-id="d2140-165">Esses buffers devem ser fornecidos na ordem mostrada.</span><span class="sxs-lookup"><span data-stu-id="d2140-165">These buffers must be supplied in the order shown.</span></span>

 



| <span data-ttu-id="d2140-166">Tipo de buffer</span><span class="sxs-lookup"><span data-stu-id="d2140-166">Buffer type</span></span>                           | <span data-ttu-id="d2140-167">Description</span><span class="sxs-lookup"><span data-stu-id="d2140-167">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2140-168">\_cabeçalho de fluxo de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="d2140-168">SECBUFFER\_STREAM\_HEADER</span></span><br/>  | <span data-ttu-id="d2140-169">Usado internamente.</span><span class="sxs-lookup"><span data-stu-id="d2140-169">Used internally.</span></span> <span data-ttu-id="d2140-170">Nenhuma inicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2140-170">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="d2140-171">dados do SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="d2140-171">SECBUFFER\_DATA</span></span><br/>            | <span data-ttu-id="d2140-172">Contém a mensagem de [*texto sem formatação*](../secgloss/s-gly.md) a ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="d2140-172">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span><br/> |
| <span data-ttu-id="d2140-173">\_trailer de fluxo de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="d2140-173">SECBUFFER\_STREAM\_TRAILER</span></span><br/> | <span data-ttu-id="d2140-174">Usado internamente.</span><span class="sxs-lookup"><span data-stu-id="d2140-174">Used internally.</span></span> <span data-ttu-id="d2140-175">Nenhuma inicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2140-175">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="d2140-176">SECBUFFER \_ vazio</span><span class="sxs-lookup"><span data-stu-id="d2140-176">SECBUFFER\_EMPTY</span></span><br/>           | <span data-ttu-id="d2140-177">Usado internamente.</span><span class="sxs-lookup"><span data-stu-id="d2140-177">Used internally.</span></span> <span data-ttu-id="d2140-178">Nenhuma inicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2140-178">No initialization required.</span></span> <span data-ttu-id="d2140-179">O tamanho pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="d2140-179">Size can be zero.</span></span><br/>                                                      |



 

<span data-ttu-id="d2140-180">Para um desempenho ideal, as estruturas *PMessage* devem ser alocadas da memória contígua.</span><span class="sxs-lookup"><span data-stu-id="d2140-180">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="d2140-181">**Windows XP:** Essa função também era conhecida como **SealMessage**.</span><span class="sxs-lookup"><span data-stu-id="d2140-181">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="d2140-182">Os aplicativos agora devem usar apenas **EncryptMessage (Digest)** .</span><span class="sxs-lookup"><span data-stu-id="d2140-182">Applications should now use **EncryptMessage (Digest)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2140-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2140-183">Requirements</span></span>



| <span data-ttu-id="d2140-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2140-184">Requirement</span></span> | <span data-ttu-id="d2140-185">Valor</span><span class="sxs-lookup"><span data-stu-id="d2140-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2140-186">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2140-186">Minimum supported client</span></span><br/> | <span data-ttu-id="d2140-187">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d2140-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d2140-188">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2140-188">Minimum supported server</span></span><br/> | <span data-ttu-id="d2140-189">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2140-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d2140-190">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2140-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2140-191"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="d2140-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2140-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2140-193"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="d2140-194">DLL</span><span class="sxs-lookup"><span data-stu-id="d2140-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2140-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2140-195"><dt>Secur32.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="d2140-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2140-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2140-197">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="d2140-197">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="d2140-198">**AcceptSecurityContext (resumo)**</span><span class="sxs-lookup"><span data-stu-id="d2140-198">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="d2140-199">**DecryptMessage (resumo)**</span><span class="sxs-lookup"><span data-stu-id="d2140-199">**DecryptMessage (Digest)**</span></span>](decryptmessage--digest.md)
</dt> <dt>

[<span data-ttu-id="d2140-200">**InitializeSecurityContext (resumo)**</span><span class="sxs-lookup"><span data-stu-id="d2140-200">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="d2140-201">**QueryContextAttributes (resumo)**</span><span class="sxs-lookup"><span data-stu-id="d2140-201">**QueryContextAttributes (Digest)**</span></span>](querycontextattributes--digest.md)
</dt> <dt>

[<span data-ttu-id="d2140-202">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="d2140-202">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="d2140-203">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="d2140-203">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
