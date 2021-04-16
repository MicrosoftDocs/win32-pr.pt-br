---
description: O método de importação copia para um certificado aberto armazena o conteúdo de um repositório de certificados exportado anteriormente. Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Método Store. Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747232"
---
# <a name="storeimport-method"></a><span data-ttu-id="fab02-104">Método Store. Import</span><span class="sxs-lookup"><span data-stu-id="fab02-104">Store.Import method</span></span>

<span data-ttu-id="fab02-105">\[O método de **importação** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="fab02-105">\[The **Import** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fab02-106">Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fab02-106">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fab02-107">O método de **importação** copia para um [*certificado aberto armazena*](../secgloss/c-gly.md) o conteúdo de um repositório de certificados exportado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fab02-107">The **Import** method copies into an open [*certificate store*](../secgloss/c-gly.md) the contents of a previously exported certificate store.</span></span> <span data-ttu-id="fab02-108">Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fab02-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab02-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fab02-109">Syntax</span></span>


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a><span data-ttu-id="fab02-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fab02-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab02-111">*EncodedStore* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fab02-111">*EncodedStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab02-112">A cadeia de caracteres que contém os certificados codificados a serem importados.</span><span class="sxs-lookup"><span data-stu-id="fab02-112">The string that contains the encoded certificates to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab02-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fab02-113">Return value</span></span>

<span data-ttu-id="fab02-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fab02-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fab02-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fab02-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fab02-116">Quando esse método é chamado de um script da Web, o script precisa acessar certificados digitais no computador local.</span><span class="sxs-lookup"><span data-stu-id="fab02-116">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="fab02-117">Se você permitir que o script acesse seus certificados digitais, o site do qual o script é executado também obterá acesso a todas as informações pessoais armazenadas nos certificados.</span><span class="sxs-lookup"><span data-stu-id="fab02-117">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="fab02-118">Na primeira vez que esse método é chamado de um domínio específico, uma caixa de diálogo é gerada na qual o usuário deve indicar se o acesso aos certificados deve ser permitido.</span><span class="sxs-lookup"><span data-stu-id="fab02-118">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="fab02-119">Se o repositório não estiver aberto com permissão de leitura/gravação, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="fab02-119">If the store is not opened with read/write permission, this method fails.</span></span> <span data-ttu-id="fab02-120">Embora esse método possa ser usado com armazenamentos de memória, as alterações feitas em um repositório de memória não são mantidas quando o armazenamento é fechado.</span><span class="sxs-lookup"><span data-stu-id="fab02-120">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab02-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab02-121">Requirements</span></span>



| <span data-ttu-id="fab02-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab02-122">Requirement</span></span> | <span data-ttu-id="fab02-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fab02-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fab02-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="fab02-124">Redistributable</span></span><br/> | <span data-ttu-id="fab02-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="fab02-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fab02-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fab02-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="fab02-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fab02-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab02-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fab02-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab02-129">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="fab02-129">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="fab02-130">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="fab02-130">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
