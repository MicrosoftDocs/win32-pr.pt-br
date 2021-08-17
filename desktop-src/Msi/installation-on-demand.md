---
description: Com a tecnologia de instalação tradicional, é necessário sair de um aplicativo e executar a instalação de novo para executar uma tarefa de instalação.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Instalação sob demanda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd20f83465fa110c4f749c6f11ba5ece1c6797a521174a8caebb9d152740aaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633865"
---
# <a name="installation-on-demand"></a>Instalação sob demanda

Com a tecnologia de instalação tradicional, é necessário sair de um aplicativo e executar a instalação de novo para executar uma tarefa de instalação. Isso normalmente ocorreu quando um usuário queria um recurso ou produto não escolhido durante a primeira operação de instalação. Isso geralmente tornou o processo de configuração do produto ineficiente porque exigia que o usuário antecipava a funcionalidade necessária antes de usar o produto.

A instalação sob demanda possibilita oferecer funcionalidade a usuários e aplicativos na ausência dos próprios arquivos. Essa noção é conhecida como anúncio. O Windows instalador tem a capacidade de anunciar a funcionalidade e tornar a instalação sob demanda de recursos do aplicativo ou produtos inteiros possíveis. Quando um usuário ou aplicativo ativa um recurso ou produto anunciado, o instalador continua com a instalação dos componentes necessários. Isso reduz o processo de configuração porque a funcionalidade adicional pode ser acessada sem precisar sair e reprisar outro procedimento de instalação.

Quando um produto usa o instalador, um usuário pode escolher no momento da instalação quais recursos ou aplicativos instalar e quais anunciar. Em seguida, se durante a execução de um aplicativo o usuário solicitar um recurso anunciado que ainda não foi instalado, o aplicativo chamará o instalador para executar uma instalação just-in-time do nível de recurso dos arquivos necessários. Se o usuário ativar um produto anunciado que ainda não foi instalado, o sistema operacional chamará o instalador para acionar uma instalação just-in-time no nível do produto.

[O](advertisement.md) anúncio e a instalação sob demanda também podem facilitar o gerenciamento do sistema, permitindo que os administradores designem aplicativos conforme necessário ou opcional para diferentes grupos de usuários. Há dois tipos de publicidade conhecidos como "atribuindo" e "publicação". Se um administrador atribuir um aplicativo a um grupo, esses usuários poderão instalar o aplicativo sob demanda. No entanto, se o administrador publicar o aplicativo no grupo, nenhum ponto de entrada aparecerá para esses usuários e a instalação sob demanda só será ativada se outro aplicativo ativar o aplicativo publicado.

 

 



