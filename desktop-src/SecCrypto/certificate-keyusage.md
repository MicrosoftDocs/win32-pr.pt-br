---
description: Retorna um objeto KeyUsage que indica o uso de chave válido do certificado.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: 'Método ICertificate2:: KeyUsage'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85fe008880d9613586d38dba7afaca39bb29f72f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754504"
---
# <a name="icertificate2keyusage-method"></a><span data-ttu-id="ba482-103">Método ICertificate2:: KeyUsage</span><span class="sxs-lookup"><span data-stu-id="ba482-103">ICertificate2::KeyUsage method</span></span>

<span data-ttu-id="ba482-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ba482-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ba482-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ba482-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ba482-106">O método **KeyUsage** retorna um objeto [**KeyUsage**](keyusage.md) que indica o uso de chave válido do certificado.</span><span class="sxs-lookup"><span data-stu-id="ba482-106">The **KeyUsage** method returns a [**KeyUsage**](keyusage.md) object that indicates the valid key usage of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba482-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba482-107">Syntax</span></span>


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="ba482-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba482-108">Parameters</span></span>

<span data-ttu-id="ba482-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ba482-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba482-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba482-110">Requirements</span></span>



| <span data-ttu-id="ba482-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba482-111">Requirement</span></span> | <span data-ttu-id="ba482-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ba482-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba482-113">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ba482-113">End of client support</span></span><br/> | <span data-ttu-id="ba482-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba482-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ba482-115">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ba482-115">End of server support</span></span><br/> | <span data-ttu-id="ba482-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba482-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ba482-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ba482-117">Redistributable</span></span><br/>       | <span data-ttu-id="ba482-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba482-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ba482-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ba482-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ba482-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba482-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba482-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba482-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba482-122">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="ba482-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="ba482-123">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="ba482-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
