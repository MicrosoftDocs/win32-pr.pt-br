---
title: Entrada do mousewheel para Windows 8.1
description: Entrada do mousewheel para Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2285d2a0456376b01289ac7a4c2607117441384ebd13b0aaf0a162eac50fdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211379"
---
# <a name="mousewheel-input-for-windows-81"></a>Entrada do mousewheel para Windows 8.1

## <a name="platform"></a>Plataforma

<dl> Clientes – Windows 8.1  
Servidores – Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

No Windows 8.1, os eventos do mousewheel não são mais entregues com base no foco do teclado, como nas versões anteriores do Windows. No Windows 8.1, se o mouse estiver passeando sobre um aplicativo da loja, o mousewheel será entregue a esse aplicativo; Para fins de compatibilidade, no entanto, se o mouse estiver focalizando um aplicativo da área de trabalho, o mouse continuará a ser entregue com base no foco do teclado.

## <a name="manifestations"></a>Manifestações

Quando o mouse estiver passando o mouse sobre aplicativos da Store, o mouse rolará qualquer conteúdo aplicável sem que o usuário tenha que clicar no aplicativo da Store. Isso também se aplica à tela inicial. Isso torna a rolagem por mouse uma interação mais simples no Windows 8.1 do que no Windows 8.

## <a name="mitigation"></a>Atenuação

Na maior parte, essa alteração não deve ter nenhum impacto sobre os aplicativos existentes. Se um aplicativo da Store escutar eventos de mousewheel somente depois de registrar um evento de clique do mouse, esse aplicativo não terá a probabilidade de responder ao mouse até que o usuário tenha clicado ativamente nele. Consequentemente, a desvantagem mais provável aqui é simplesmente que um aplicativo continue a operar da mesma forma que no Windows 8. Para aplicativos da área de trabalho, ter o foco do teclado não oferece mais ao aplicativo uma entrada sobre o mouse, mas isso também não quebra esses aplicativos de forma alguma. Portanto, nenhuma mitigação de curto prazo é necessária.

## <a name="solution"></a>Solução

Os desenvolvedores de aplicativos da Loja devem esperar receber eventos de roda do mouse sem um evento de clique do mouse com o mouse. Eles não devem, por exemplo, escutar eventos de mousewheel somente depois de registrar um clique do mouse. Da mesma forma, os aplicativos da área de trabalho não devem tentar capturar eventos de mouse (por exemplo, definindo um gancho de baixo nível) quando eles têm o foco do teclado.

## <a name="tests"></a>Testes

Os desenvolvedores de aplicativos da Store devem testar Windows 8.1 verificar se todas as funcionalidades de rolagem funcionam sempre que o mouse estiver passe o mouse sobre o aplicativo. Os desenvolvedores de aplicativos da área de trabalho devem testar no Windows 8.1 para verificar se não estão capturando eventos de mouse (de acordo com as diretrizes acima).)

 

 




