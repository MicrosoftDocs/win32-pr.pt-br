---
title: Alterações no suporte de hardware herdado DX9
description: Alterações no suporte de hardware herdado DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105813447"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Alterações no suporte de hardware herdado DX9

## <a name="platform"></a>Plataforma

**Clientes** – Windows 8 


## <a name="description"></a>Descrição

A Intel e a AMD/ATI não suportam mais suas partes gráficas DX9 e não estarão Atualizando Drivers para esses dispositivos para o Windows 8. Além disso, esses dispositivos não são abordados na caixa para o Windows 8. Os últimos drivers para esses dispositivos estão disponíveis no WU e nos sites do OEM/IHV; muitas datas do vista e muitos desses drivers de versão final apresentam problemas no Windows 8. Além disso, o nVidia afirmou recentemente que eles não oferecerão suporte às suas peças de DX9 (vista e mais antigas) móveis (Notebook) para o Windows 8. Eles continuam a dar suporte às suas partes de desktop DX9.

Todas essas combinações de driver/parte estão na lista de fallback de software do Internet Explorer 9. Isso significa que, para fins de desempenho ou estabilidade, o Internet Explorer 9 usa a renderização de software nesses dispositivos. Essa é uma boa indicação de que a experiência com aplicativos da Windows Store não será satisfatória nesses drivers e partes.

## <a name="manifestation"></a>Manifestação

Como não há nenhum suporte na caixa para esses dispositivos, muitos usuários com essas partes serão executados no driver de vídeo básico da Microsoft. Trata-se de uma GPU de software WDDM 1,2 baseada em distorção e é, na verdade, mais rápida do que algumas das partes desta classe, por exemplo, a série GMA500 da Intel. Ele dá suporte ao Aero-Glass e ao DWM e pode executar aplicativos da Windows Store.

No entanto, ele tem algumas limitações importantes:

-   Ele não dá suporte a vários monitores ou projeção
-   Ele não dá suporte à suspensão, embora ofereça suporte à hibernação
-   Geralmente, não permitirá a alteração da resolução da tela

## <a name="mitigation"></a>Atenuação

Se, após o teste, você descobrir que a experiência do usuário não é aceitável, poderá optar por definir os requisitos de hardware para seus produtos que excluem essas partes mais antigas do DX9 Intel e AMD. Você também pode optar por alertar seus clientes de que eles podem ter uma experiência inaceitável nessas partes.

## <a name="tests"></a>Testes

Avalie o desempenho e a experiência nesses dispositivos:

-   Qual é a experiência como na versão final do driver disponível?
-   Qual é a experiência como no MSBDD?

 

 




