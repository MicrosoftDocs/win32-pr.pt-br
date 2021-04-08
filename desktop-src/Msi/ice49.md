---
description: ICE49 verifica as entradas de registro padrão que não são do \_ tipo reg sz.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829477"
---
# <a name="ice49"></a><span data-ttu-id="7a4d3-103">ICE49</span><span class="sxs-lookup"><span data-stu-id="7a4d3-103">ICE49</span></span>

<span data-ttu-id="7a4d3-104">ICE49 verifica as entradas de registro padrão que não são do tipo **reg \_ sz** .</span><span class="sxs-lookup"><span data-stu-id="7a4d3-104">ICE49 checks for default registry entries that are not a **REG\_SZ** type.</span></span>

## <a name="result"></a><span data-ttu-id="7a4d3-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="7a4d3-105">Result</span></span>

<span data-ttu-id="7a4d3-106">ICE49 posta um aviso se houver uma entrada de registro padrão que não seja um tipo **reg \_ sz** .</span><span class="sxs-lookup"><span data-stu-id="7a4d3-106">ICE49 posts an warning if there is a default registry entry that is not a **REG\_SZ** type.</span></span>

## <a name="example"></a><span data-ttu-id="7a4d3-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7a4d3-107">Example</span></span>

<span data-ttu-id="7a4d3-108">ICE49 relata o seguinte aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="7a4d3-108">ICE49 reports the following warning for the example shown.</span></span>

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

<span data-ttu-id="7a4d3-109">O valor ' \# 123 ' é um valor de registro **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7a4d3-109">The value '\#123' is a **DWORD** registry value.</span></span>

<span data-ttu-id="7a4d3-110">[Tabela do registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="7a4d3-110">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="7a4d3-111">Registro</span><span class="sxs-lookup"><span data-stu-id="7a4d3-111">Registry</span></span> | <span data-ttu-id="7a4d3-112">Nome</span><span class="sxs-lookup"><span data-stu-id="7a4d3-112">Name</span></span> | <span data-ttu-id="7a4d3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7a4d3-113">Value</span></span> |
|----------|------|-------|
| <span data-ttu-id="7a4d3-114">Reg1</span><span class="sxs-lookup"><span data-stu-id="7a4d3-114">Reg1</span></span>     |      | <span data-ttu-id="7a4d3-115">\#123</span><span class="sxs-lookup"><span data-stu-id="7a4d3-115">\#123</span></span> |



 

<span data-ttu-id="7a4d3-116">Para corrigir esse aviso, altere o valor para tipo **reg \_ sz**.</span><span class="sxs-lookup"><span data-stu-id="7a4d3-116">To fix this warning, change the value to type **REG\_SZ**.</span></span>

<span data-ttu-id="7a4d3-117">Os componentes com **\_ sz não reg** são válidos.</span><span class="sxs-lookup"><span data-stu-id="7a4d3-117">Components with non-**REG\_SZ** are valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a4d3-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a4d3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a4d3-119">Sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="7a4d3-119">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="7a4d3-120">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="7a4d3-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



