---
description: Descriptografa uma mensagem usando NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: Função DecryptMessage (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 707f1bcd9ae697de0c3e23529fe2857f58d0e5e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780734"
---
# <a name="decryptmessage-ntlm-function"></a><span data-ttu-id="2e0fa-103">Função DecryptMessage (NTLM)</span><span class="sxs-lookup"><span data-stu-id="2e0fa-103">DecryptMessage (NTLM) function</span></span>

<span data-ttu-id="2e0fa-104">A função **DecryptMessage (NTLM)** descriptografa uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-104">The **DecryptMessage (NTLM)** function decrypts a message.</span></span> <span data-ttu-id="2e0fa-105">Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="2e0fa-106">[**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) e **DecryptMessage (NTLM)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-106">[**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) and **DecryptMessage (NTLM)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="2e0fa-107">Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0fa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e0fa-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="2e0fa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e0fa-109">Parameters</span></span>

<span data-ttu-id="2e0fa-110">*phContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e0fa-110">*phContext* \[in\]</span></span>

<span data-ttu-id="2e0fa-111">Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para descriptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="2e0fa-112">*PMessage* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2e0fa-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="2e0fa-113">Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="2e0fa-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="2e0fa-114">Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2e0fa-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="2e0fa-115">Pelo menos um deles deve ser do tipo dados SECBUFFER \_ .</span><span class="sxs-lookup"><span data-stu-id="2e0fa-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="2e0fa-116">Esse buffer contém a mensagem criptografada.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="2e0fa-117">A mensagem criptografada é descriptografada no local, substituindo o conteúdo original de seu buffer.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="2e0fa-118">*MessageSeqNo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e0fa-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="2e0fa-119">O número de sequência esperado pelo aplicativo de transporte, se houver.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="2e0fa-120">Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="2e0fa-121">*pfQOP* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2e0fa-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="2e0fa-122">Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="2e0fa-123">Esse parâmetro pode ser o sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="2e0fa-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2e0fa-124">Value</span></span></th><th><span data-ttu-id="2e0fa-125">Significado</span><span class="sxs-lookup"><span data-stu-id="2e0fa-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="2e0fa-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2e0fa-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="2e0fa-127">A mensagem não foi criptografada, mas um cabeçalho ou trailer foi produzido.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="2e0fa-128">KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="2e0fa-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e0fa-129">Return value</span></span>

<span data-ttu-id="2e0fa-130">Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="2e0fa-131">Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="2e0fa-132">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2e0fa-132">Return code</span></span>                     | <span data-ttu-id="2e0fa-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e0fa-133">Description</span></span>                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0fa-134">**s \_ E \_ mensagem incompleta \_**</span><span class="sxs-lookup"><span data-stu-id="2e0fa-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="2e0fa-135">Os dados no buffer de entrada estão incompletos.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="2e0fa-136">O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) novamente.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-136">The application needs to read more data from the server and call [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) again.</span></span> |
| <span data-ttu-id="2e0fa-137">**s \_ E \_ fora \_ de \_ sequência**</span><span class="sxs-lookup"><span data-stu-id="2e0fa-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="2e0fa-138">A mensagem não foi recebida na sequência correta.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-138">The message was not received in the correct sequence.</span></span>                                                                                                                    |

## <a name="remarks"></a><span data-ttu-id="2e0fa-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e0fa-139">Remarks</span></span>

<span data-ttu-id="2e0fa-140">Às vezes, um aplicativo lerá os dados da parte remota, tentará descriptografá-los usando **DecryptMessage (NTLM)** e descobrirá que o **DecryptMessage (NTLM)** foi bem-sucedido, mas os buffers de saída estão vazios.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (NTLM)**, and discover that **DecryptMessage (NTLM)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="2e0fa-141">Esse comportamento é normal e os aplicativos devem ser capazes de lidar com eles.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="2e0fa-142">**Windows XP:** Essa função também era conhecida como **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="2e0fa-143">Os aplicativos agora devem usar somente **DecryptMessage (NTLM)** .</span><span class="sxs-lookup"><span data-stu-id="2e0fa-143">Applications should now use **DecryptMessage (NTLM)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e0fa-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e0fa-144">Requirements</span></span>

| <span data-ttu-id="2e0fa-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e0fa-145">Requirement</span></span> | <span data-ttu-id="2e0fa-146">Valor</span><span class="sxs-lookup"><span data-stu-id="2e0fa-146">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="2e0fa-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e0fa-147">Minimum supported client</span></span> | <span data-ttu-id="2e0fa-148">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2e0fa-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="2e0fa-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e0fa-149">Minimum supported server</span></span> | <span data-ttu-id="2e0fa-150">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e0fa-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="2e0fa-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e0fa-151">Header</span></span>                   | <span data-ttu-id="2e0fa-152">SSPI. h (incluir Security. h)</span><span class="sxs-lookup"><span data-stu-id="2e0fa-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="2e0fa-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e0fa-153">Library</span></span>                  | <span data-ttu-id="2e0fa-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="2e0fa-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="2e0fa-155">DLL</span><span class="sxs-lookup"><span data-stu-id="2e0fa-155">DLL</span></span>                      | <span data-ttu-id="2e0fa-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="2e0fa-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="2e0fa-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e0fa-157">See also</span></span>

- [<span data-ttu-id="2e0fa-158">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="2e0fa-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="2e0fa-159">**EncryptMessage (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="2e0fa-159">**EncryptMessage (NTLM)**</span></span>](encryptmessage--ntlm.md)
- [<span data-ttu-id="2e0fa-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="2e0fa-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="2e0fa-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="2e0fa-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
