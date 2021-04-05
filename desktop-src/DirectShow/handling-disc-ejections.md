---
description: Lidando com Ejetações de disco
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Lidando com Ejetações de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825472"
---
# <a name="handling-disc-ejections"></a>Lidando com Ejetações de disco

Quando o usuário ejeta um DVD da unidade, o navegador de DVD envia ao aplicativo uma \_ \_ mensagem ejetada no DVD do EC \_ . O aplicativo pode ignorar essa mensagem com segurança e permitir que o navegador de DVD gerencie o estado do grafo. Um aplicativo também pode manipular o \_ \_ método ejetado do disco DVD EC \_ para implementar o comportamento personalizado quando um disco é ejetado. Se você tratar a mensagem, deverá definir o sinalizador DVD \_ ResetOnStop como **true** com o método [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e, em seguida, chamar [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) antes de fechar o aplicativo ou reproduzir outro disco.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



