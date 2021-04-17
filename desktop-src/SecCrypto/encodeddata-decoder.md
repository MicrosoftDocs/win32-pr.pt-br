---
description: Obtém um objeto decodificador, se houver.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: Método EncodedData. Decoder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749472"
---
# <a name="encodeddatadecoder-method"></a><span data-ttu-id="d1a8a-103">Método EncodedData. Decoder</span><span class="sxs-lookup"><span data-stu-id="d1a8a-103">EncodedData.Decoder method</span></span>

<span data-ttu-id="d1a8a-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d1a8a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d1a8a-105">Em vez disso, use a [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d1a8a-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d1a8a-106">O método de **decodificador** Obtém um objeto decodificador, se houver.</span><span class="sxs-lookup"><span data-stu-id="d1a8a-106">The **Decoder** method obtains a decoder object, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a8a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1a8a-107">Syntax</span></span>


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a><span data-ttu-id="d1a8a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1a8a-108">Parameters</span></span>

<span data-ttu-id="d1a8a-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d1a8a-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1a8a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1a8a-110">Remarks</span></span>

<span data-ttu-id="d1a8a-111">Se os dados codificados não tiverem um objeto decodificador, **NULL** será retornado.</span><span class="sxs-lookup"><span data-stu-id="d1a8a-111">If the encoded data does not have a decoder object, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a8a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1a8a-112">Requirements</span></span>



| <span data-ttu-id="d1a8a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1a8a-113">Requirement</span></span> | <span data-ttu-id="d1a8a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d1a8a-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a8a-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d1a8a-115">End of client support</span></span><br/> | <span data-ttu-id="d1a8a-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1a8a-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d1a8a-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d1a8a-117">End of server support</span></span><br/> | <span data-ttu-id="d1a8a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1a8a-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d1a8a-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d1a8a-119">Redistributable</span></span><br/>       | <span data-ttu-id="d1a8a-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1a8a-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d1a8a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d1a8a-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d1a8a-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1a8a-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
