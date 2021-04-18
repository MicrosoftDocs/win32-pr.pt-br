---
title: Aceleração de GPU no WSL
description: O Direct Machine Learning (DirectML) alimenta a GPU-accelleration no subsistema do Windows para Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105792891"
---
# <a name="gpu-accelerated-ml-training"></a>Treinamento de ML acelerado por GPU

![Gráfico do Windows ML](images/winml-graphic.png)

Esta documentação aborda o que atualmente tem suporte na visualização de treinamento do ML (aprendizado de máquina acelerada por GPU) para o [subsistema do Windows para Linux](/windows/wsl/about) (WSL) e o Windows nativo.  

Essa versão prévia dá suporte a cenários profissionais e iniciantes. Abaixo você encontrará ponteiros para guias passo a passo sobre como obter a configuração do sistema dependendo do seu nível de experiência em ML, fornecedor de GPU e a biblioteca de software que você pretende usar. 

> [!NOTE]
> Os recursos a seguir estão em versão prévia e estão sujeitos a alterações.


## <a name="professionals"></a>Alista

Se você for um cientista de dados profissional que usa um ambiente Linux nativo de desenvolvimento e experimentação de ML de loop interno e tiver uma GPU NVIDIA, é recomendável configurar a [Visualização NVIDIA CUDA no WSL 2.](gpu-cuda-in-wsl.md)

## <a name="students-and-beginners"></a>Estudantes e iniciantes 

Se você for um aluno ou iniciante procurando começar a criar seu conhecimento no espaço ML, recomendamos configurar o TensorFlow com o pacote de back-end DirectML. Esse pacote atualmente acelera fluxos de trabalho em GPUs AMD e Intel. O suporte para GPUs NVIDIA estará disponível em breve. 

Para aqueles mais familiarizados com um ambiente Linux nativo que estão começando com fluxos de trabalho ML, recomendamos executar o [TensorFlow com o pacote DirectML dentro do WSL 2](gpu-tensorflow-wsl.md). 

Para aqueles mais familiarizados com o Windows que estão começando com fluxos de trabalho ML, é recomendável configurar o [TensorFlow com o pacote DirectML no Windows nativo](gpu-tensorflow-windows.md). 

## <a name="next-steps"></a>Próximas etapas

* [Habilite a visualização NVIDIA CUDA no WSL 2](gpu-cuda-in-wsl.md).
* [Habilite o TensorFlow com o pacote DirectML dentro do WSL 2](gpu-tensorflow-wsl.md).
* [Habilite o TensorFlow com o pacote DirectML no Windows nativo](gpu-tensorflow-windows.md).