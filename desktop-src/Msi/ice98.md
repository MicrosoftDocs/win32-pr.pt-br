---
description: ICE98 verifica o campo de descrição da tabela ODBCDataSource para uma fonte de dados ODBC. Ele usa a função SQLValidDSN para verificar se somente caracteres válidos são usados e se a descrição não excede o comprimento máximo permitido.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170056"
---
# <a name="ice98"></a><span data-ttu-id="6cb57-104">ICE98</span><span class="sxs-lookup"><span data-stu-id="6cb57-104">ICE98</span></span>

<span data-ttu-id="6cb57-105">ICE98 verifica o campo de descrição da [tabela ODBCDataSource](odbcdatasource-table.md) para uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="6cb57-105">ICE98 verifies the description field of the [ODBCDataSource Table](odbcdatasource-table.md) for an ODBC data source.</span></span> <span data-ttu-id="6cb57-106">Ele usa a função **SQLValidDSN** para verificar se somente caracteres válidos são usados e se a descrição não excede o comprimento máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="6cb57-106">It uses the **SQLValidDSN** function to check that only valid characters are used, and that the description does not exceed the maximum allowed length.</span></span>

## <a name="result"></a><span data-ttu-id="6cb57-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="6cb57-107">Result</span></span>

<span data-ttu-id="6cb57-108">ICE98 posta os seguintes avisos.</span><span class="sxs-lookup"><span data-stu-id="6cb57-108">ICE98 posts the following warnings.</span></span>



| <span data-ttu-id="6cb57-109">Aviso de ICE98</span><span class="sxs-lookup"><span data-stu-id="6cb57-109">ICE98 warning</span></span>                    | <span data-ttu-id="6cb57-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cb57-110">Description</span></span>                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb57-111">O nome da fonte de dados é inválido.</span><span class="sxs-lookup"><span data-stu-id="6cb57-111">The data source name is invalid.</span></span> | <span data-ttu-id="6cb57-112">O valor na coluna Descrição da [tabela ODBCDataSource](odbcdatasource-table.md) contém caracteres inválidos ou é muito longo, o que significa que ele excede o \_ comprimento máximo \_ \_ de DSN do SQL de 32.</span><span class="sxs-lookup"><span data-stu-id="6cb57-112">The value in the Description column of the [ODBCDataSource Table](odbcdatasource-table.md) either contains invalid characters or is too long, which means that it exceeds the SQL\_MAX\_DSN\_LENGTH of 32.</span></span> |



 

## <a name="example"></a><span data-ttu-id="6cb57-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6cb57-113">Example</span></span>

<span data-ttu-id="6cb57-114">ICE98 relata os seguintes avisos para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="6cb57-114">ICE98 reports the following warnings for the example:</span></span>

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

<span data-ttu-id="6cb57-115">[Tabela ODBCDataSource](odbcdatasource-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6cb57-115">[ODBCDataSource Table](odbcdatasource-table.md) (partial)</span></span>



| <span data-ttu-id="6cb57-116">DataSource</span><span class="sxs-lookup"><span data-stu-id="6cb57-116">DataSource</span></span> | <span data-ttu-id="6cb57-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cb57-117">Description</span></span>                      |
|------------|----------------------------------|
| <span data-ttu-id="6cb57-118">BadChar</span><span class="sxs-lookup"><span data-stu-id="6cb57-118">BadChar</span></span>    | <span data-ttu-id="6cb57-119">!</span><span class="sxs-lookup"><span data-stu-id="6cb57-119">!</span></span>                                |
| <span data-ttu-id="6cb57-120">TooLong</span><span class="sxs-lookup"><span data-stu-id="6cb57-120">TooLong</span></span>    | <span data-ttu-id="6cb57-121"><String of length > 32></span><span class="sxs-lookup"><span data-stu-id="6cb57-121"><String of length > 32></span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6cb57-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cb57-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb57-123">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="6cb57-123">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="6cb57-124">Tabela ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="6cb57-124">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
</dt> </dl>

 

 



