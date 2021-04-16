---
description: Retorna uma representação de cadeia de caracteres dos dados codificados.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Método EncodedData. Format
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750498"
---
# <a name="encodeddataformat-method"></a><span data-ttu-id="09c2a-103">Método EncodedData. Format</span><span class="sxs-lookup"><span data-stu-id="09c2a-103">EncodedData.Format method</span></span>

<span data-ttu-id="09c2a-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="09c2a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="09c2a-105">Em vez disso, use a [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="09c2a-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="09c2a-106">O método **Format** retorna uma representação de cadeia de caracteres dos dados codificados.</span><span class="sxs-lookup"><span data-stu-id="09c2a-106">The **Format** method returns a string representation of the encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="09c2a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09c2a-107">Syntax</span></span>


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a><span data-ttu-id="09c2a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09c2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09c2a-109">*bMultiLines* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="09c2a-109">*bMultiLines* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09c2a-110">Valor booliano que indica se a cadeia de caracteres retornada contém várias linhas.</span><span class="sxs-lookup"><span data-stu-id="09c2a-110">Boolean value that indicates whether the returned string contains multiple lines.</span></span> <span data-ttu-id="09c2a-111">Se **for true**, a cadeia de caracteres retornada poderá conter várias linhas separadas por **vbCrLf**.</span><span class="sxs-lookup"><span data-stu-id="09c2a-111">If **True**, the returned string may contain multiple lines separated by **vbCrLf**.</span></span> <span data-ttu-id="09c2a-112">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="09c2a-112">The default value is **False**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09c2a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09c2a-113">Return value</span></span>

<span data-ttu-id="09c2a-114">Uma cadeia de caracteres legível que representa os dados codificados.</span><span class="sxs-lookup"><span data-stu-id="09c2a-114">A human-readable string that represents the encoded data.</span></span> <span data-ttu-id="09c2a-115">Se o CAPICOM não entender os dados codificados, uma representação hexadecimal dos dados será retornada.</span><span class="sxs-lookup"><span data-stu-id="09c2a-115">If CAPICOM does not understand the encoded data, a hexadecimal representation of the data is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="09c2a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="09c2a-116">Remarks</span></span>

<span data-ttu-id="09c2a-117">O formato da cadeia de caracteres retornada pode mudar entre versões diferentes do CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="09c2a-117">The format of the returned string may change between different versions of CAPICOM.</span></span> <span data-ttu-id="09c2a-118">Não confie em nenhum formato específico em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="09c2a-118">Do not rely on any particular format in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="09c2a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09c2a-119">Requirements</span></span>



| <span data-ttu-id="09c2a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="09c2a-120">Requirement</span></span> | <span data-ttu-id="09c2a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="09c2a-121">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09c2a-122">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="09c2a-122">End of client support</span></span><br/> | <span data-ttu-id="09c2a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09c2a-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="09c2a-124">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="09c2a-124">End of server support</span></span><br/> | <span data-ttu-id="09c2a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09c2a-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="09c2a-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="09c2a-126">Redistributable</span></span><br/>       | <span data-ttu-id="09c2a-127">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="09c2a-127">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="09c2a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="09c2a-128">DLL</span></span><br/>                   | <dl> <span data-ttu-id="09c2a-129"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09c2a-129"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09c2a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="09c2a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09c2a-131">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="09c2a-131">**EncodedData**</span></span>](encodeddata.md)
</dt> </dl>

 

 
