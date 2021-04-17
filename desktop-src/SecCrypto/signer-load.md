---
description: Carrega um certificado de autenticação de um arquivo. pfx especificado.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Método signatário. Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769270"
---
# <a name="signerload-method"></a><span data-ttu-id="ed9fa-103">Método signatário. Load</span><span class="sxs-lookup"><span data-stu-id="ed9fa-103">Signer.Load method</span></span>

<span data-ttu-id="ed9fa-104">\[O método **Load** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ed9fa-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ed9fa-105">Em vez disso, use a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="ed9fa-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ed9fa-106">O método **Load** carrega um certificado de autenticação de um arquivo. pfx especificado.</span><span class="sxs-lookup"><span data-stu-id="ed9fa-106">The **Load** method loads a signing certificate from a specified .pfx file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed9fa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed9fa-107">Syntax</span></span>


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ed9fa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed9fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed9fa-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="ed9fa-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9fa-110">Nome do arquivo. pfx que contém o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ed9fa-110">Name of the .pfx file that contains the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="ed9fa-111">*Senha* \[ do adicional\]</span><span class="sxs-lookup"><span data-stu-id="ed9fa-111">*Password* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ed9fa-112">Cadeia de caracteres que contém a senha de texto não criptografado usada para abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ed9fa-112">String containing the plaintext password used to open the file.</span></span> <span data-ttu-id="ed9fa-113">Até 32 caracteres Unicode, incluindo um caractere nulo de terminação, podem ser usados para a senha.</span><span class="sxs-lookup"><span data-stu-id="ed9fa-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="ed9fa-114">O valor padrão é uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="ed9fa-114">The default value is an empty string ("").</span></span> <span data-ttu-id="ed9fa-115">Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="ed9fa-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed9fa-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed9fa-116">Return value</span></span>

<span data-ttu-id="ed9fa-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ed9fa-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed9fa-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed9fa-118">Remarks</span></span>

<span data-ttu-id="ed9fa-119">Esse método carrega o primeiro certificado no arquivo. pfx que tem uma chave privada associada a ele.</span><span class="sxs-lookup"><span data-stu-id="ed9fa-119">This method loads the first certificate in the .pfx file that has a private key associated with it.</span></span>

<span data-ttu-id="ed9fa-120">Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="ed9fa-120">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed9fa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed9fa-121">Requirements</span></span>



| <span data-ttu-id="ed9fa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed9fa-122">Requirement</span></span> | <span data-ttu-id="ed9fa-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ed9fa-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9fa-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ed9fa-124">Redistributable</span></span><br/> | <span data-ttu-id="ed9fa-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed9fa-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ed9fa-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ed9fa-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="ed9fa-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed9fa-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed9fa-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed9fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed9fa-129">**Signatário**</span><span class="sxs-lookup"><span data-stu-id="ed9fa-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
