---
title: Lojas Online Exclusivas
description: Lojas Online Exclusivas
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player online, exclusivas
- lojas online, exclusivas
- tipo 1 lojas online, exclusivas
- tipo 2 lojas online, exclusivas
- lojas online exclusivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d199c47a201743ca56f9f9f199b5202bbdbe5fb320628afc5052b0ca8b969c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650086"
---
# <a name="exclusive-online-stores"></a>Lojas Online Exclusivas

Com Windows Media Player 11, um aplicativo que incorpora o controle Player remotamente pode especificar uma loja online exclusiva. Nesse caso, o seletor de serviço Windows Media Player está desabilitado e apenas o armazenamento online especificado está disponível para o usuário. Além disso, Windows Media Player adota a cor especificada pelo elemento **Color** do documento ServiceInfo da loja online exclusiva.

Para especificar um armazenamento online exclusivo, um aplicativo deve anexar ExclusiveService:*keyname* ao final da cadeia de caracteres que ele retorna de [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Por exemplo, suponha que Proseware seja o nome da chave dado a uma loja online específica. Se **GetServiceType** retornar a cadeia de caracteres "Remote ExclusiveService:Proseware", o Proseware será o único armazenamento online disponível no controle player inserido remotamente.

Um aplicativo pode limitar Windows Media Player a um armazenamento online exclusivo somente se Windows Media Player ainda não estiver em execução quando o aplicativo for lançado. É responsabilidade do aplicativo informar ao usuário que ele deve fechar Windows Media Player antes de executar o aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online do tipo 1 e do tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




