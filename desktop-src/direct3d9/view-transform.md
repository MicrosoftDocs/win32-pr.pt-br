---
description: Esta seção apresenta os conceitos básicos da exibição de transformação e fornece detalhes sobre como configurar uma matriz de transformação de exibição em um aplicativo do Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Exibir transformação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500514"
---
# <a name="view-transform-direct3d-9"></a>Exibir transformação (Direct3D 9)

Esta seção apresenta os conceitos básicos da exibição de transformação e fornece detalhes sobre como configurar uma matriz de transformação de exibição em um aplicativo do Direct3D.

A transformação de exibição localiza o visualizador no espaço do mundo, transformando vértices em espaço da câmera. No espaço de câmera, a câmera ou visualizador está na origem, olhando na direção z positiva. Lembre-se de que o Direct3D usa um sistema de coordenadas à esquerda, portanto, z é positivo em uma cena. A matriz de exibição realoca os objetos no mundo ao redor de uma posição de câmera - a origem do espaço da câmera - e orientação.

Há muitas maneiras de criar uma matriz de exibição. Em todos os casos, a câmera tem algumas posições e orientações lógicas no espaço do mundo que são usadas como ponto de partida para criar uma matriz de exibição que será aplicada aos modelos em uma cena. A matriz de visualização é convertida e gira objetos para colocá-los no espaço da câmera, onde a câmera está na origem. Uma maneira de criar uma matriz de exibição é combinar uma matriz de translação com matrizes de rotação para cada eixo. Nesta abordagem, a seguinte equação de matriz geral se aplica.

![equação de transformação de exibição](images/viewtran.png)

Nessa fórmula, V é a matriz de visualização que está sendo criada, T é uma matriz de tradução que reposiciona objetos no mundo e Rₓ por R<sub>z</sub> são matrizes de rotação que giram objetos ao longo do eixo x, y e z. As matrizes de translação e rotação se baseiam na posição e orientação lógicas da câmera no espaço do mundo. Portanto, se a posição lógica da câmera no mundo for <10, 20100>, o objetivo da matriz de conversão é mover objetos-10 unidades ao longo das unidades do eixo x,-20, ao longo do eixo y e-100 ao longo do eixo z. As matrizes de rotação na fórmula são baseadas na orientação da câmera, em termos de quanto os eixos do espaço da câmera são girados para fora do alinhamento com o espaço do mundo. Por exemplo, se a câmera mencionada anteriormente estiver apontando diretamente para baixo, o seu eixo z é de 90 graus (pi/2 radianos) desalinhado com o eixo z do espaço do mundo, conforme mostrado na ilustração a seguir.

![Ilustração do espaço de exibição da câmera em comparação com o espaço do mundo](images/camtop.png)

As matrizes de rotação aplicam rotações de magnitude igual, porém oposta, aos modelos na cena. A matriz de visualização de câmera inclui uma rotação de -90 graus em torno do eixo x. A matriz de rotação é combinada com a matriz de translação para criar uma matriz de exibição que ajusta a posição e a orientação dos objetos na cena para que sua parte superior fique voltada para a câmera, dando a impressão de que a câmera está acima do modelo.

## <a name="setting-up-a-view-matrix"></a>Configurando uma matriz de exibição

As funções auxiliares [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) e [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) criam uma matriz de exibição com base no local da câmera e um ponto de visão.

O exemplo a seguir cria uma matriz de exibição para coordenadas da mão esquerda.


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



O Direct3D usa as matrizes de mundo e modo de exibição para configurar várias estruturas de dados internas. Cada vez que você define um novo mundo ou uma matriz de exibição, o sistema recalcula as estruturas internas associadas. Definir essas matrizes com frequência é algo computacionalmente demorado. Você pode minimizar o número de cálculos necessários concatenando as matrizes de mundo e modo de exibição em uma matriz de exibição de mundo que você define como matriz de mundo, e, em seguida, definindo a matriz de visualização para a identidade. Mantenha cópias em cache das matrizes individuais de mundo e modo de exibição para que você possa modificar, concatenar e restaurar a matriz de mundo conforme necessário. Para maior clareza, os exemplos raramente empregam essa otimização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformações](transforms.md)
</dt> </dl>

 

 



