---
title: Alterações no suporte a hardware herdado DX9
description: Alterações no suporte a hardware herdado DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfd0b8bbb05161ffe14ff57cc5db97fe88a22bf6e64a495e2b43dd8240def82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211802"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Alterações no suporte a hardware herdado DX9

## <a name="platform"></a>Plataforma

**Clientes** – Windows 8 


## <a name="description"></a>Descrição

Intel e AMD/ATI não são mais compatíveis com suas partes gráficas DX9 e não atualizarão drivers para esses dispositivos para Windows 8. Além disso, esses dispositivos não são abordados na caixa de Windows 8. Os últimos drivers para esses dispositivos são aqueles disponíveis no WU e nos sites do OEM/IHV; muitos datas do Vista e muitos desses drivers de versão final apresentam problemas Windows 8. Além disso, a nVidia declarou recentemente que não dará suporte às partes móveis (notebook) DX9 (Vista e mais antigas) para Windows 8. Eles continuam a dar suporte às partes DX9 da área de trabalho.

Todas essas combinações de driver/parte estão na lista Internet Explorer fallback de software 9. Isso significa que, por motivos de desempenho ou estabilidade, Internet Explorer 9 usa a renderização de software nesses dispositivos. Essa é uma boa indicação de que a experiência com aplicativos Windows Store não será satisfatória nesses drivers e partes.

## <a name="manifestation"></a>Manifestação

Como não há suporte in-box para esses dispositivos, muitos usuários com essas partes acabarão sendo executados no Microsoft Basic Display Driver. Essa é uma GPU de software WDDM 1.2 baseada em WARP e é, na verdade, mais rápida do que algumas das partes nesta classe, por exemplo, a série Intel GMA500). Ele dá suporte a aero-glass e DWM e pode executar aplicativos Windows Store.

No entanto, ele tem algumas limitações importantes:

-   Ele não dá suporte a vários monitores ou projeção
-   Ele não dá suporte a sleep, embora ele dá suporte à hibernação
-   Geralmente, ele não permitirá alterar a resolução da tela

## <a name="mitigation"></a>Atenuação

Se, após o teste, você descobrir que a experiência do usuário não é aceitável, poderá optar por definir requisitos de hardware para seus produtos que excluam essas partes DX9 Intel e AMD mais antigas. Você também pode optar por alertar seus clientes de que eles podem ter uma experiência inaceitável nessas partes.

## <a name="tests"></a>Testes

Avalie o desempenho e a experiência nesses dispositivos:

-   Como é a experiência na versão final do driver disponível?
-   Como é a experiência no MSBDD?

 

 




