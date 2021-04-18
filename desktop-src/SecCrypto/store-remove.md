---
description: O método remove remove um certificado de um repositório de certificados aberto. Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Método Store. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753211"
---
# <a name="storeremove-method"></a><span data-ttu-id="d7eb5-104">Método Store. Remove</span><span class="sxs-lookup"><span data-stu-id="d7eb5-104">Store.Remove method</span></span>

<span data-ttu-id="d7eb5-105">\[O método **Remove** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-105">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d7eb5-106">Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d7eb5-106">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d7eb5-107">O método **Remove** remove um [*certificado*](../secgloss/c-gly.md) de um [*repositório de certificados*](../secgloss/c-gly.md)aberto.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-107">The **Remove** method removes a [*certificate*](../secgloss/c-gly.md) from an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="d7eb5-108">Esse método só pode ser usado com um repositório que tenha sido aberto com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7eb5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7eb5-109">Syntax</span></span>


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="d7eb5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7eb5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7eb5-111">*Certificado* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d7eb5-111">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb5-112">Expressão que resolve para uma instância de um objeto de [**certificado**](certificate.md) a ser removido do repositório.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-112">Expression that resolves to an instance of a [**Certificate**](certificate.md) object to be removed from the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7eb5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7eb5-113">Return value</span></span>

<span data-ttu-id="d7eb5-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7eb5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7eb5-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7eb5-116">Quando esse método é chamado de um script da Web, o script precisa excluir certificados digitais do computador local.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-116">When this method is called from a web script, the script needs to delete digital certificates from the local computer.</span></span> <span data-ttu-id="d7eb5-117">Permitir que sites não confiáveis exclua certificados digitais é um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-117">Allowing untrusted websites to delete digital certificates is a security risk.</span></span> <span data-ttu-id="d7eb5-118">Uma caixa de diálogo que pergunta se o site pode excluir certificados é exibida quando esse método é chamado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-118">A dialog box that asks whether the website can delete certificates appears when this method is first called.</span></span> <span data-ttu-id="d7eb5-119">Se você permitir que o aplicativo exclua certificados e selecionar "não mostrar esta caixa de diálogo novamente", a caixa de diálogo não aparecerá mais para nenhum script que exclua certificados dentro desse domínio.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-119">If you allow the application to delete certificates and select "Do not show this dialog box again," the dialog box will no longer appear for any script that deletes certificates within that domain.</span></span> <span data-ttu-id="d7eb5-120">No entanto, os scripts fora desse domínio que tentarem excluir certificados ainda farão com que essa caixa de diálogo seja exibida.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-120">However, scripts outside that domain that attempt to delete certificates will still cause this dialog box to appear.</span></span> <span data-ttu-id="d7eb5-121">Se você não permitir que o script exclua certificados e selecionar "não mostrar esta caixa de diálogo novamente", os scripts nesse domínio serão recusados automaticamente na capacidade de excluir certificados.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-121">If you do not allow the script to delete certificates and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to delete certificates.</span></span>

 

<span data-ttu-id="d7eb5-122">Ao excluir um certificado de um repositório, primeiro exclua a chave privada associada ao certificado.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-122">When you delete a certificate from a store, you should first delete the private key associated with the certificate.</span></span>

<span data-ttu-id="d7eb5-123">Se o armazenamento não estiver aberto com permissão de leitura/gravação, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-123">If the store is not open with read/write permission, this method fails.</span></span> <span data-ttu-id="d7eb5-124">Embora esse método possa ser usado com armazenamentos de memória, as alterações feitas em um repositório de memória não são mantidas quando o armazenamento é fechado.</span><span class="sxs-lookup"><span data-stu-id="d7eb5-124">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7eb5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7eb5-125">Requirements</span></span>



| <span data-ttu-id="d7eb5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7eb5-126">Requirement</span></span> | <span data-ttu-id="d7eb5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d7eb5-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7eb5-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d7eb5-128">Redistributable</span></span><br/> | <span data-ttu-id="d7eb5-129">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7eb5-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d7eb5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d7eb5-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="d7eb5-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb5-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7eb5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7eb5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7eb5-133">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="d7eb5-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="d7eb5-134">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="d7eb5-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
