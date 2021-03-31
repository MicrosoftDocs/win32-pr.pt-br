---
title: Problemas comuns de integração para lojas de música online
description: Problemas comuns de integração para lojas de música online
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Lojas online do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f600d1035e0fd20be7786af4d4ffed4482138a72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641621"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>Problemas comuns de integração para lojas de música online

Aqui está uma lista de problemas comuns de integração do Windows Media Player que você deve tentar evitar. Qualquer um desses problemas pode fazer com que o armazenamento falhe no teste de validação. Com falha, a passagem RC2 adiará a inicialização até a próxima janela de inicialização disponível.

1.  Falha na transição de servidores de teste para servidores de produção
    -   Páginas ausentes
    -   Configurações do IIS (acesso, VRoots, HTTPS ou outras configurações de segurança)
    -   As contas de teste não funcionam mais.
    -   As contas de teste não têm créditos aplicados.
    -   Os logotipos hospedados do serviço não são movidos.
    -   As restrições de IP que foram convidadas anteriormente ocorrem novamente. Em particular, os sistemas de comércio eletrônico podem ter um conjunto diferente de restrições do site de música.
    -   O documento do serviceInfo não é atualizado para apontar para produção.
2.  O link comprar (ou o link de compras) na área em execução é inválido. Esse é um problema comumente ignorado e fará com que o armazenamento falhe mesmo quando todo o resto estiver em ordem de trabalho.
3.  Os testadores da Microsoft devem ter uma potência de compra adequada. A equipe de validação da Microsoft será executada por meio de vários cenários de compra que vão desde pequenas compras até compras muito grandes. Você deve fornecer uma maneira recarregáveis para que eles atuem como consumidores em sua loja. Isso pode variar desde o fornecimento de uma variedade de contas por meio do fornecimento de um cartão de crédito fictício. Por exemplo, um repositório falhará no RC2 se um testador de validação tentar comprar um álbum, mas tiver apenas crédito suficiente para comprar uma única faixa.
4.  Se você usar controles ActiveX dentro de suas páginas de serviço, certifique-se de que eles sejam instalados e desinstalados corretamente em todas as versões aplicáveis do Windows. A falha em fazer isso é um problema típico. Geralmente, os desenvolvedores e testadores em uma loja online têm os controles ActiveX registrados em seus próprios computadores, mas esquecem de instalar os controles no computador do usuário.

    Se a sua loja instala um plug-in ou um controle ActiveX, você deve fornecer ao usuário uma maneira fácil de desinstalá-lo. Por exemplo, a Microsoft descobriu recentemente que alguns lojas online instalaram controles ActiveX no Windows Media Player 11 para Windows Vista que não puderam ser removidos por meio do menu Adicionar/remover programas. Depois de alguma investigação, a Microsoft descobriu que os controles ActiveX poderiam ser removidos por meio do Gerenciador de Complementos no Internet Explorer. É importante que você se comunique (por meio de um arquivo de ajuda, pelo menos) a maneira de instalar e desinstalar os controles e plug-ins do ActiveX.

    Para obter mais informações sobre como integrar sua loja com a infraestrutura de segurança do Windows Vista, consulte o artigo intitulado ["práticas recomendadas para desenvolvedores e diretrizes para aplicativos em um ambiente menos privilegiado"](/previous-versions/aa905330(v=msdn.10)).

 

 