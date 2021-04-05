---
description: Não há suporte para a função RKeyPFXInstall.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Função RKeyPFXInstall (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920926"
---
# <a name="rkeypfxinstall-function"></a><span data-ttu-id="dfaeb-103">Função RKeyPFXInstall</span><span class="sxs-lookup"><span data-stu-id="dfaeb-103">RKeyPFXInstall function</span></span>

<span data-ttu-id="dfaeb-104">Não há suporte para a função **RKeyPFXInstall** .</span><span class="sxs-lookup"><span data-stu-id="dfaeb-104">The **RKeyPFXInstall** function is not supported.</span></span>

<span data-ttu-id="dfaeb-105">**Windows Server 2003:** A função **RKeyPFXInstall** instala um certificado em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-105">**Windows Server 2003:** The **RKeyPFXInstall** function installs a certificate on a remote computer.</span></span> <span data-ttu-id="dfaeb-106">Observe que esse comportamento foi alterado com o Windows Server 2003 com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dfaeb-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="dfaeb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfaeb-107">Syntax</span></span>


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dfaeb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfaeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfaeb-109">*hKeySvcCli* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dfaeb-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfaeb-110">Um identificador de [**\_ identificador KEYSVCC**](keysvcc-handle.md) aberto anteriormente pelo [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="dfaeb-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="dfaeb-111">O identificador representa o computador remoto que receberá o certificado.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-111">The handle represents the remote computer that will receive the certificate.</span></span> <span data-ttu-id="dfaeb-112">Esse valor não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-112">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfaeb-113">*pPFX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dfaeb-113">*pPFX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfaeb-114">Um ponteiro para uma estrutura de [**\_ blob KEYSVC**](keysvc-blob.md) que representa o certificado a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-114">A pointer to a [**KEYSVC\_BLOB**](keysvc-blob.md) structure that represents the certificate to install.</span></span> <span data-ttu-id="dfaeb-115">O BLOB está no formato [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="dfaeb-115">The BLOB is in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> <dt>

<span data-ttu-id="dfaeb-116">*ppassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dfaeb-116">*pPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfaeb-117">Um ponteiro para uma estrutura de [**\_ cadeia de \_ caracteres Unicode KEYSVC**](keysvc-unicode-string.md) que representa a senha para o blob.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-117">A pointer to a [**KEYSVC\_UNICODE\_STRING**](keysvc-unicode-string.md) structure that represents the password for the BLOB.</span></span> <span data-ttu-id="dfaeb-118">Quando você terminar de usar a senha, limpe a senha da memória chamando a função [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dfaeb-118">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="dfaeb-119">Para obter mais informações sobre como proteger senhas, consulte [manipulando senhas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="dfaeb-119">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfaeb-120">*ulFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dfaeb-120">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfaeb-121">Sinalizadores que especificam as opções de instalação do certificado.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-121">Flags that specify the certificate installation options.</span></span> <span data-ttu-id="dfaeb-122">Esse parâmetro pode ser um zero ou uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-122">This parameter can be a zero or a combination of the following values.</span></span>



| <span data-ttu-id="dfaeb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dfaeb-123">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="dfaeb-124">Significado</span><span class="sxs-lookup"><span data-stu-id="dfaeb-124">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <span data-ttu-id="dfaeb-125"><dt>**Cript \_ Exportável**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dfaeb-125"><dt>**CRYPT\_EXPORTABLE**</dt> <dt></dt></span></span> </dl>              | <span data-ttu-id="dfaeb-126">As chaves importadas são marcadas como exportáveis.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-126">Imported keys are marked as exportable.</span></span><br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <span data-ttu-id="dfaeb-127"><dt>**Cript \_ conjunto de \_ chaves da máquina**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dfaeb-127"><dt>**CRYPT\_MACHINE\_KEYSET**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="dfaeb-128">As chaves privadas são armazenadas no computador remoto e não no usuário atual.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-128">Private keys are stored under the remote computer and not under the current user.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfaeb-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dfaeb-129">Return value</span></span>

<span data-ttu-id="dfaeb-130">Se a função for bem-sucedida, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-130">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="dfaeb-131">Se a função falhar, o valor de retorno será um **ULONG** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-131">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfaeb-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfaeb-132">Requirements</span></span>



| <span data-ttu-id="dfaeb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfaeb-133">Requirement</span></span> | <span data-ttu-id="dfaeb-134">Valor</span><span class="sxs-lookup"><span data-stu-id="dfaeb-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfaeb-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfaeb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dfaeb-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dfaeb-136">None supported</span></span><br/>                                                             |
| <span data-ttu-id="dfaeb-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfaeb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dfaeb-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dfaeb-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dfaeb-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfaeb-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfaeb-140"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfaeb-140"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfaeb-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfaeb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfaeb-142">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="dfaeb-142">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="dfaeb-143">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="dfaeb-143">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 
