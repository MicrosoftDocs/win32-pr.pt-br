---
description: A propriedade PrimaryKeys do objeto Database retorna um objeto Record contendo o nome da tabela no campo 0 e os nomes de coluna (que compreendem as chaves primárias) em campos com sucesso correspondentes aos seus números de coluna.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Propriedade Database. PrimaryKeys
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758961"
---
# <a name="databaseprimarykeys-property"></a><span data-ttu-id="fd50d-103">Propriedade Database. PrimaryKeys</span><span class="sxs-lookup"><span data-stu-id="fd50d-103">Database.PrimaryKeys property</span></span>

<span data-ttu-id="fd50d-104">A propriedade **primarykeys** do objeto [**Database**](database-object.md) retorna um objeto [**Record**](record-object.md) contendo o nome da tabela no campo 0 e os nomes de coluna (que compreendem as chaves primárias) em campos com sucesso correspondentes aos seus números de coluna.</span><span class="sxs-lookup"><span data-stu-id="fd50d-104">The **PrimaryKeys** property of the [**Database**](database-object.md) object returns a [**Record**](record-object.md) object containing the table name in field 0 and the column names (comprising the primary keys) in succeeding fields corresponding to their column numbers.</span></span> <span data-ttu-id="fd50d-105">A contagem de campos do registro é a contagem de colunas de chave primária.</span><span class="sxs-lookup"><span data-stu-id="fd50d-105">The field count of the record is the count of primary key columns.</span></span>

<span data-ttu-id="fd50d-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="fd50d-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd50d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd50d-107">Syntax</span></span>


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a><span data-ttu-id="fd50d-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fd50d-108">Property value</span></span>

<span data-ttu-id="fd50d-109">Nome necessário de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="fd50d-109">Required name of an existing table.</span></span> <span data-ttu-id="fd50d-110">Um erro será gerado se a tabela não existir.</span><span class="sxs-lookup"><span data-stu-id="fd50d-110">An error is generated if the table does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd50d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd50d-111">Remarks</span></span>

<span data-ttu-id="fd50d-112">A propriedade **primarykeys** não pode ser usada com a [ \_ tabela tabelas](-tables-table.md) ou com a [ \_ tabela Columns](-columns-table.md).</span><span class="sxs-lookup"><span data-stu-id="fd50d-112">The **PrimaryKeys** property cannot be used with the [\_Tables table](-tables-table.md) or the [\_Columns table](-columns-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd50d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd50d-113">Requirements</span></span>



| <span data-ttu-id="fd50d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd50d-114">Requirement</span></span> | <span data-ttu-id="fd50d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fd50d-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd50d-116">Versão</span><span class="sxs-lookup"><span data-stu-id="fd50d-116">Version</span></span><br/> | <span data-ttu-id="fd50d-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fd50d-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fd50d-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fd50d-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fd50d-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="fd50d-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fd50d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fd50d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd50d-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd50d-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fd50d-122">IID</span><span class="sxs-lookup"><span data-stu-id="fd50d-122">IID</span></span><br/>     | <span data-ttu-id="fd50d-123">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fd50d-123">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




