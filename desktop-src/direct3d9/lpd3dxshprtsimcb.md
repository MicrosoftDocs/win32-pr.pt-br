---
description: Função de retorno de chamada para simulação e compactação de PRT (Transferência de Radiance Pré-comutada).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a7c4911bf2a7b7fa2aa83422a206644f6eb747
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342801"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="c55a6-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="c55a6-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="c55a6-104">Função de retorno de chamada para simulação e compactação de PRT (Transferência de Radiance Pré-comutada).</span><span class="sxs-lookup"><span data-stu-id="c55a6-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c55a6-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="c55a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c55a6-106">Parameters</span></span>

<span data-ttu-id="c55a6-107">fPercentDone – número de ponto flutuante entre 0 e 1,0 que representa o percentual de cálculos concluídos (entre 0 e 100%).</span><span class="sxs-lookup"><span data-stu-id="c55a6-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="c55a6-108">lpUserContext – ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c55a6-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="c55a6-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c55a6-109">Return Value</span></span>

<span data-ttu-id="c55a6-110">Essa função deve ser implementada para retornar S \_ OK para continuar executando o simulador.</span><span class="sxs-lookup"><span data-stu-id="c55a6-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="c55a6-111">Qualquer outro valor interromperá o simulador.</span><span class="sxs-lookup"><span data-stu-id="c55a6-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="c55a6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c55a6-112">Remarks</span></span>

<span data-ttu-id="c55a6-113">Especifique a convenção de chamada Tipos de [**Dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c55a6-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="c55a6-114">Caso contrário, podem ocorrer estouros de pilha.</span><span class="sxs-lookup"><span data-stu-id="c55a6-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="c55a6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c55a6-115">Requirement</span></span>                         | <span data-ttu-id="c55a6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c55a6-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="c55a6-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c55a6-117">Header</span></span>                   | <span data-ttu-id="c55a6-118">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="c55a6-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="c55a6-119">Bibliotecas de importação</span><span class="sxs-lookup"><span data-stu-id="c55a6-119">Import Library</span></span>           | <span data-ttu-id="c55a6-120">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="c55a6-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="c55a6-121">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="c55a6-121">Minimum Operating System</span></span> | <span data-ttu-id="c55a6-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c55a6-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="c55a6-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c55a6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c55a6-124">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="c55a6-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
