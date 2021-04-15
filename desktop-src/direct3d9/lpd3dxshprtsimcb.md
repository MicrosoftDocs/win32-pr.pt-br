---
description: Função de retorno de chamada para simulação e compactação de PRT (transferência de radiante preputada).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456716"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="212ae-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="212ae-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="212ae-104">Função de retorno de chamada para simulação e compactação de PRT (transferência de radiante preputada).</span><span class="sxs-lookup"><span data-stu-id="212ae-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="212ae-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="212ae-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="212ae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="212ae-106">Parameters</span></span>

<span data-ttu-id="212ae-107">fPercentDone-número de ponto flutuante entre 0 e 1,0 que representa a porcentagem de cálculos concluídos (entre 0 e 100 por cento).</span><span class="sxs-lookup"><span data-stu-id="212ae-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="212ae-108">lpUserContext-ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="212ae-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="212ae-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="212ae-109">Return Value</span></span>

<span data-ttu-id="212ae-110">Essa função deve ser implementada para retornar S \_ OK para continuar executando o simulador.</span><span class="sxs-lookup"><span data-stu-id="212ae-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="212ae-111">Qualquer outro valor interromperá o simulador.</span><span class="sxs-lookup"><span data-stu-id="212ae-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="212ae-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="212ae-112">Remarks</span></span>

<span data-ttu-id="212ae-113">Certifique-se de especificar a Convenção de chamada de [**tipos de dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="212ae-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="212ae-114">Caso contrário, podem ocorrer estouros de pilha.</span><span class="sxs-lookup"><span data-stu-id="212ae-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="212ae-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="212ae-115">Header</span></span>                   | <span data-ttu-id="212ae-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="212ae-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="212ae-117">Bibliotecas de importação</span><span class="sxs-lookup"><span data-stu-id="212ae-117">Import Library</span></span>           | <span data-ttu-id="212ae-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="212ae-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="212ae-119">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="212ae-119">Minimum Operating System</span></span> | <span data-ttu-id="212ae-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="212ae-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="212ae-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="212ae-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="212ae-122">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="212ae-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
