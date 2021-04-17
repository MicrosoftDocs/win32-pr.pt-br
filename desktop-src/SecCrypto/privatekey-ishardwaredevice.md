---
description: Retorna um valor booliano que indica se a chave privada está armazenada em um dispositivo de hardware.
ms.assetid: 9a06f598-55cd-441b-a85f-8bec299f8245
title: Método PrivateKey. IsHardwareDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsHardwareDevice
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23b6fd379fd3a3b53fe0600dbf28481cd5ef2f86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779355"
---
# <a name="privatekeyishardwaredevice-method"></a><span data-ttu-id="4a2a8-103">Método PrivateKey. IsHardwareDevice</span><span class="sxs-lookup"><span data-stu-id="4a2a8-103">PrivateKey.IsHardwareDevice method</span></span>

<span data-ttu-id="4a2a8-104">\[O método **IsHardwareDevice** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4a2a8-104">\[The **IsHardwareDevice** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4a2a8-105">Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4a2a8-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4a2a8-106">O método **IsHardwareDevice** retorna um valor booliano que indica se a chave privada está armazenada em um dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="4a2a8-106">The **IsHardwareDevice** method returns a Boolean value that indicates whether the private key is stored in a hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2a8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a2a8-107">Syntax</span></span>


```VB
PrivateKey.IsHardwareDevice()
```



## <a name="parameters"></a><span data-ttu-id="4a2a8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a2a8-108">Parameters</span></span>

<span data-ttu-id="4a2a8-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4a2a8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a2a8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a2a8-110">Return value</span></span>

<span data-ttu-id="4a2a8-111">Se for true, a chave privada será armazenada em um dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="4a2a8-111">If true, the private key is stored in a hardware device.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a2a8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a2a8-112">Remarks</span></span>

<span data-ttu-id="4a2a8-113">O valor de retorno desse método é dependente do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) usado.</span><span class="sxs-lookup"><span data-stu-id="4a2a8-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="4a2a8-114">Esse método retornará um valor confiável se um Microsoft CSP for usado.</span><span class="sxs-lookup"><span data-stu-id="4a2a8-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="4a2a8-115">Se o CSP não for um CSP da Microsoft, o valor de retorno não poderá ser confiável para ser preciso.</span><span class="sxs-lookup"><span data-stu-id="4a2a8-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2a8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a2a8-116">Requirements</span></span>



| <span data-ttu-id="4a2a8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2a8-117">Requirement</span></span> | <span data-ttu-id="4a2a8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4a2a8-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2a8-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4a2a8-119">Redistributable</span></span><br/> | <span data-ttu-id="4a2a8-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a2a8-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4a2a8-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4a2a8-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="4a2a8-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a2a8-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2a8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a2a8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2a8-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="4a2a8-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
