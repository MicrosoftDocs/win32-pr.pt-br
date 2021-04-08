---
title: Classe MDM_Policy_Result01_Location02
description: A \_ classe MDM Policy \_ Result01 \_ Location02 Obtém as configurações do serviço de localização do dispositivo.
ms.assetid: f6d639db-c9d4-4d7e-b857-54aad602ea29
keywords:
- Classe MDM_Policy_Result01_Location02
- Classe MDM_Policy_Result01_Location02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Location02
- MDM_Policy_Result01_Location02.InstanceID
- MDM_Policy_Result01_Location02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 210fb38e45e600e45590acecb9c647d00ab13995
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824330"
---
# <a name="mdm_policy_result01_location02-class"></a><span data-ttu-id="97e53-105">\_Classe MDM \_ Result01 \_ Location02</span><span class="sxs-lookup"><span data-stu-id="97e53-105">MDM\_Policy\_Result01\_Location02 class</span></span>

<span data-ttu-id="97e53-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="97e53-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="97e53-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="97e53-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="97e53-108">A \_ classe MDM Policy \_ Result01 \_ Location02 Obtém as configurações do serviço de localização do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97e53-108">The MDM\_Policy\_Result01\_Location02 class gets the settings of the location service of the device.</span></span>

<span data-ttu-id="97e53-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="97e53-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e53-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97e53-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Location02
{
  string InstanceID;
  string ParentID;
  sint32 EnableLocation;
};
```

## <a name="members"></a><span data-ttu-id="97e53-111">Membros</span><span class="sxs-lookup"><span data-stu-id="97e53-111">Members</span></span>

<span data-ttu-id="97e53-112">A **classe \_ \_ Result01 \_ Location02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="97e53-112">The **MDM\_Policy\_Result01\_Location02** class has these types of members:</span></span>

-   [<span data-ttu-id="97e53-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="97e53-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97e53-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="97e53-114">Properties</span></span>

<span data-ttu-id="97e53-115">A **classe \_ \_ Result01 \_ Location02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="97e53-115">The **MDM\_Policy\_Result01\_Location02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97e53-116">**EnableLocation**</span><span class="sxs-lookup"><span data-stu-id="97e53-116">**EnableLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e53-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="97e53-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="97e53-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="97e53-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="97e53-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="97e53-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e53-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="97e53-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97e53-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="97e53-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97e53-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="97e53-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="97e53-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="97e53-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e53-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="97e53-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97e53-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="97e53-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97e53-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="97e53-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97e53-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97e53-127">Requirements</span></span>



| <span data-ttu-id="97e53-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e53-128">Requirement</span></span> | <span data-ttu-id="97e53-129">Valor</span><span class="sxs-lookup"><span data-stu-id="97e53-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97e53-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97e53-130">Minimum supported client</span></span><br/> | <span data-ttu-id="97e53-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="97e53-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="97e53-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97e53-132">Minimum supported server</span></span><br/> | <span data-ttu-id="97e53-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="97e53-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="97e53-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="97e53-134">Namespace</span></span><br/>                | <span data-ttu-id="97e53-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="97e53-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="97e53-136">MOF</span><span class="sxs-lookup"><span data-stu-id="97e53-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97e53-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97e53-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="97e53-138">DLL</span><span class="sxs-lookup"><span data-stu-id="97e53-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97e53-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97e53-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

