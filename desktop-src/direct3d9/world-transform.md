---
description: A discussão da transformação do mundo apresenta conceitos básicos e fornece detalhes sobre como configurar uma transformação do mundo.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Transformação mundial (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370098"
---
# <a name="world-transform-direct3d-9"></a><span data-ttu-id="62720-103">Transformação mundial (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="62720-103">World Transform (Direct3D 9)</span></span>

<span data-ttu-id="62720-104">A discussão da transformação do mundo apresenta conceitos básicos e fornece detalhes sobre como configurar uma transformação do mundo.</span><span class="sxs-lookup"><span data-stu-id="62720-104">The discussion of the world transformation introduces basic concepts and provides details on how to set up a world transform.</span></span>

## <a name="what-is-a-world-transform"></a><span data-ttu-id="62720-105">O que é uma transformação mundial?</span><span class="sxs-lookup"><span data-stu-id="62720-105">What Is a World Transform?</span></span>

<span data-ttu-id="62720-106">Uma transformação mundial altera as coordenadas do espaço do modelo, em que os vértices são definidos em relação à origem local de um modelo, para o espaço mundial, em que os vértices são definidos em relação a uma origem comum a todos os objetos em uma cena.</span><span class="sxs-lookup"><span data-stu-id="62720-106">A world transform changes coordinates from model space, where vertices are defined relative to a model's local origin, to World Space, where vertices are defined relative to an origin common to all the objects in a scene.</span></span> <span data-ttu-id="62720-107">Em essência, a transformação do mundo coloca um modelo no mundo; daí o seu nome.</span><span class="sxs-lookup"><span data-stu-id="62720-107">In essence, the world transform places a model into the world; hence its name.</span></span> <span data-ttu-id="62720-108">O diagrama a seguir mostra a relação entre o sistema de coordenadas do mundo e o sistema de coordenadas local do modelo.</span><span class="sxs-lookup"><span data-stu-id="62720-108">The following diagram shows the relationship between the world coordinate system and a model's local coordinate system.</span></span>

![diagrama de como as coordenadas de mundo e locais estão relacionadas](images/worldcrd.png)

<span data-ttu-id="62720-110">A transformação do mundo pode incluir qualquer combinação de traduções, rotações e escalas.</span><span class="sxs-lookup"><span data-stu-id="62720-110">The world transform can include any combination of translations, rotations, and scalings.</span></span>

## <a name="setting-up-a-world-matrix"></a><span data-ttu-id="62720-111">Configurando uma matriz de mundo</span><span class="sxs-lookup"><span data-stu-id="62720-111">Setting Up a World Matrix</span></span>

<span data-ttu-id="62720-112">Assim como com qualquer outra transformação, crie a transformação do mundo concatenando uma série de matrizes em uma única matriz que contém a soma total de seus efeitos.</span><span class="sxs-lookup"><span data-stu-id="62720-112">As with any other transform, create the world transform by concatenating a series of matrices into a single matrix that contains the sum total of their effects.</span></span> <span data-ttu-id="62720-113">No caso mais simples, quando um modelo está na origem de mundo e seus eixos de coordenada locais são orientados da mesma forma que o espaço do mundo, a matriz de mundo é a matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="62720-113">In the simplest case, when a model is at the world origin and its local coordinate axes are oriented the same as world space, the world matrix is the identity matrix.</span></span> <span data-ttu-id="62720-114">Mais comumente, a matriz de mundo é uma combinação de uma translação no espaço do mundo e possivelmente uma ou mais rotações para girar o modelo conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="62720-114">More commonly, the world matrix is a combination of a translation into world space and possibly one or more rotations to turn the model as needed.</span></span>

<span data-ttu-id="62720-115">O exemplo a seguir, de uma classe de modelo 3D fictícia escrita em C++, usa as funções auxiliares incluídas na biblioteca do utilitário D3DX para criar uma matriz mundial que inclui três rotações para orientar um modelo e uma tradução para realocá-la em relação à sua posição no espaço de mundo.</span><span class="sxs-lookup"><span data-stu-id="62720-115">The following example, from a fictitious 3D model class written in C++, uses the helper functions included in the D3DX utility library to create a world matrix that includes three rotations to orient a model and a translation to relocate it relative to its position in world space.</span></span>


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



<span data-ttu-id="62720-116">Depois de preparar a matriz mundial, chame o método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) para defini-lo, especificando a macro do [**D3DTS \_ World**](d3dts-world.md) para o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="62720-116">After you prepare the world matrix, call the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method to set it, specifying the [**D3DTS\_WORLD**](d3dts-world.md) macro for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="62720-117">O Direct3D usa as matrizes de mundo e modo de exibição que você definiu para configurar várias estruturas de dados internas.</span><span class="sxs-lookup"><span data-stu-id="62720-117">Direct3D uses the world and view matrices that you set to configure several internal data structures.</span></span> <span data-ttu-id="62720-118">Cada vez que você define um novo mundo ou uma matriz de exibição, o sistema recalcula as estruturas internas associadas.</span><span class="sxs-lookup"><span data-stu-id="62720-118">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="62720-119">Definir essas matrizes frequentemente, por exemplo, milhares de vezes por quadro, é computacionalmente demorado.</span><span class="sxs-lookup"><span data-stu-id="62720-119">Setting these matrices frequently-for example, thousands of times per frame-is computationally time-consuming.</span></span> <span data-ttu-id="62720-120">Você pode minimizar o número de cálculos necessários concatenando as matrizes de mundo e modo de exibição em uma matriz de exibição de mundo que você define como matriz de mundo, e, em seguida, definindo a matriz de visualização para a identidade.</span><span class="sxs-lookup"><span data-stu-id="62720-120">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="62720-121">Mantenha cópias em cache das matrizes individuais de mundo e modo de exibição para que você possa modificar, concatenar e restaurar a matriz de mundo conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="62720-121">Keep cached copies of individual world and view matrices so that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="62720-122">Para maior clareza, nesta documentação, exemplos de Direct3D raramente empregam essa otimização.</span><span class="sxs-lookup"><span data-stu-id="62720-122">For clarity, in this documentation Direct3D samples rarely employ this optimization.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="62720-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62720-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62720-124">Transformações</span><span class="sxs-lookup"><span data-stu-id="62720-124">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



