---
description: Constantes de limitação de recursos.
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1d6bf4f72c4ef09eafba3ee50659e5e6ffc682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296103"
---
# <a name="d3d10_req"></a>\_Req d3d10

Constantes de limitação de recursos.



| \#definir                                      | Valor | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Níveis de \_ MIP de req d3d10 \_                       | 14    | Número máximo de níveis de mipmap que um recurso de textura pode ter.                                                                                                                                                                                                                                                                                                                                                                    |
| \_ \_ Tamanho do recurso req d3d10 \_ \_ em \_ megabytes     | 128   | Tamanho máximo possível de um recurso em megabytes. Os aplicativos podem criar recursos maiores do que o tamanho máximo de recursos em alguns hardwares gráficos. No entanto, recomendamos que os aplicativos mantenham recursos menores do que o tamanho máximo do recurso para obter a quantidade máxima de compatibilidade entre fornecedores de gráficos. O tempo de execução garante apenas que as alocações dentro do tamanho máximo do recurso sejam suportadas por todo o hardware do Direct3D 10. |
| \_Dimensão do \_ \_ eixo da matriz d3d10 req TEXTURE1D \_ \_ | 512   | Tamanho máximo da matriz de uma matriz de textura 1D.                                                                                                                                                                                                                                                                                                                                                                                       |
| \_Dimensão do \_ \_ eixo da matriz d3d10 req TEXTURE2D \_ \_ | 512   | Tamanho máximo da matriz de uma matriz de textura 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| \_Dimensão d3d10 req \_ TEXTURE1D \_ U \_           | 8192  | Largura máxima de uma textura 1D.                                                                                                                                                                                                                                                                                                                                                                                                  |
| \_Dimensão d3d10 req \_ TEXTURE2D \_ U \_ ou \_ V \_    | 8192  | Largura e altura máximas de uma textura 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| \_Dimensão d3d10 req \_ TEXTURE3D \_ U \_ V \_ ou \_ W \_ | 2.048  | Largura máxima, altura e profundidade de uma textura 3D.                                                                                                                                                                                                                                                                                                                                                                               |
| \_Dimensão de \_ TEXTURECUBE \_ req d3d10            | 8192  | Tamanho máximo de uma textura de cubo.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

As constantes são definidas em D3D10. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de recurso](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[Referência do Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



