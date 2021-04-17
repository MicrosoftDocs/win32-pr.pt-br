---
description: Usado para configurar componentes CAPICOM.
title: Objeto de configurações
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762010"
---
# <a name="settings-object-cryptography"></a><span data-ttu-id="172d0-103">Objeto Settings (criptografia)</span><span class="sxs-lookup"><span data-stu-id="172d0-103">Settings object (Cryptography)</span></span>

<span data-ttu-id="172d0-104">\[O objeto de **configurações** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="172d0-104">\[The **Settings** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="172d0-105">O objeto **Settings** é usado para configurar os componentes CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="172d0-105">The **Settings** object is used to configure CAPICOM components.</span></span>

## <a name="members"></a><span data-ttu-id="172d0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="172d0-106">Members</span></span>

<span data-ttu-id="172d0-107">O objeto de **configurações** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="172d0-107">The **Settings** object has these types of members:</span></span>

-   [<span data-ttu-id="172d0-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="172d0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="172d0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="172d0-109">Properties</span></span>

<span data-ttu-id="172d0-110">O objeto **Settings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="172d0-110">The **Settings** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="172d0-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="172d0-111">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="172d0-112">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="172d0-112">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="172d0-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="172d0-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="172d0-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="172d0-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="172d0-115">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="172d0-115">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="172d0-116">Define ou recupera o local de pesquisa do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="172d0-116">Sets or retrieves the Active Directory search location.</span></span> <span data-ttu-id="172d0-117">O local inicial não é especificado por padrão.</span><span class="sxs-lookup"><span data-stu-id="172d0-117">The initial location is unspecified by default.</span></span> <span data-ttu-id="172d0-118">Quando o local não é especificado, o catálogo global é pesquisado e, em seguida, o domínio padrão é pesquisado.</span><span class="sxs-lookup"><span data-stu-id="172d0-118">When the location is unspecified, the global catalog is searched, then the default domain is searched.</span></span> <span data-ttu-id="172d0-119">A pesquisa determina se o atributo de certificado do usuário é publicado nesse local.</span><span class="sxs-lookup"><span data-stu-id="172d0-119">The search determines whether the user certificate attribute is published at that location.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="172d0-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="172d0-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="172d0-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="172d0-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="172d0-122">Define ou recupera um valor booliano que indica se os prompts de interface do usuário para uma identidade de signatário ou remetente podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="172d0-122">Sets or retrieves a Boolean value that indicates whether user interface prompts for a signer or sender's identity can be used.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="172d0-123">Definir essa propriedade não desabilita os avisos gerados antes de qualquer uso de chave privada ser feito de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="172d0-123">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="172d0-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="172d0-124">Remarks</span></span>

<span data-ttu-id="172d0-125">O objeto de **configurações** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="172d0-125">The **Settings** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="172d0-126">O ProgID do objeto de **configurações** é CAPICOM. Configurações. 1.</span><span class="sxs-lookup"><span data-stu-id="172d0-126">The ProgID for the **Settings** object is CAPICOM.Settings.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="172d0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="172d0-127">Requirements</span></span>



| <span data-ttu-id="172d0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="172d0-128">Requirement</span></span> | <span data-ttu-id="172d0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="172d0-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="172d0-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="172d0-130">Redistributable</span></span><br/> | <span data-ttu-id="172d0-131">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="172d0-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="172d0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="172d0-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="172d0-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="172d0-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="172d0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="172d0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="172d0-135">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="172d0-135">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 




