---
description: A discussão da transformação do mundo apresenta conceitos básicos e fornece detalhes sobre como configurar uma transformação do mundo.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Transformação mundial (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbddefbaa5ad4bd41e7dafa79e086605d8f40e761cca2bd6ce9b9c0b212950a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518895"
---
# <a name="world-transform-direct3d-9"></a>Transformação mundial (Direct3D 9)

A discussão da transformação do mundo apresenta conceitos básicos e fornece detalhes sobre como configurar uma transformação do mundo.

## <a name="what-is-a-world-transform"></a>O que é uma transformação mundial?

Uma transformação mundial altera as coordenadas do espaço do modelo, em que os vértices são definidos em relação à origem local de um modelo, para o espaço mundial, em que os vértices são definidos em relação a uma origem comum a todos os objetos em uma cena. Em essência, a transformação do mundo coloca um modelo no mundo; daí o seu nome. O diagrama a seguir mostra a relação entre o sistema de coordenadas do mundo e o sistema de coordenadas local do modelo.

![diagrama de como as coordenadas de mundo e locais estão relacionadas](images/worldcrd.png)

A transformação do mundo pode incluir qualquer combinação de traduções, rotações e escalas.

## <a name="setting-up-a-world-matrix"></a>Configurando uma matriz de mundo

Assim como com qualquer outra transformação, crie a transformação do mundo concatenando uma série de matrizes em uma única matriz que contém a soma total de seus efeitos. No caso mais simples, quando um modelo está na origem de mundo e seus eixos de coordenada locais são orientados da mesma forma que o espaço do mundo, a matriz de mundo é a matriz de identidade. Mais comumente, a matriz de mundo é uma combinação de uma translação no espaço do mundo e possivelmente uma ou mais rotações para girar o modelo conforme necessário.

O exemplo a seguir, de uma classe de modelo 3D fictícia escrita em C++, usa as funções auxiliares incluídas na biblioteca do utilitário D3DX para criar uma matriz mundial que inclui três rotações para orientar um modelo e uma tradução para realocá-la em relação à sua posição no espaço de mundo.


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



Depois de preparar a matriz mundial, chame o método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) para defini-lo, especificando a macro do [**D3DTS \_ World**](d3dts-world.md) para o primeiro parâmetro.

> [!Note]  
> O Direct3D usa as matrizes de mundo e modo de exibição que você definiu para configurar várias estruturas de dados internas. Cada vez que você define um novo mundo ou uma matriz de exibição, o sistema recalcula as estruturas internas associadas. Definir essas matrizes frequentemente, por exemplo, milhares de vezes por quadro, é computacionalmente demorado. Você pode minimizar o número de cálculos necessários concatenando as matrizes de mundo e modo de exibição em uma matriz de exibição de mundo que você define como matriz de mundo, e, em seguida, definindo a matriz de visualização para a identidade. Mantenha cópias em cache das matrizes individuais de mundo e modo de exibição para que você possa modificar, concatenar e restaurar a matriz de mundo conforme necessário. Para maior clareza, nesta documentação, exemplos de Direct3D raramente empregam essa otimização.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformações](transforms.md)
</dt> </dl>

 

 



