---
description: Todos os recursos compartilham as propriedades a seguir.
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: Propriedades do recurso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7b53a23e489b5f53495c5d2626da1e2633c9cf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646066"
---
# <a name="resource-properties-direct3d-9"></a>Propriedades do recurso (Direct3D 9)

Todos os recursos compartilham as propriedades a seguir.

-   Uso. A maneira como um recurso é usado, por exemplo, como uma textura ou um destino de renderização.
-   Formato. O formato dos dados, por exemplo, o formato de pixel de uma superfície 2D.
-   Pool. O tipo de memória em que o recurso está alocado.
-   Digite. O tipo de recurso, por exemplo, um buffer de vértice ou destino de renderização.

Os usos de recursos são impostos. Um aplicativo que usará um recurso em uma determinada operação deve especificar essa operação no momento da criação do recurso. Para obter uma lista das constantes de uso definidas para recursos, consulte [**D3DUSAGE**](d3dusage.md).

As \_ constantes D3DUSAGE RTPATCHES, D3DUSAGE \_ NPATCHES e D3DUSAGE \_ Point indicam ao driver que os dados nesses buffers provavelmente serão usados para patches triangulares ou de grade, N-patches ou sprites, respectivamente. Esses sinalizadores são fornecidos caso o hardware não possa executar essas operações sem processamento de host. Portanto, o driver desejará alocar essas superfícies na memória do sistema para que a CPU possa acessá-las. Se o driver puder executar essas operações inteiramente no hardware, ele poderá alocar essas superfícies na memória de vídeo ou AGP para evitar uma cópia do host e melhorar o desempenho pelo menos duplo. Observe que as informações fornecidas por esses sinalizadores não são absolutamente necessárias. Um driver pode detectar que essas operações estão sendo executadas nos dados e moverá o buffer de volta para a memória do sistema para quadros subsequentes.

Para obter detalhes sobre os sinalizadores de uso e como eles se relacionam com recursos específicos, consulte as páginas de referência nos métodos de criação de recursos individuais.

Para obter informações sobre o formato de superfície de recursos, consulte o tipo enumerado [D3DFORMAT](d3dformat.md) .

A classe de memória que contém os buffers de um recurso é chamada de pool. Os valores de pool são definidos pelo tipo enumerado [**D3DPOOL**](./d3dpool.md) . Um pool não pode ser misturado para objetos diferentes contidos em um único recurso, ou seja, níveis de MIP em um mipmap-e, quando um pool é escolhido para um recurso, o pool não pode ser alterado.

Os tipos de recursos são definidos implicitamente em tempo de execução quando o aplicativo chama um método de criação de recursos, como [**IDirect3DDevice9:: CreateCubeTexture**](/windows/desktop/api). Os tipos de recurso são definidos pelo tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) . Os aplicativos podem consultar esses tipos em tempo de execução; no entanto, espera-se que a maioria dos cenários não exija a verificação do tipo em tempo de execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
