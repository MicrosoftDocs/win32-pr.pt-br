---
description: Função de retorno de chamada para UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342791"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="063d1-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="063d1-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="063d1-104">Função de retorno de chamada para UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="063d1-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="063d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="063d1-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="063d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="063d1-106">Parameters</span></span>

<span data-ttu-id="063d1-107">\[out \] fPercentDone-número de ponto flutuante entre 0 e 1,0 que representa a porcentagem de cálculos concluídos (entre 0 e 100 por cento).</span><span class="sxs-lookup"><span data-stu-id="063d1-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="063d1-108">\[no \] lpUserContext-pointer para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="063d1-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="063d1-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="063d1-109">Return Value</span></span>

<span data-ttu-id="063d1-110">Essa função deve ser implementada para retornar S \_ OK para continuar executando o simulador.</span><span class="sxs-lookup"><span data-stu-id="063d1-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="063d1-111">Qualquer outro valor interromperá o simulador.</span><span class="sxs-lookup"><span data-stu-id="063d1-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="063d1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="063d1-112">Remarks</span></span>

<span data-ttu-id="063d1-113">Certifique-se de especificar a Convenção de chamada de [**tipos de dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="063d1-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="063d1-114">Caso contrário, podem ocorrer estouros de pilha.</span><span class="sxs-lookup"><span data-stu-id="063d1-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="063d1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="063d1-115">Requirement</span></span>                         | <span data-ttu-id="063d1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="063d1-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="063d1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="063d1-117">Header</span></span>                   | <span data-ttu-id="063d1-118">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="063d1-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="063d1-119">Bibliotecas de importação</span><span class="sxs-lookup"><span data-stu-id="063d1-119">Import Library</span></span>           | <span data-ttu-id="063d1-120">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="063d1-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="063d1-121">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="063d1-121">Minimum Operating System</span></span> | <span data-ttu-id="063d1-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="063d1-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="063d1-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="063d1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="063d1-124">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="063d1-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
