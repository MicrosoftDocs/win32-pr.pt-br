---
description: A propriedade DatabaseState do objeto de banco de dados é uma propriedade somente leitura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Propriedade Database. DatabaseState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747555"
---
# <a name="databasedatabasestate-property"></a><span data-ttu-id="3e625-103">Propriedade Database. DatabaseState</span><span class="sxs-lookup"><span data-stu-id="3e625-103">Database.DatabaseState property</span></span>

<span data-ttu-id="3e625-104">A propriedade **DatabaseState** do objeto de [**banco de dados**](database-object.md) é uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3e625-104">The **DatabaseState** property of the [**Database**](database-object.md) object is a read-only property.</span></span>

<span data-ttu-id="3e625-105">Essa propriedade retorna o estado de persistência do banco de dados como um dos parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e625-105">This property returns the persistence state of the database as one of the following parameters.</span></span>



| <span data-ttu-id="3e625-106">Estado do banco de dados</span><span class="sxs-lookup"><span data-stu-id="3e625-106">Database state</span></span>        | <span data-ttu-id="3e625-107">Valor</span><span class="sxs-lookup"><span data-stu-id="3e625-107">Value</span></span> | <span data-ttu-id="3e625-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e625-108">Description</span></span>                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e625-109">msiDatabaseStateRead</span><span class="sxs-lookup"><span data-stu-id="3e625-109">msiDatabaseStateRead</span></span>  | <span data-ttu-id="3e625-110">0</span><span class="sxs-lookup"><span data-stu-id="3e625-110">0</span></span>     | <span data-ttu-id="3e625-111">O banco de dados é aberto como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3e625-111">Database opens as read-only.</span></span> <span data-ttu-id="3e625-112">As alterações nos dados persistentes não são permitidas e os dados temporários não são salvos.</span><span class="sxs-lookup"><span data-stu-id="3e625-112">Changes to persistent data are not permitted and temporary data is not saved.</span></span> |
| <span data-ttu-id="3e625-113">msiDatabaseStateWrite</span><span class="sxs-lookup"><span data-stu-id="3e625-113">msiDatabaseStateWrite</span></span> | <span data-ttu-id="3e625-114">1</span><span class="sxs-lookup"><span data-stu-id="3e625-114">1</span></span>     | <span data-ttu-id="3e625-115">O banco de dados está totalmente operacional para leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="3e625-115">Database is fully operational for read and write.</span></span>                                                          |



 

<span data-ttu-id="3e625-116">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3e625-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e625-117">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e625-117">Syntax</span></span>


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a><span data-ttu-id="3e625-118">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3e625-118">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="3e625-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e625-119">Requirements</span></span>



| <span data-ttu-id="3e625-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e625-120">Requirement</span></span> | <span data-ttu-id="3e625-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3e625-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e625-122">Versão</span><span class="sxs-lookup"><span data-stu-id="3e625-122">Version</span></span><br/> | <span data-ttu-id="3e625-123">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3e625-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3e625-124">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3e625-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3e625-125">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e625-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3e625-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3e625-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3e625-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e625-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3e625-128">IID</span><span class="sxs-lookup"><span data-stu-id="3e625-128">IID</span></span><br/>     | <span data-ttu-id="3e625-129">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3e625-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




