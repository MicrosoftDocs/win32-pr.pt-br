---
description: Importa um certificado codificado anteriormente de uma cadeia de caracteres para o objeto de certificado.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'Método ICertificate2:: Import'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749209"
---
# <a name="icertificate2import-method"></a><span data-ttu-id="7376a-103">Método ICertificate2:: Import</span><span class="sxs-lookup"><span data-stu-id="7376a-103">ICertificate2::Import method</span></span>

<span data-ttu-id="7376a-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7376a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7376a-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7376a-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7376a-106">O método de **importação** importa um certificado codificado anteriormente de uma cadeia de caracteres para o objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="7376a-106">The **Import** method imports a previously encoded certificate from a string into the [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="7376a-107">Chamar esse método redefine o [*estado*](../secgloss/s-gly.md) desse objeto.</span><span class="sxs-lookup"><span data-stu-id="7376a-107">Calling this method resets the [*state*](../secgloss/s-gly.md) of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7376a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7376a-108">Syntax</span></span>


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a><span data-ttu-id="7376a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7376a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7376a-110">*EncodedCertificate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7376a-110">*EncodedCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7376a-111">Uma cadeia de caracteres que contém os dados de certificado codificados a serem importados.</span><span class="sxs-lookup"><span data-stu-id="7376a-111">A string that contains the encoded certificate data to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7376a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7376a-112">Return value</span></span>

<span data-ttu-id="7376a-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7376a-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7376a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7376a-114">Requirements</span></span>



| <span data-ttu-id="7376a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7376a-115">Requirement</span></span> | <span data-ttu-id="7376a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7376a-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7376a-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7376a-117">End of client support</span></span><br/> | <span data-ttu-id="7376a-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7376a-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7376a-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7376a-119">End of server support</span></span><br/> | <span data-ttu-id="7376a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7376a-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7376a-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7376a-121">Redistributable</span></span><br/>       | <span data-ttu-id="7376a-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="7376a-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7376a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7376a-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7376a-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7376a-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7376a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7376a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7376a-126">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="7376a-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7376a-127">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="7376a-127">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
