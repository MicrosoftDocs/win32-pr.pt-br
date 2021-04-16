---
description: Cria uma cadeia de verificação de certificado para um certificado e retorna um objeto CertificateStatus que contém o status de validade do certificado.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'Método ICertificate2:: IsValid'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757477"
---
# <a name="icertificate2isvalid-method"></a><span data-ttu-id="5f27c-103">Método ICertificate2:: IsValid</span><span class="sxs-lookup"><span data-stu-id="5f27c-103">ICertificate2::IsValid method</span></span>

<span data-ttu-id="5f27c-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5f27c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5f27c-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="5f27c-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5f27c-106">O método **IsValid** cria uma cadeia de verificação de certificado para um certificado e retorna um objeto [**CertificateStatus**](certificatestatus.md) que contém o status de validade do certificado.</span><span class="sxs-lookup"><span data-stu-id="5f27c-106">The **IsValid** method builds a certificate verification chain for a certificate and returns a [**CertificateStatus**](certificatestatus.md) object that contains the validity status of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f27c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f27c-107">Syntax</span></span>


```VB
Certificate.IsValid()
```



## <a name="parameters"></a><span data-ttu-id="5f27c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f27c-108">Parameters</span></span>

<span data-ttu-id="5f27c-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5f27c-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f27c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f27c-110">Requirements</span></span>



| <span data-ttu-id="5f27c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f27c-111">Requirement</span></span> | <span data-ttu-id="5f27c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5f27c-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f27c-113">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5f27c-113">End of client support</span></span><br/> | <span data-ttu-id="5f27c-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f27c-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5f27c-115">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="5f27c-115">End of server support</span></span><br/> | <span data-ttu-id="5f27c-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f27c-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5f27c-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5f27c-117">Redistributable</span></span><br/>       | <span data-ttu-id="5f27c-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5f27c-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5f27c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5f27c-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5f27c-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f27c-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f27c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f27c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f27c-122">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="5f27c-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="5f27c-123">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="5f27c-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
