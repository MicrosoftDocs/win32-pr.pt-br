---
description: Sinalizador de funcionalidade do driver.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059c2f9f1bf32275423bb9f2a9f484c12824bcda
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797622"
---
# <a name="d3denum"></a><span data-ttu-id="db33e-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="db33e-103">D3DENUM</span></span>

<span data-ttu-id="db33e-104">Sinalizador de funcionalidade do driver.</span><span class="sxs-lookup"><span data-stu-id="db33e-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db33e-105">#definir</span><span class="sxs-lookup"><span data-stu-id="db33e-105">#define</span></span></td>
<td><span data-ttu-id="db33e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="db33e-106">Value</span></span></td>
<td><span data-ttu-id="db33e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="db33e-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db33e-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="db33e-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="db33e-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="db33e-109">0x00000002L</span></span></td>
<td><span data-ttu-id="db33e-110">Teste de driver do Microsoft Windows Hardware Quality Labs (WHQL).</span><span class="sxs-lookup"><span data-stu-id="db33e-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="db33e-111">Esse é um teste demorado que exige uma penalidade de tempo de um segundo ou de dois segundos.</span><span class="sxs-lookup"><span data-stu-id="db33e-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="db33e-112">Essa constante é usada pelo membro WHQLLevel de <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db33e-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db33e-113">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="db33e-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="db33e-114">O D3DENUM_WHQL_LEVEL foi preterido para Direct3D9Ex em execução no Windows Vista, no Windows Server 2008, no Windows 7 e no Windows Server 2008 R2 (ou mais no sistema operacional atual).</span><span class="sxs-lookup"><span data-stu-id="db33e-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="db33e-115">Qualquer um desses sistemas operacionais retorna 1 para o nível do WHQL sem verificar o status do driver.</span><span class="sxs-lookup"><span data-stu-id="db33e-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="db33e-116">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="db33e-116">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="db33e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db33e-117">Header</span></span>                   | <span data-ttu-id="db33e-118">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="db33e-118">d3d9.h</span></span>     |
| <span data-ttu-id="db33e-119">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="db33e-119">Minimum operating system</span></span> | <span data-ttu-id="db33e-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="db33e-120">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="db33e-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db33e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db33e-122">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="db33e-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




