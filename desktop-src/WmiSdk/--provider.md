---
description: Serve como a classe pai para a \_ \_ classe do sistema Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: Classe __Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791427"
---
# <a name="__provider-class"></a><span data-ttu-id="77ad9-103">\_\_Classe de provedor</span><span class="sxs-lookup"><span data-stu-id="77ad9-103">\_\_Provider class</span></span>

<span data-ttu-id="77ad9-104">A classe de sistema do **\_ \_ provedor** é uma classe base abstrata que serve como a classe pai para a classe do sistema [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="77ad9-104">The **\_\_Provider** system class is an abstract base class that serves as the parent class for the [**\_\_Win32Provider**](--win32provider.md) system class.</span></span>

<span data-ttu-id="77ad9-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="77ad9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="77ad9-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="77ad9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ad9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77ad9-107">Syntax</span></span>

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="77ad9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="77ad9-108">Members</span></span>

<span data-ttu-id="77ad9-109">A classe **\_ \_ Provider** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="77ad9-109">The **\_\_Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="77ad9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="77ad9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77ad9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="77ad9-111">Properties</span></span>

<span data-ttu-id="77ad9-112">A classe **\_ \_ Provider** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="77ad9-112">The **\_\_Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77ad9-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="77ad9-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ad9-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ad9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ad9-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="77ad9-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77ad9-116">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="77ad9-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="77ad9-117">Cadeia de caracteres neutra de idioma que identifica exclusivamente o provedor.</span><span class="sxs-lookup"><span data-stu-id="77ad9-117">Language-neutral string that uniquely identifies the provider.</span></span> <span data-ttu-id="77ad9-118">O seguinte formato é sugerido para evitar conflitos de nomenclatura:</span><span class="sxs-lookup"><span data-stu-id="77ad9-118">The following format is suggested to prevent naming conflicts:</span></span>

<span data-ttu-id="77ad9-119">\|versão do provedor de fornecedor \|</span><span class="sxs-lookup"><span data-stu-id="77ad9-119">vendor\|provider\|version</span></span>

<span data-ttu-id="77ad9-120">Por exemplo, esse nome de provedor representa a versão 1,0 do Microsoft Testprovider:</span><span class="sxs-lookup"><span data-stu-id="77ad9-120">For example, this provider name represents version 1.0 of the Microsoft TestProvider:</span></span>

<span data-ttu-id="77ad9-121">"Microsoft \| testprovider \| v 1.0"</span><span class="sxs-lookup"><span data-stu-id="77ad9-121">"Microsoft\|TestProvider\|V1.0"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77ad9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="77ad9-122">Remarks</span></span>

<span data-ttu-id="77ad9-123">A classe de **\_ \_ provedor** é derivada de [**\_ \_ SystemClass**](--systemclass.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="77ad9-123">The **\_\_Provider** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="77ad9-124">Os provedores criam instâncias [**\_ \_ Win32Provider**](--win32provider.md) para especificar informações sobre sua implementação física.</span><span class="sxs-lookup"><span data-stu-id="77ad9-124">Providers create [**\_\_Win32Provider**](--win32provider.md) instances to specify information about their physical implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ad9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ad9-125">Requirements</span></span>



| <span data-ttu-id="77ad9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ad9-126">Requirement</span></span> | <span data-ttu-id="77ad9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="77ad9-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="77ad9-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ad9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="77ad9-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77ad9-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="77ad9-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ad9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="77ad9-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77ad9-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="77ad9-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="77ad9-132">Namespace</span></span><br/>                | <span data-ttu-id="77ad9-133">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="77ad9-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="77ad9-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="77ad9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ad9-135">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="77ad9-135">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="77ad9-136">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="77ad9-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="77ad9-137">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="77ad9-137">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

