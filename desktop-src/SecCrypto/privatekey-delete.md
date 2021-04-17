---
description: Exclui o contêiner de chave privada referenciado pelo objeto PrivateKey.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: Método PrivateKey. Delete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769276"
---
# <a name="privatekeydelete-method"></a><span data-ttu-id="05367-103">Método PrivateKey. Delete</span><span class="sxs-lookup"><span data-stu-id="05367-103">PrivateKey.Delete method</span></span>

<span data-ttu-id="05367-104">\[O método **delete** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="05367-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="05367-105">Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="05367-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="05367-106">O método **delete** exclui o contêiner de chave privada referenciado pelo objeto [**PrivateKey**](privatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="05367-106">The **Delete** method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="05367-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05367-107">Syntax</span></span>


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a><span data-ttu-id="05367-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05367-108">Parameters</span></span>

<span data-ttu-id="05367-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="05367-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05367-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05367-110">Return value</span></span>

<span data-ttu-id="05367-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="05367-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05367-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="05367-112">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05367-113">Esse método exclui o contêiner de chave privada referenciado pelo objeto [**PrivateKey**](privatekey.md) , bem como todas as chaves privadas no contêiner.</span><span class="sxs-lookup"><span data-stu-id="05367-113">This method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object as well as all private keys in the container.</span></span> <span data-ttu-id="05367-114">Qualquer coisa criptografada usando as chaves públicas correspondentes às chaves privadas excluídas não poderá mais ser descriptografada.</span><span class="sxs-lookup"><span data-stu-id="05367-114">Anything encrypted using the public keys corresponding to the deleted private keys will no longer be able to be decrypted.</span></span>

 

<span data-ttu-id="05367-115">Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="05367-115">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="05367-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05367-116">Requirements</span></span>



| <span data-ttu-id="05367-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05367-117">Requirement</span></span> | <span data-ttu-id="05367-118">Valor</span><span class="sxs-lookup"><span data-stu-id="05367-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05367-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="05367-119">Redistributable</span></span><br/> | <span data-ttu-id="05367-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="05367-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="05367-121">DLL</span><span class="sxs-lookup"><span data-stu-id="05367-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="05367-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05367-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
