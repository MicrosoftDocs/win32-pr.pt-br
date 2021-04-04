---
description: O ICE66 usa as tabelas no banco de dados para determinar qual esquema seu banco de dados deve usar.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647528"
---
# <a name="ice66"></a><span data-ttu-id="030da-103">ICE66</span><span class="sxs-lookup"><span data-stu-id="030da-103">ICE66</span></span>

<span data-ttu-id="030da-104">O ICE66 usa as tabelas no banco de dados para determinar qual esquema seu banco de dados deve usar.</span><span class="sxs-lookup"><span data-stu-id="030da-104">ICE66 uses the tables in the database to determine which schema your database should use.</span></span>

<span data-ttu-id="030da-105">Algumas funcionalidades só poderão ser disponibilizadas se o pacote estiver instalado em um sistema com uma versão atual do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="030da-105">Some functionality may only be available if the package is installed on a system with a current Windows Installer version.</span></span>

## <a name="result"></a><span data-ttu-id="030da-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="030da-106">Result</span></span>

<span data-ttu-id="030da-107">ICE66 posta um aviso se o seu banco de dados estiver usando o esquema incorreto.</span><span class="sxs-lookup"><span data-stu-id="030da-107">ICE66 posts a warning if your database is using the wrong schema.</span></span>

## <a name="example"></a><span data-ttu-id="030da-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="030da-108">Example</span></span>

<span data-ttu-id="030da-109">ICE66 relata o seguinte aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="030da-109">ICE66 reports the following warning for the example shown.</span></span>

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

<span data-ttu-id="030da-110">Esse aviso poderá ser ignorado se você quiser que o pacote seja instalado usando uma versão de Windows Installer atual.</span><span class="sxs-lookup"><span data-stu-id="030da-110">This warning can be ignored if you want your package to be installed using a current Windows Installer version.</span></span> <span data-ttu-id="030da-111">Por exemplo, se você quiser que o pacote seja instalado somente na versão 2,0 ou posterior, altere o esquema do pacote (PID \_ PageCount) para 200.</span><span class="sxs-lookup"><span data-stu-id="030da-111">For example, if you want your package to be installable only on version 2.0 or later, change your package schema (PID\_PAGECOUNT) to 200.</span></span>

[<span data-ttu-id="030da-112">Tabela IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="030da-112">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="030da-113">Componente \_ compartilhado</span><span class="sxs-lookup"><span data-stu-id="030da-113">Component\_Shared</span></span> | <span data-ttu-id="030da-114">Aplicativo de componente \_</span><span class="sxs-lookup"><span data-stu-id="030da-114">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="030da-115">Component1</span><span class="sxs-lookup"><span data-stu-id="030da-115">Component1</span></span>        | <span data-ttu-id="030da-116">Component2</span><span class="sxs-lookup"><span data-stu-id="030da-116">Component2</span></span>             |



 

[<span data-ttu-id="030da-117">Fluxo de informações de resumo</span><span class="sxs-lookup"><span data-stu-id="030da-117">Summary Information Stream</span></span>](summary-information-stream.md)



| <span data-ttu-id="030da-118">PIDt</span><span class="sxs-lookup"><span data-stu-id="030da-118">PIDt</span></span>           | <span data-ttu-id="030da-119">Valor</span><span class="sxs-lookup"><span data-stu-id="030da-119">Value</span></span> |
|----------------|-------|
| <span data-ttu-id="030da-120">DTI \_ PageCount</span><span class="sxs-lookup"><span data-stu-id="030da-120">PID\_PAGECOUNT</span></span> | <span data-ttu-id="030da-121">100</span><span class="sxs-lookup"><span data-stu-id="030da-121">100</span></span>   |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="030da-122">Tabela usada durante a execução:</span><span class="sxs-lookup"><span data-stu-id="030da-122">Table used during execution:</span></span>

[<span data-ttu-id="030da-123">\_Tabela de colunas</span><span class="sxs-lookup"><span data-stu-id="030da-123">\_Columns table</span></span>](-columns-table.md)

## <a name="related-topics"></a><span data-ttu-id="030da-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="030da-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="030da-125">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="030da-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



