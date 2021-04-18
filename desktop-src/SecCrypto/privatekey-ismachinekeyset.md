---
description: Retorna um valor booliano que indica se a chave privada pertence a um conjunto de chaves do computador.
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: Método PrivateKey. ismachinekeyset
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a42e3f932b8294d9671b7901437151d9fbbe5a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788106"
---
# <a name="privatekeyismachinekeyset-method"></a><span data-ttu-id="6726a-103">Método PrivateKey. ismachinekeyset</span><span class="sxs-lookup"><span data-stu-id="6726a-103">PrivateKey.IsMachineKeyset method</span></span>

<span data-ttu-id="6726a-104">\[O método **Ismachinekeyset** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6726a-104">\[The **IsMachineKeyset** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6726a-105">Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6726a-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6726a-106">O método **Ismachinekeyset** retorna um valor booliano que indica se a chave privada pertence a um conjunto de chaves de computador.</span><span class="sxs-lookup"><span data-stu-id="6726a-106">The **IsMachineKeyset** method returns a Boolean value that indicates whether the private key belongs to a machine key set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6726a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6726a-107">Syntax</span></span>


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a><span data-ttu-id="6726a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6726a-108">Parameters</span></span>

<span data-ttu-id="6726a-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6726a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6726a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6726a-110">Return value</span></span>

<span data-ttu-id="6726a-111">Se for true, a chave privada pertencerá a um conjunto de chaves de computador.</span><span class="sxs-lookup"><span data-stu-id="6726a-111">If true, the private key belongs to a machine key set.</span></span>

## <a name="remarks"></a><span data-ttu-id="6726a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6726a-112">Remarks</span></span>

<span data-ttu-id="6726a-113">O valor de retorno desse método é dependente do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) usado.</span><span class="sxs-lookup"><span data-stu-id="6726a-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="6726a-114">Esse método retornará um valor confiável se um Microsoft CSP for usado.</span><span class="sxs-lookup"><span data-stu-id="6726a-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="6726a-115">Se o CSP não for um CSP da Microsoft, o valor de retorno não poderá ser confiável para ser preciso.</span><span class="sxs-lookup"><span data-stu-id="6726a-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6726a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6726a-116">Requirements</span></span>



| <span data-ttu-id="6726a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6726a-117">Requirement</span></span> | <span data-ttu-id="6726a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6726a-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6726a-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6726a-119">Redistributable</span></span><br/> | <span data-ttu-id="6726a-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6726a-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6726a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6726a-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="6726a-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6726a-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6726a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6726a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6726a-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="6726a-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
