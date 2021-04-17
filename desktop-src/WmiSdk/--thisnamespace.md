---
description: Mantém os direitos de segurança do namespace na forma de um descritor de segurança.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: classe __thisNAMESPACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759926"
---
# <a name="__thisnamespace-class"></a><span data-ttu-id="7d4e7-103">\_\_classe thisNAMESPACE</span><span class="sxs-lookup"><span data-stu-id="7d4e7-103">\_\_thisNAMESPACE class</span></span>

<span data-ttu-id="7d4e7-104">A classe de sistema **\_ \_ thisNamespace** mantém os direitos de segurança para o namespace na forma de um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-104">The **\_\_thisNAMESPACE** system class holds the security rights for the namespace in the form of a security descriptor.</span></span> <span data-ttu-id="7d4e7-105">Essa classe e uma única instância são encontradas em todos os namespaces.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-105">This class and a single instance is found in all namespaces.</span></span>

<span data-ttu-id="7d4e7-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7d4e7-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d4e7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d4e7-108">Syntax</span></span>

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a><span data-ttu-id="7d4e7-109">Membros</span><span class="sxs-lookup"><span data-stu-id="7d4e7-109">Members</span></span>

<span data-ttu-id="7d4e7-110">A classe **\_ \_ thisNamespace** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7d4e7-110">The **\_\_thisNAMESPACE** class has these types of members:</span></span>

-   [<span data-ttu-id="7d4e7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7d4e7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d4e7-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7d4e7-112">Properties</span></span>

<span data-ttu-id="7d4e7-113">A classe **\_ \_ thisNamespace** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-113">The **\_\_thisNAMESPACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d4e7-114">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="7d4e7-114">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d4e7-115">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="7d4e7-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7d4e7-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d4e7-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d4e7-117">Descritor de segurança que descreve quem pode acessar o namespace e quem pode ler ou gravar no namespace.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-117">Security descriptor describing who can access the namespace and who can read from or write to the namespace.</span></span> <span data-ttu-id="7d4e7-118">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="7d4e7-118">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="7d4e7-119">Para obter mais informações sobre o formato dos descritores de segurança, consulte [descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors) na seção segurança do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-119">For more information about the format of security descriptors, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors) in the Security section of the Windows SDK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d4e7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d4e7-120">Remarks</span></span>

<span data-ttu-id="7d4e7-121">A instância singleton de **\_ \_ thisNamespace** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-121">The singleton instance of **\_\_thisNAMESPACE** is read-only.</span></span> <span data-ttu-id="7d4e7-122">Para alterar as configurações da propriedade descritor de segurança, use os métodos da classe [**\_ \_ SystemSecurity**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="7d4e7-122">To change the settings of the security descriptor property, use the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span> <span data-ttu-id="7d4e7-123">A classe **\_ \_ thisNamespace** deriva de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="7d4e7-123">The **\_\_thisNAMESPACE** class derives from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d4e7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d4e7-124">Requirements</span></span>



| <span data-ttu-id="7d4e7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d4e7-125">Requirement</span></span> | <span data-ttu-id="7d4e7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7d4e7-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7d4e7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d4e7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7d4e7-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d4e7-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7d4e7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d4e7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7d4e7-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d4e7-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7d4e7-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d4e7-131">Namespace</span></span><br/>                | <span data-ttu-id="7d4e7-132">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="7d4e7-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7d4e7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d4e7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d4e7-134">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="7d4e7-134">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="7d4e7-135">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="7d4e7-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

