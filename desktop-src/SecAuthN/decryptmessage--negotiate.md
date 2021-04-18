---
description: Descriptografa uma mensagem usando Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: Função DecryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764317"
---
# <a name="decryptmessage-negotiate-function"></a><span data-ttu-id="da04a-103">Função DecryptMessage (Negotiate)</span><span class="sxs-lookup"><span data-stu-id="da04a-103">DecryptMessage (Negotiate) function</span></span>

<span data-ttu-id="da04a-104">A função **DecryptMessage (Negotiate)** descriptografa uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="da04a-104">The **DecryptMessage (Negotiate)** function decrypts a message.</span></span> <span data-ttu-id="da04a-105">Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.</span><span class="sxs-lookup"><span data-stu-id="da04a-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="da04a-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) e **DecryptMessage (Negotiate)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando.</span><span class="sxs-lookup"><span data-stu-id="da04a-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) and **DecryptMessage (Negotiate)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="da04a-107">Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="da04a-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="da04a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da04a-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="da04a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da04a-109">Parameters</span></span>

<span data-ttu-id="da04a-110">*phContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da04a-110">*phContext* \[in\]</span></span>

<span data-ttu-id="da04a-111">Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para descriptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="da04a-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="da04a-112">*PMessage* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="da04a-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="da04a-113">Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="da04a-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="da04a-114">Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) .</span><span class="sxs-lookup"><span data-stu-id="da04a-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures .</span></span> <span data-ttu-id="da04a-115">Pelo menos um deles deve ser do tipo dados SECBUFFER \_ .</span><span class="sxs-lookup"><span data-stu-id="da04a-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="da04a-116">Esse buffer contém a mensagem criptografada.</span><span class="sxs-lookup"><span data-stu-id="da04a-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="da04a-117">A mensagem criptografada é descriptografada no local, substituindo o conteúdo original de seu buffer.</span><span class="sxs-lookup"><span data-stu-id="da04a-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="da04a-118">*MessageSeqNo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da04a-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="da04a-119">O número de sequência esperado pelo aplicativo de transporte, se houver.</span><span class="sxs-lookup"><span data-stu-id="da04a-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="da04a-120">Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="da04a-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="da04a-121">*pfQOP* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="da04a-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="da04a-122">Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.</span><span class="sxs-lookup"><span data-stu-id="da04a-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="da04a-123">Esse parâmetro pode ser o sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="da04a-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="da04a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="da04a-124">Value</span></span></th><th><span data-ttu-id="da04a-125">Significado</span><span class="sxs-lookup"><span data-stu-id="da04a-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="da04a-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da04a-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="da04a-127">A mensagem não foi criptografada, mas um cabeçalho ou trailer foi produzido.</span><span class="sxs-lookup"><span data-stu-id="da04a-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="da04a-128">KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</span><span class="sxs-lookup"><span data-stu-id="da04a-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="da04a-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da04a-129">Return value</span></span>

<span data-ttu-id="da04a-130">Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da04a-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="da04a-131">Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="da04a-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="da04a-132">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="da04a-132">Return code</span></span>                     | <span data-ttu-id="da04a-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="da04a-133">Description</span></span>                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da04a-134">**s \_ E \_ mensagem incompleta \_**</span><span class="sxs-lookup"><span data-stu-id="da04a-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="da04a-135">Os dados no buffer de entrada estão incompletos.</span><span class="sxs-lookup"><span data-stu-id="da04a-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="da04a-136">O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) novamente.</span><span class="sxs-lookup"><span data-stu-id="da04a-136">The application needs to read more data from the server and call [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) again.</span></span> |
| <span data-ttu-id="da04a-137">**s \_ E \_ fora \_ de \_ sequência**</span><span class="sxs-lookup"><span data-stu-id="da04a-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="da04a-138">A mensagem não foi recebida na sequência correta.</span><span class="sxs-lookup"><span data-stu-id="da04a-138">The message was not received in the correct sequence.</span></span>                                                                                                                              |

## <a name="remarks"></a><span data-ttu-id="da04a-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="da04a-139">Remarks</span></span>

<span data-ttu-id="da04a-140">Às vezes, um aplicativo lerá os dados da parte remota, tentará descriptografá-los usando **DecryptMessage (Negotiate)** e descobrirá que o **DecryptMessage (Negotiate)** foi bem-sucedido, mas os buffers de saída estão vazios.</span><span class="sxs-lookup"><span data-stu-id="da04a-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Negotiate)**, and discover that **DecryptMessage (Negotiate)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="da04a-141">Esse comportamento é normal e os aplicativos devem ser capazes de lidar com eles.</span><span class="sxs-lookup"><span data-stu-id="da04a-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="da04a-142">**Windows XP:** Essa função também era conhecida como **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="da04a-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="da04a-143">Os aplicativos agora devem usar apenas **DecryptMessage (Negotiate)** .</span><span class="sxs-lookup"><span data-stu-id="da04a-143">Applications should now use **DecryptMessage (Negotiate)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="da04a-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da04a-144">Requirements</span></span>

| <span data-ttu-id="da04a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="da04a-145">Requirement</span></span> | <span data-ttu-id="da04a-146">Valor</span><span class="sxs-lookup"><span data-stu-id="da04a-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="da04a-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da04a-147">Minimum supported client</span></span> | <span data-ttu-id="da04a-148">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="da04a-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="da04a-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da04a-149">Minimum supported server</span></span> | <span data-ttu-id="da04a-150">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da04a-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="da04a-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da04a-151">Header</span></span>                   | <span data-ttu-id="da04a-152">SSPI. h (incluir Security. h)</span><span class="sxs-lookup"><span data-stu-id="da04a-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="da04a-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da04a-153">Library</span></span>                  | <span data-ttu-id="da04a-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="da04a-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="da04a-155">DLL</span><span class="sxs-lookup"><span data-stu-id="da04a-155">DLL</span></span>                      | <span data-ttu-id="da04a-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="da04a-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="da04a-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="da04a-157">See also</span></span>

- [<span data-ttu-id="da04a-158">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="da04a-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="da04a-159">**EncryptMessage (negociar)**</span><span class="sxs-lookup"><span data-stu-id="da04a-159">**EncryptMessage (Negotiate)**</span></span>](encryptmessage--negotiate.md)
- [<span data-ttu-id="da04a-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="da04a-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="da04a-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="da04a-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
