---
title: Entrada MouseWheel para Windows 8.1
description: Entrada MouseWheel para Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822465"
---
# <a name="mousewheel-input-for-windows-81"></a>Entrada MouseWheel para Windows 8.1

## <a name="platform"></a>Plataforma

<dl> Clientes-Windows 8.1  
Servidores-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Em Windows 8.1, os eventos MouseWheel não são mais entregues com base no foco do teclado como nas versões anteriores do Windows. Em Windows 8.1, se o mouse estiver focalizando um aplicativo da loja, o MouseWheel será entregue a esse aplicativo; para fins de compatibilidade, no entanto, se o mouse estiver focalizando um aplicativo de área de trabalho, o MouseWheel continuará a ser entregue com base no foco do teclado.

## <a name="manifestations"></a>Manifestações

Quando o mouse estiver focalizando os aplicativos da loja, o MouseWheel rolará qualquer conteúdo aplicável sem que o usuário precise clicar no aplicativo da loja. Isso também se aplica à tela inicial. Isso torna a rolagem por MouseWheel uma interação mais simples em Windows 8.1 do que no Windows 8.

## <a name="mitigation"></a>Atenuação

Na maior parte, essa alteração não deve ter nenhum impacto sobre os aplicativos existentes. Se um aplicativo da loja tiver escutado por eventos MouseWheel somente depois de ter registrado um evento de clique do mouse, esse aplicativo não provavelmente responderia ao MouseWheel até que o usuário o tenha clicado ativamente. Consequentemente, a desvantagem mais provável aqui é simplesmente que um aplicativo continua a operar da mesma forma que no Windows 8. Para aplicativos da área de trabalho, o foco do teclado não dá mais ao aplicativo uma monopolização da entrada MouseWheel, mas isso também não faz nenhum tipo de quebra desses aplicativos. Portanto, nenhuma mitigação de curto prazo é necessária.

## <a name="solution"></a>Solução

Os desenvolvedores de aplicativos da loja devem esperar receber eventos MouseWheel sem um evento de clique do mouse com o cursor. Eles não devem, por exemplo, escutar eventos MouseWheel somente depois de registrar um clique do mouse. Da mesma forma, os aplicativos de área de trabalho não devem tentar capturar eventos MouseWheel (por exemplo, definindo um gancho de nível baixo) quando têm o foco do teclado.

## <a name="tests"></a>Testes

Os desenvolvedores de aplicativos da loja devem testar Windows 8.1 para verificar se toda a funcionalidade de rolagem funciona sempre que o mouse está focalizando o aplicativo. Os desenvolvedores de aplicativos de desktop devem testar Windows 8.1 para verificar se eles não estão capturando eventos MouseWheel (segundo diretrizes acima).

 

 




