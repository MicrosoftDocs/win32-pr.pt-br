---
description: Define ou recupera os dados a serem assinados. Essa é a propriedade padrão.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: Propriedade SignedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750742"
---
# <a name="signeddatacontent-property"></a><span data-ttu-id="1ff85-104">Propriedade SignedData. Content</span><span class="sxs-lookup"><span data-stu-id="1ff85-104">SignedData.Content property</span></span>

<span data-ttu-id="1ff85-105">\[A propriedade de **conteúdo** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1ff85-105">\[The **Content** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1ff85-106">Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="1ff85-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1ff85-107">A propriedade de **conteúdo** define ou recupera os dados a serem assinados.</span><span class="sxs-lookup"><span data-stu-id="1ff85-107">The **Content** property sets or retrieves the data to be signed.</span></span> <span data-ttu-id="1ff85-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="1ff85-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff85-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ff85-109">Syntax</span></span>


```VB
SignedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="1ff85-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1ff85-110">Property value</span></span>

<span data-ttu-id="1ff85-111">Os dados a serem assinados.</span><span class="sxs-lookup"><span data-stu-id="1ff85-111">The data to be signed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ff85-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ff85-112">Remarks</span></span>

<span data-ttu-id="1ff85-113">Essa propriedade deve ser inicializada antes que o método [**Sign**](signeddata-sign.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="1ff85-113">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span> <span data-ttu-id="1ff85-114">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer assinatura associada ao objeto antes da alteração da propriedade é perdida.</span><span class="sxs-lookup"><span data-stu-id="1ff85-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff85-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ff85-115">Requirements</span></span>



| <span data-ttu-id="1ff85-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ff85-116">Requirement</span></span> | <span data-ttu-id="1ff85-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1ff85-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff85-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="1ff85-118">Redistributable</span></span><br/> | <span data-ttu-id="1ff85-119">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ff85-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1ff85-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1ff85-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="1ff85-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ff85-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff85-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ff85-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff85-123">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="1ff85-123">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
