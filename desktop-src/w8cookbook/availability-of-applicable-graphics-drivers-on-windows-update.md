---
title: disponibilidade de drivers gráficos aplicáveis no Windows Update
description: a disponibilidade desses drivers em Windows Update (WU) determinará se um usuário recebe automaticamente uma atualização do Windows 7, Windows 8 ou Windows 8.1 para Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 906894f317a86d851501e913e3c9491dc1f83336f7f80eefa660ee43d3510b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935426"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>disponibilidade de drivers gráficos aplicáveis no Windows Update

a disponibilidade desses drivers em Windows Update (WU) determinará se um usuário recebe automaticamente uma atualização do Windows 7, Windows 8 ou Windows 8.1 para Windows 10. se as verificações de hardware mostrarem que não havia nenhum driver de gráfico disponível em Windows Update para o adaptador gráfico no PC, os usuários não terão oferecido o sistema operacional atualizado Windows 10. no entanto, os usuários ainda podem obter Windows 10 por meio de outras fontes e executar manualmente a atualização.

alguns usuários não tinham certeza de por que eles não ofereciam a atualização quando outras pessoas eram, mesmo que a Supervisor de Atualização tenha explicado que não havia driver de gráficos disponível para seu hardware.

Além disso, alguns usuários forçaram uma atualização e, em seguida, descobriram que sua funcionalidade gráfica e desempenho sofreu devido à falta de um driver de hardware.

## <a name="mitigations"></a>Atenuações

para atenuar isso, os usuários podem instalar manualmente um driver mais antigo, ou seja, do Windows 7, Windows 8 ou Windows 8.1, acessando o site do IHV ou OEM e baixando um driver explicitamente. Isso deve ser feito após a atualização e não há garantia de que funcione. Não há solução com suporte se um driver gráfico adequado não estiver disponível no WU. O usuário deve decidir se:

-   Permanecer no sistema operacional anterior;
-   Aceite as limitações do driver de software, o adaptador de vídeo básico da Microsoft (MSBDA); or
-   compre uma nova placa gráfica que tenha um driver de Windows 10 com suporte.

## <a name="solutions"></a>Soluções

é fundamental que os IHVs e os OEMs carreguem seus drivers gráficos de Windows 10 no WU para qualquer hardware que pretendam oferecer suporte.

Observe que o hardware que atingiu o fim da vida útil (EOL) pode não ter drivers no WU. Não há nenhuma solução nesse caso – o usuário deve escolher uma das opções em atenuações acima.

 

 




