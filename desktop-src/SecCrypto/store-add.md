---
description: Adiciona um objeto de certificado a um repositório de certificados aberto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Método Store. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768427"
---
# <a name="storeadd-method"></a><span data-ttu-id="ad2b3-103">Método Store. Add</span><span class="sxs-lookup"><span data-stu-id="ad2b3-103">Store.Add method</span></span>

<span data-ttu-id="ad2b3-104">\[O método **Add** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ad2b3-105">Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ad2b3-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ad2b3-106">O método **Add** adiciona um objeto de [**certificado**](certificate.md) a um [*repositório de certificados*](../secgloss/c-gly.md)aberto.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-106">The **Add** method adds a [**Certificate**](certificate.md) object to an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="ad2b3-107">Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-107">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2b3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad2b3-108">Syntax</span></span>


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="ad2b3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad2b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad2b3-110">*Certificado* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ad2b3-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2b3-111">Expressão que resolve para um objeto de [**certificado**](certificate.md) a ser adicionado ao repositório.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-111">Expression that resolves to a [**Certificate**](certificate.md) object to be added to the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad2b3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad2b3-112">Return value</span></span>

<span data-ttu-id="ad2b3-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad2b3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad2b3-114">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad2b3-115">Quando esse método é chamado em um repositório de sistema de um script da Web, o script precisa acessar certificados digitais no computador local.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-115">When this method is called on a system store from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="ad2b3-116">Se você permitir que o script acesse seus certificados digitais, o site do qual o script é executado também obterá acesso a todas as informações pessoais armazenadas nos certificados.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-116">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="ad2b3-117">Na primeira vez que esse método é chamado de um domínio específico, uma caixa de diálogo é gerada na qual o usuário deve indicar se o acesso aos certificados deve ser permitido.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-117">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="ad2b3-118">Se o repositório não estiver aberto no modo de leitura/gravação, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-118">If the store is not open in read/write mode, this method fails.</span></span> <span data-ttu-id="ad2b3-119">Embora esse método possa ser usado com armazenamentos de memória, as alterações feitas em um repositório de memória não são mantidas quando o armazenamento é fechado.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-119">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

<span data-ttu-id="ad2b3-120">Se o certificado que está sendo adicionado ao repositório for o mesmo que já existe, o método **Add** excluirá o certificado existente da loja e, em seguida, adicionará o novo certificado.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-120">If the certificate being added to the store is the same as one that is already there, the **Add** method deletes the existing certificate from the store and then adds the new certificate.</span></span> <span data-ttu-id="ad2b3-121">O novo certificado herda as propriedades do certificado existente.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-121">The new certificate inherits properties from the existing certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad2b3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad2b3-122">Requirements</span></span>



| <span data-ttu-id="ad2b3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad2b3-123">Requirement</span></span> | <span data-ttu-id="ad2b3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ad2b3-124">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2b3-125">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ad2b3-125">Redistributable</span></span><br/> | <span data-ttu-id="ad2b3-126">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ad2b3-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ad2b3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ad2b3-127">DLL</span></span><br/>             | <dl> <span data-ttu-id="ad2b3-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad2b3-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad2b3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad2b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2b3-130">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="ad2b3-130">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="ad2b3-131">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="ad2b3-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
