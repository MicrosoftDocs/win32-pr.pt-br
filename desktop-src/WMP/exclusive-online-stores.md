---
title: Repositórios online exclusivos
description: Repositórios online exclusivos
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Armazenamentos online do Windows Media Player, exclusivo
- lojas online, exclusivo
- tipos 1 lojas online, exclusivo
- tipo 2 lojas online, exclusivo
- repositórios online exclusivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105813162"
---
# <a name="exclusive-online-stores"></a>Repositórios online exclusivos

Com o Windows Media Player 11, um aplicativo que incorpora o controle Player remotamente pode especificar um repositório online exclusivo. Nesse caso, o seletor de serviço no Windows Media Player é desabilitado e apenas o repositório online especificado está disponível para o usuário. Além disso, o Windows Media Player adota a cor especificada pelo elemento **Color** do documento de informações do repositório online exclusivo.

Para especificar um repositório online exclusivo, um aplicativo deve acrescentar ExclusiveService:*KeyName* ao final da cadeia de caracteres que ele retorna de [IWMPRemoteMediaServices:: getservicetype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Por exemplo, suponha que o Proseware seja o nome da chave fornecida para uma loja online específica. Se **Getservicetype** retornar a cadeia de caracteres "Remote ExclusiveService: Proseware", o Proseware será a única loja online disponível no controle player incorporado remotamente.

Um aplicativo pode limitar o Windows Media Player a um repositório online exclusivo somente se o Windows Media Player ainda não estiver em execução quando o aplicativo for iniciado. É responsabilidade do aplicativo informar ao usuário que ele deve fechar o Windows Media Player antes de executar o aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




