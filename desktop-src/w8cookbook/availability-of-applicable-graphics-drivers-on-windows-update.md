---
title: Disponibilidade de drivers gráficos aplicáveis no Windows Update
description: A disponibilidade desses drivers em Windows Update (WU) determinará se um usuário recebe automaticamente uma atualização do Windows 7, Windows 8 ou Windows 8.1 para o Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784964"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Disponibilidade de drivers gráficos aplicáveis no Windows Update

A disponibilidade desses drivers em Windows Update (WU) determinará se um usuário recebe automaticamente uma atualização do Windows 7, Windows 8 ou Windows 8.1 para o Windows 10. Se as verificações de hardware mostrarem que não havia driver de gráficos disponível em Windows Update para o adaptador gráfico no PC, os usuários não receberam o sistema operacional Windows 10 atualizado. No entanto, os usuários ainda podem obter o Windows 10 por meio de outras fontes e executar manualmente a atualização.

Alguns usuários não tinham certeza de por que eles não ofereciam a atualização quando outras pessoas eram, embora o supervisor de atualização tenha explicado que não havia nenhum driver de gráfico disponível para seu hardware.

Além disso, alguns usuários forçaram uma atualização e, em seguida, descobriram que sua funcionalidade gráfica e desempenho sofreu devido à falta de um driver de hardware.

## <a name="mitigations"></a>Atenuações

Para atenuar isso, os usuários podem instalar manualmente um driver mais antigo, ou seja, do Windows 7, Windows 8 ou Windows 8.1, acessando o site da Web do IHV ou OEM e baixando um driver explicitamente. Isso deve ser feito após a atualização e não há garantia de que funcione. Não há solução com suporte se um driver gráfico adequado não estiver disponível no WU. O usuário deve decidir se:

-   Permanecer no sistema operacional anterior;
-   Aceite as limitações do driver de software, o adaptador de vídeo básico da Microsoft (MSBDA); or
-   Compre uma nova placa gráfica que tenha um driver do Windows 10 com suporte.

## <a name="solutions"></a>Soluções

É fundamental que os IHVs e os OEMs Carreguem seus drivers gráficos do Windows 10 no WU para qualquer hardware que pretendam oferecer suporte.

Observe que o hardware que atingiu o fim da vida útil (EOL) pode não ter drivers no WU. Não há nenhuma solução nesse caso – o usuário deve escolher uma das opções em atenuações acima.

 

 




