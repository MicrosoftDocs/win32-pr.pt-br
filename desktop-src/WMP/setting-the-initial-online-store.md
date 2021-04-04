---
title: Configurando a loja online inicial
description: Configurando a loja online inicial
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Lojas online do Windows Media Player, configurando lojas online iniciais
- lojas online, configurando lojas online iniciais
- Digite 1 lojas online, configurando lojas online iniciais
- tipo 2 lojas online, configurando lojas online iniciais
- Lojas online do Windows Media Player, primeira loja online exibida
- lojas online, primeira loja online exibida
- Digite 1 lojas online, primeira loja online exibida
- Digite 2 lojas online, primeira loja online exibida
- primeira loja online exibida
- Configurando lojas online iniciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822856"
---
# <a name="setting-the-initial-online-store"></a>Configurando a loja online inicial

Para obter detalhes sobre como redistribuir o software do Windows Media Player com seu aplicativo, consulte [redistribuindo o software do Windows Media Player](redistributing-windows-media-player-software.md).

Quando um usuário instala o Windows Media Player pela primeira vez, o aplicativo de instalação define o repositório online ativo inicial como um padrão escolhido pela Microsoft. Os OEMs (fabricantes de equipamentos originais) do computador pessoal podem optar por alterar essa configuração.

Para especificar e configurar a primeira loja online que o usuário vê quando instala o Windows Media Player, você deve:

-   Crie um documento do serviceInfo que você instale no disco rígido do usuário. Este documento contém as informações sobre como configurar o repositório online ativo inicial.
-   Acrescente um conjunto de parâmetros de linha de comando ao executar o aplicativo de instalação.

Há três cenários para instalar o Windows Media Player e configurar o repositório online inicial. As seções a seguir fornecem mais detalhes sobre cada cenário:

-   [Instalando enquanto estiver offline](installing-while-offline.md)
-   [Instalando de um CD enquanto estiver online](installing-from-a-cd-while-online.md)
-   [Instalando a partir da Web enquanto estiver online](installing-from-the-web-while-online.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Parâmetros de linha de comando de instalação para lojas online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




