---
description: A propriedade ComponentClients somente leitura retorna um objeto StringList que enumera o conjunto de clientes de um componente especificado.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Propriedade Installer. ComponentClients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748983"
---
# <a name="installercomponentclients-property"></a><span data-ttu-id="e08b7-103">Propriedade Installer. ComponentClients</span><span class="sxs-lookup"><span data-stu-id="e08b7-103">Installer.ComponentClients property</span></span>

<span data-ttu-id="e08b7-104">A propriedade **ComponentClients** somente leitura retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de clientes de um componente especificado.</span><span class="sxs-lookup"><span data-stu-id="e08b7-104">The read-only **ComponentClients** property returns a [**StringList**](stringlist-object.md) object enumerating the set of clients of a specified component.</span></span>

<span data-ttu-id="e08b7-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e08b7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08b7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e08b7-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a><span data-ttu-id="e08b7-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e08b7-107">Property value</span></span>

<span data-ttu-id="e08b7-108">Um GUID de cadeia de caracteres que representa o código do componente.</span><span class="sxs-lookup"><span data-stu-id="e08b7-108">A string GUID that represents the component code of the component.</span></span> <span data-ttu-id="e08b7-109">Os códigos de componente são especificados na coluna ComponentID da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e08b7-109">The component codes are specified in the ComponentId column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e08b7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e08b7-110">Remarks</span></span>

<span data-ttu-id="e08b7-111">Para enumerar os clientes do componente, um aplicativo pode iterar por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each.</span><span class="sxs-lookup"><span data-stu-id="e08b7-111">To enumerate the component clients, an application may iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="e08b7-112">Como os clientes não são ordenados, todos os componentes novos têm um índice arbitrário.</span><span class="sxs-lookup"><span data-stu-id="e08b7-112">Because clients are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="e08b7-113">Isso significa que a função pode retornar clientes em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="e08b7-113">This means that the function may return clients in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="e08b7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e08b7-114">Requirements</span></span>



| <span data-ttu-id="e08b7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e08b7-115">Requirement</span></span> | <span data-ttu-id="e08b7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e08b7-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08b7-117">Versão</span><span class="sxs-lookup"><span data-stu-id="e08b7-117">Version</span></span><br/> | <span data-ttu-id="e08b7-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e08b7-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e08b7-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e08b7-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e08b7-120">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e08b7-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e08b7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e08b7-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e08b7-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e08b7-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e08b7-123">IID</span><span class="sxs-lookup"><span data-stu-id="e08b7-123">IID</span></span><br/>     | <span data-ttu-id="e08b7-124">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e08b7-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e08b7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e08b7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08b7-126">**MsiEnumClients**</span><span class="sxs-lookup"><span data-stu-id="e08b7-126">**MsiEnumClients**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




