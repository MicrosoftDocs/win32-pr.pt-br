---
description: Define ou recupera o valor do atributo.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Propriedade Attribute. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758282"
---
# <a name="attributevalue-property"></a><span data-ttu-id="c9a89-103">Propriedade Attribute. Value</span><span class="sxs-lookup"><span data-stu-id="c9a89-103">Attribute.Value property</span></span>

<span data-ttu-id="c9a89-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c9a89-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="c9a89-105">Em vez disso, use a [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="c9a89-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="c9a89-106">A propriedade **Value** define ou recupera o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="c9a89-106">The **Value** property sets or retrieves the value of the attribute.</span></span>

<span data-ttu-id="c9a89-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c9a89-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a89-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9a89-108">Syntax</span></span>


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="c9a89-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c9a89-109">Property value</span></span>

<span data-ttu-id="c9a89-110">Uma variável **Variant** que contém o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="c9a89-110">A **Variant** variable that contains the value of the attribute.</span></span> <span data-ttu-id="c9a89-111">Para atributos de **tempo de \_ \_ \_ assinatura \_ de atributo capicod** , o tipo de dados é **Date**.</span><span class="sxs-lookup"><span data-stu-id="c9a89-111">For **CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME** attributes, the data type is **DATE**.</span></span> <span data-ttu-id="c9a89-112">Para todos os outros atributos, o valor da propriedade é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c9a89-112">For all other attributes, the property value is a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a89-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9a89-113">Requirements</span></span>



| <span data-ttu-id="c9a89-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a89-114">Requirement</span></span> | <span data-ttu-id="c9a89-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c9a89-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a89-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c9a89-116">End of client support</span></span><br/> | <span data-ttu-id="c9a89-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9a89-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c9a89-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c9a89-118">End of server support</span></span><br/> | <span data-ttu-id="c9a89-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9a89-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c9a89-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c9a89-120">Redistributable</span></span><br/>       | <span data-ttu-id="c9a89-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9a89-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c9a89-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c9a89-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c9a89-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9a89-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
