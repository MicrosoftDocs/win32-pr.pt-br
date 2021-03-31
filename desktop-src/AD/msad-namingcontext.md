---
title: Classe MSAD_NamingContext
description: Representa um NC (contexto de nomenclatura) específico no controlador de domínio.
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- Classe de MSAD_NamingContext Active Directory
- Active Directory de MSAD_NamingContext classe, descrita
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68f70c6e40e823df0a6827e1114f40dae7937be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644671"
---
# <a name="msad_namingcontext-class"></a><span data-ttu-id="c7475-105">\_Classe MSAD NamingContext</span><span class="sxs-lookup"><span data-stu-id="c7475-105">MSAD\_NamingContext class</span></span>

<span data-ttu-id="c7475-106">Representa um NC (contexto de nomenclatura) específico no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c7475-106">Represents a particular naming context (NC) on the domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7475-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7475-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="c7475-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c7475-108">Members</span></span>

<span data-ttu-id="c7475-109">A classe **MSAD \_ NamingContext** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7475-109">The **MSAD\_NamingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="c7475-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7475-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7475-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7475-111">Properties</span></span>

<span data-ttu-id="c7475-112">A classe **MSAD \_ NamingContext** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c7475-112">The **MSAD\_NamingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7475-113">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="c7475-113">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7475-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7475-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c7475-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7475-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7475-116">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c7475-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c7475-117">Obtém o caminho X. 500 do NC.</span><span class="sxs-lookup"><span data-stu-id="c7475-117">Gets the X.500 path of the NC.</span></span>

</dd> <dt>

<span data-ttu-id="c7475-118">**IsFullReplica**</span><span class="sxs-lookup"><span data-stu-id="c7475-118">**IsFullReplica**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7475-119">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7475-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7475-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7475-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7475-121">Obtém o valor que indica se o NC é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c7475-121">Gets the value that indicates whether the NC is read/write.</span></span> <span data-ttu-id="c7475-122">**True** se o NC for de leitura/gravação; **False** se o NC for somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c7475-122">**TRUE** if the NC is read/write; **FALSE** if the NC is read-only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7475-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7475-123">Requirements</span></span>



| <span data-ttu-id="c7475-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7475-124">Requirement</span></span> | <span data-ttu-id="c7475-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c7475-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7475-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7475-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c7475-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c7475-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7475-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7475-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c7475-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7475-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7475-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7475-130">Namespace</span></span><br/>                | <span data-ttu-id="c7475-131">\\MicrosoftActiveDirectory raiz</span><span class="sxs-lookup"><span data-stu-id="c7475-131">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="c7475-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c7475-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7475-133"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7475-133"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7475-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c7475-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7475-135"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7475-135"><dt>Replprov.dll</dt></span></span> </dl> |



 

