---
title: Sinalizadores de criação de transformação do CMM
description: CMMs use sinalizadores de criação de transformação como dicas sobre como criar uma transformação de cor. Cabe ao CMM determinar a melhor maneira de usar esses sinalizadores.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2021
ms.locfileid: "105764344"
---
# <a name="cmm-transform-creation-flags"></a>Sinalizadores de criação de transformação do CMM

CMMs use sinalizadores de criação de transformação como dicas sobre como criar uma transformação de cor. Cabe ao CMM determinar a melhor maneira de usar esses sinalizadores.

Todas as funções que usam esses sinalizadores passam ou recebem valores de sinalizador por meio de um parâmetro chamado *dwFlags*. A **palavra** de ordem superior do *dwFlags* deve ser definida como um valor da tabela a seguir.



| Constante                    | Descrição                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Habilitar \_ verificação de gama \_     | Use essa transformação para verificação de gamut.                                                                                                       |
| USAR \_ \_ colorimétrico relativo | Não preserve o ponto branco. Se a gama de saída não oferecer suporte a uma determinada cor, use a cor mais próxima com suporte. Consulte tentativas de renderização. |
| \_conversão rápida             | Pesquisar apenas a cor. Não interpolar a cor.                                                                                            |
| PRESERVEBLACK               | Insere o GMMP de geração de preto apropriado como o último GMMP na sequência de transformação                                                     |
| WCS \_ sempre                 | Use o caminho do código WCS até mesmo para transformações ICC.                                                                                               |
| transformação SEQUENCIAl \_       | Sinalizador de criação de transformação para criar uma transformação de cor sequencial (não otimizada).                                                           |



 

A **palavra** de ordem inferior pode ter um dos valores constantes a seguir.



| Constante     | Descrição                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| modo de prova \_  | A transformação será usada para visualizar a imagem. Baixa qualidade da imagem.                                    |
| \_modo normal | A transformação será usada para exibição de imagem normal. Qualidade média da imagem.                            |
| \_modo melhor   | A transformação será usada para a exibição da imagem de qualidade mais alta possível no dispositivo de destino. |



 

Movendo do modo de prova \_ para o melhor \_ modo, a qualidade da saída geralmente melhora e transforma as rejeições de velocidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Constantes de ICM](wcs-constants.md)
</dt> </dl>

 

 




