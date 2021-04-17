---
description: Define ou recupera o conteúdo de texto não criptografado de uma mensagem a ser envelopada. Essa é a propriedade padrão.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Propriedade EnvelopedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751318"
---
# <a name="envelopeddatacontent-property"></a><span data-ttu-id="72267-104">Propriedade EnvelopedData. Content</span><span class="sxs-lookup"><span data-stu-id="72267-104">EnvelopedData.Content property</span></span>

<span data-ttu-id="72267-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72267-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="72267-106">Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="72267-106">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="72267-107">A propriedade de **conteúdo** define ou recupera o conteúdo de texto não criptografado de uma mensagem a ser envelopada.</span><span class="sxs-lookup"><span data-stu-id="72267-107">The **Content** property sets or retrieves the plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="72267-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="72267-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="72267-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="72267-109">Syntax</span></span>


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="72267-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="72267-110">Property value</span></span>

<span data-ttu-id="72267-111">O conteúdo de texto não criptografado de uma mensagem a ser envelopada.</span><span class="sxs-lookup"><span data-stu-id="72267-111">The plaintext content of a message to be enveloped.</span></span>

## <a name="remarks"></a><span data-ttu-id="72267-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="72267-112">Remarks</span></span>

<span data-ttu-id="72267-113">A definição dessa propriedade deve ser feita antes que o método [**Encrypt**](envelopeddata-encrypt.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="72267-113">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span> <span data-ttu-id="72267-114">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer conteúdo criptografado no objeto é perdido.</span><span class="sxs-lookup"><span data-stu-id="72267-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="72267-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72267-115">Requirements</span></span>



| <span data-ttu-id="72267-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72267-116">Requirement</span></span> | <span data-ttu-id="72267-117">Valor</span><span class="sxs-lookup"><span data-stu-id="72267-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72267-118">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="72267-118">End of client support</span></span><br/> | <span data-ttu-id="72267-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72267-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="72267-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="72267-120">End of server support</span></span><br/> | <span data-ttu-id="72267-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72267-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="72267-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="72267-122">Redistributable</span></span><br/>       | <span data-ttu-id="72267-123">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="72267-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="72267-124">DLL</span><span class="sxs-lookup"><span data-stu-id="72267-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="72267-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72267-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72267-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="72267-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72267-127">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="72267-127">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
