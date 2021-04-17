---
title: Método Modify da classe MicrosoftDNS_AFSDBType
description: O método Modify atualiza um registro de recurso do servidor de banco de dados Andrew File System (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_AFSDBType classe
- MicrosoftDNS_AFSDBType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753558"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="ac07b-106">Método Modify da classe MicrosoftDNS \_ AFSDBType</span><span class="sxs-lookup"><span data-stu-id="ac07b-106">Modify method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="ac07b-107">O método **Modify** atualiza um registro de recurso do servidor de banco de dados Andrew File System (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="ac07b-107">The **Modify** method updates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac07b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac07b-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ac07b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac07b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac07b-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ac07b-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07b-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="ac07b-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ac07b-112">*Subtipo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ac07b-112">*Subtype* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07b-113">Subtipo do servidor host AFS.</span><span class="sxs-lookup"><span data-stu-id="ac07b-113">Subtype of the host AFS server.</span></span> <span data-ttu-id="ac07b-114">Para o subtipo 1 (valor = 1), o host tem um servidor de local de volume AFS versão 3,0 para a célula AFS nomeada.</span><span class="sxs-lookup"><span data-stu-id="ac07b-114">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="ac07b-115">No caso do subtipo 2 (valor = 2), o host tem um servidor de nomes autenticado que contém o nó do diretório raiz da célula para a célula de DCE/NCA nomeada.</span><span class="sxs-lookup"><span data-stu-id="ac07b-115">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="ac07b-116">*Nome do Server* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ac07b-116">*ServerName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07b-117">FQDN que especifica um host que tem um servidor para a célula AFS especificada no nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="ac07b-117">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="ac07b-118">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="ac07b-118">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07b-119">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="ac07b-119">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac07b-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac07b-120">Return value</span></span>

<span data-ttu-id="ac07b-121">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ac07b-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac07b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac07b-122">Remarks</span></span>

<span data-ttu-id="ac07b-123">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="ac07b-123">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac07b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac07b-124">Requirements</span></span>



| <span data-ttu-id="ac07b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac07b-125">Requirement</span></span> | <span data-ttu-id="ac07b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ac07b-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac07b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac07b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ac07b-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ac07b-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ac07b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac07b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ac07b-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ac07b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ac07b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac07b-131">Namespace</span></span><br/>                | <span data-ttu-id="ac07b-132">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ac07b-132">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ac07b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ac07b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac07b-134"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac07b-134"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac07b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac07b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac07b-136">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="ac07b-136">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="ac07b-137">**Método CreateInstanceFromPropertyData da \_ classe AFSDBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ac07b-137">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ac07b-138">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ac07b-138">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





