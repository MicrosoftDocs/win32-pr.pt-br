---
description: Descriptografa o conteúdo Envelopado.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: Método EnvelopedData. Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752336"
---
# <a name="envelopeddatadecrypt-method"></a><span data-ttu-id="e1878-103">Método EnvelopedData. Decrypt</span><span class="sxs-lookup"><span data-stu-id="e1878-103">EnvelopedData.Decrypt method</span></span>

<span data-ttu-id="e1878-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e1878-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e1878-105">Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e1878-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e1878-106">O método **Decrypt** descriptografa o conteúdo Envelopado.</span><span class="sxs-lookup"><span data-stu-id="e1878-106">The **Decrypt** method decrypts enveloped content.</span></span> <span data-ttu-id="e1878-107">A descriptografia é feita se o destinatário da mensagem tiver acesso à [*chave privada*](../secgloss/p-gly.md) emparelhada com uma das [*chaves públicas*](../secgloss/p-gly.md) usadas para envelope a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1878-107">Decryption is done if the recipient of the message has access to the [*private key*](../secgloss/p-gly.md) paired with one of the [*public keys*](../secgloss/p-gly.md) used to envelop the message.</span></span> <span data-ttu-id="e1878-108">Chamar o método **decodificar** redefine o [*estado*](../secgloss/s-gly.md) do objeto.</span><span class="sxs-lookup"><span data-stu-id="e1878-108">Calling the **Decrypt** method resets the [*state*](../secgloss/s-gly.md) of the object.</span></span> <span data-ttu-id="e1878-109">Se o método **Decrypt** for executado com sucesso, a propriedade [**Content**](envelopeddata-content.md) do objeto [**EnvelopedData**](envelopeddata.md) será definida como a mensagem de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="e1878-109">If the **Decrypt** method succeeds, the [**Content**](envelopeddata-content.md) property of the [**EnvelopedData**](envelopeddata.md) object is set to the plaintext message.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1878-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1878-110">Syntax</span></span>


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="e1878-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1878-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1878-112">*EnvelopedMessage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1878-112">*EnvelopedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1878-113">Cadeia de caracteres que contém os dados de envelope a serem descriptografados.</span><span class="sxs-lookup"><span data-stu-id="e1878-113">String that contains the enveloped data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1878-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1878-114">Return value</span></span>

<span data-ttu-id="e1878-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e1878-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1878-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1878-116">Remarks</span></span>

<span data-ttu-id="e1878-117">Os dados descriptografados se tornam o valor da propriedade [**Content**](envelopeddata-content.md) para o objeto [**EnvelopedData**](envelopeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="e1878-117">The decrypted data becomes the [**Content**](envelopeddata-content.md) property value for the [**EnvelopedData**](envelopeddata.md) object.</span></span>

<span data-ttu-id="e1878-118">Se o usuário desse método não tiver acesso a uma chave privada que corresponda a uma das chaves públicas usadas para envelope a mensagem, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="e1878-118">If the user of this method does not have access to a private key that matches one of the public keys used to envelop the message, the method fails.</span></span> <span data-ttu-id="e1878-119">Esse método falhará se o certificado da chave privada associada não estiver no computador local MY Store ou no usuário atual MY Store.</span><span class="sxs-lookup"><span data-stu-id="e1878-119">This method will fail if the certificate for the associated private key is not in either the local computer MY store or the current user MY store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1878-120">Quando esse método é chamado de um script da Web, o script precisa usar sua [*chave privada*](../secgloss/p-gly.md) para descriptografar os dados.</span><span class="sxs-lookup"><span data-stu-id="e1878-120">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to decrypt the data.</span></span> <span data-ttu-id="e1878-121">Permitir que sites não confiáveis usem sua chave privada é um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="e1878-121">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="e1878-122">Uma caixa de diálogo que pergunta se o site pode usar sua chave privada é exibida quando esse método é chamado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="e1878-122">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="e1878-123">Se você permitir que o script Use sua chave privada e selecionar "não perguntar novamente", a caixa de diálogo não aparecerá mais para nenhum script que use sua chave privada para descriptografar os dados dentro desse domínio.</span><span class="sxs-lookup"><span data-stu-id="e1878-123">If you allow the script to use your private key and select "Do not ask me this again," the dialog box will no longer appear for any script that uses your private key to decrypt data within that domain.</span></span> <span data-ttu-id="e1878-124">No entanto, os scripts fora desse domínio que tentarem usar sua chave privada para descriptografar dados ainda farão com que essa caixa de diálogo seja exibida.</span><span class="sxs-lookup"><span data-stu-id="e1878-124">However, scripts outside that domain that attempt to use your private key to decrypt data will still cause this dialog box to appear.</span></span> <span data-ttu-id="e1878-125">Se você não permitir que o script Use sua chave privada e selecionar "não perguntar novamente", os scripts nesse domínio serão recusados automaticamente a capacidade de usar sua chave privada para descriptografar os dados.</span><span class="sxs-lookup"><span data-stu-id="e1878-125">If you do not allow the script to use your private key and select "Do not ask me this again," scripts within that domain will automatically be refused the ability to use your private key to decrypt data.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1878-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1878-126">Requirements</span></span>



| <span data-ttu-id="e1878-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1878-127">Requirement</span></span> | <span data-ttu-id="e1878-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e1878-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1878-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e1878-129">End of client support</span></span><br/> | <span data-ttu-id="e1878-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1878-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e1878-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e1878-131">End of server support</span></span><br/> | <span data-ttu-id="e1878-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1878-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e1878-133">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e1878-133">Redistributable</span></span><br/>       | <span data-ttu-id="e1878-134">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1878-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e1878-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e1878-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e1878-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1878-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1878-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1878-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1878-138">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="e1878-138">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="e1878-139">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="e1878-139">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
