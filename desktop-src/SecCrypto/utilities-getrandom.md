---
description: Gera um número aleatório seguro usando o CSP (provedor de serviços de criptografia) padrão.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Método Utilities. getaleatório
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813100"
---
# <a name="utilitiesgetrandom-method"></a><span data-ttu-id="dec3e-103">Método Utilities. getaleatório</span><span class="sxs-lookup"><span data-stu-id="dec3e-103">Utilities.GetRandom method</span></span>

<span data-ttu-id="dec3e-104">\[O método **getaleatório** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="dec3e-104">\[The **GetRandom** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="dec3e-105">O método **getaleatório** gera um número aleatório seguro usando o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) padrão.</span><span class="sxs-lookup"><span data-stu-id="dec3e-105">The **GetRandom** method generates a secure random number using the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="dec3e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dec3e-106">Syntax</span></span>


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="dec3e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dec3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec3e-108">*Comprimento* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dec3e-108">*Length* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dec3e-109">O comprimento, em bytes, do número aleatório a ser criado.</span><span class="sxs-lookup"><span data-stu-id="dec3e-109">The length, in bytes, of the random number to create.</span></span> <span data-ttu-id="dec3e-110">O valor padrão é 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="dec3e-110">The default value is 8 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dec3e-111">*EncodingType* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dec3e-111">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dec3e-112">Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que indica o tipo de codificação a ser usado para o número aleatório gerado.</span><span class="sxs-lookup"><span data-stu-id="dec3e-112">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the type of encoding to use for the generated random number.</span></span> <span data-ttu-id="dec3e-113">O valor padrão é capicote de \_ codificação \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="dec3e-113">The default value is CAPICOM\_ENCODE\_BINARY.</span></span> <span data-ttu-id="dec3e-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dec3e-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="dec3e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dec3e-115">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="dec3e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="dec3e-116">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="dec3e-117"><dt>**CAPICOM \_ codificar \_ qualquer**</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-117"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="dec3e-118">Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido.</span><span class="sxs-lookup"><span data-stu-id="dec3e-118">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="dec3e-119">Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="dec3e-119">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="dec3e-120">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="dec3e-120">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="dec3e-121"><dt>**CAPICOM \_ codificar \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-121"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="dec3e-122">Os dados são salvos como uma cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="dec3e-122">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="dec3e-123"><dt>**capicote de \_ codificação \_ binário**</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-123"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="dec3e-124">Os dados são salvos como uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="dec3e-124">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec3e-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dec3e-125">Return value</span></span>

<span data-ttu-id="dec3e-126">Um *comprimento* de número gerado aleatoriamente de bytes com a codificação especificada.</span><span class="sxs-lookup"><span data-stu-id="dec3e-126">A randomly generated number *Length* bytes long, with the specified encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec3e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec3e-127">Requirements</span></span>



| <span data-ttu-id="dec3e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec3e-128">Requirement</span></span> | <span data-ttu-id="dec3e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="dec3e-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dec3e-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="dec3e-130">Redistributable</span></span><br/> | <span data-ttu-id="dec3e-131">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="dec3e-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dec3e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dec3e-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="dec3e-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec3e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="dec3e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec3e-135">**Utilitários**</span><span class="sxs-lookup"><span data-stu-id="dec3e-135">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 
