---
title: Operações de DrawDib
description: Operações de DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib, sobre
- DrawDib, acessando
- DrawDib, abrindo
- DrawDib, operações
- DrawDib, contexto do dispositivo (DC)
- DC (contexto do dispositivo)
- Função DrawDibOpen
- Função DrawDibClose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453723"
---
# <a name="drawdib-operations"></a>Operações de DrawDib

Você pode acessar o grupo inteiro de funções DrawDib usando a função [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) . Essa função carrega a DLL (biblioteca de vínculo dinâmico), aloca recursos de memória, cria um DrawDib (contexto de dispositivo) e mantém uma contagem de referência do número de controladores de domínio que são inicializados. O **DrawDibOpen** também retorna um identificador do novo DC que você usa com as outras funções DrawDib.

Você pode liberar um DrawDib DC ao terminar de usá-lo usando a função [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) . **DrawDibClose** também decrementa a contagem de referência dos aplicativos que acessam a dll. A chamada para **DrawDibClose** deve ser a última função DrawDib em seu aplicativo.

Você pode criar quantos DCs DrawDib desejar. Você pode usar vários DCs DrawDib para desenhar vários bitmaps simultaneamente. Você também pode criar vários DCs DrawDib, cada um com características exclusivas, para que seu aplicativo possa escolher e, em seguida, usar o controlador de domínio com as configurações mais apropriadas. Por exemplo, você pode criar dois DCs DrawDib em um aplicativo: um que exibe uma imagem em sua resolução normal e o outro que exibe uma parte ampliada da imagem.

Para executar com eficiência, as funções DrawDib exigem informações sobre o adaptador de vídeo e seu driver. O perfil de exibição é obtido executando uma série de testes no adaptador de vídeo na primeira vez que a DLL que contém as funções DrawDib é acessada. As funções DrawDib usam essas informações para todos os aplicativos. Você pode repetir esses testes quando necessário usando a função [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .

> [!Note]  
> Recuperar e armazenar o perfil de exibição normalmente é uma ocorrência única. Se, no entanto, as informações de perfil forem excluídas ou outro driver de vídeo estiver instalado no sistema, o DrawDib executará novamente os testes.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre as funções DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




