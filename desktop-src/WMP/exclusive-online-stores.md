---
title: Repositórios online exclusivos
description: Repositórios online exclusivos
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player lojas online, exclusivo
- lojas online, exclusivo
- tipos 1 lojas online, exclusivo
- tipo 2 lojas online, exclusivo
- repositórios online exclusivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d199c47a201743ca56f9f9f199b5202bbdbe5fb320628afc5052b0ca8b969c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650086"
---
# <a name="exclusive-online-stores"></a>Repositórios online exclusivos

com o Windows Media Player 11, um aplicativo que incorpora o controle Player remotamente pode especificar um repositório online exclusivo. nesse caso, o seletor de serviço no Windows Media Player está desabilitado e apenas o repositório online especificado está disponível para o usuário. além disso, Windows Media Player adota a cor especificada pelo elemento **color** do documento de informações do repositório online exclusivo.

Para especificar um repositório online exclusivo, um aplicativo deve acrescentar ExclusiveService:*KeyName* ao final da cadeia de caracteres que ele retorna de [IWMPRemoteMediaServices:: getservicetype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Por exemplo, suponha que o Proseware seja o nome da chave fornecida para uma loja online específica. Se **Getservicetype** retornar a cadeia de caracteres "Remote ExclusiveService: Proseware", o Proseware será a única loja online disponível no controle player incorporado remotamente.

um aplicativo pode limitar Windows Media Player a um repositório online exclusivo somente se Windows Media Player ainda não estiver em execução quando o aplicativo for iniciado. é responsabilidade do aplicativo informar ao usuário que ele deve fechar Windows Media Player antes de executar o aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




