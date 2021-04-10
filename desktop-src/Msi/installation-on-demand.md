---
description: Com a tecnologia de instalação tradicional, é necessário sair de um aplicativo e executar novamente a instalação para executar uma tarefa de instalação.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Instalação sob demanda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f25c83135a0497d09aa0a7800a1272105d0db1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169854"
---
# <a name="installation-on-demand"></a>Instalação sob demanda

Com a tecnologia de instalação tradicional, é necessário sair de um aplicativo e executar novamente a instalação para executar uma tarefa de instalação. Isso normalmente ocorre quando um usuário queria um recurso ou produto não escolhido durante a primeira execução da instalação. Isso geralmente tornou o processo de configuração de produto ineficiente porque ele exigia que o usuário antecipasse a funcionalidade necessária antes de usar o produto.

A instalação sob demanda torna possível oferecer funcionalidade a usuários e aplicativos na ausência dos próprios arquivos. Essa noção é conhecida como anúncio. O Windows Installer tem a capacidade de anunciar a funcionalidade e tornar possível a instalação sob demanda de recursos do aplicativo ou de produtos inteiros. Quando um usuário ou aplicativo ativa um recurso ou produto anunciado, o instalador prossegue com a instalação dos componentes necessários. Isso reduz o processo de configuração, pois outras funcionalidades podem ser acessadas sem a necessidade de sair e executar novamente outro procedimento de instalação.

Quando um produto usa o instalador, um usuário pode escolher no momento da configuração quais recursos ou aplicativos instalar e quais anunciar. Em seguida, se durante a execução de um aplicativo o usuário solicitar um recurso anunciado que ainda não tenha sido instalado, o aplicativo chamará o instalador para aplicar uma instalação de nível de recurso just-in-time dos arquivos necessários. Se o usuário ativar um produto anunciado que ainda não foi instalado, o sistema operacional chamará o instalador para aplicar uma instalação de nível de produto just-in-time.

O [anúncio](advertisement.md) e a instalação sob demanda também podem facilitar o gerenciamento do sistema, permitindo que os administradores designem aplicativos conforme necessário ou opcionais para diferentes grupos de usuários. Há dois tipos de publicidade conhecidos como "atribuição" e "publicação". Se um administrador atribuir um aplicativo a um grupo, esses usuários poderão instalar o aplicativo sob demanda. No entanto, se o administrador publicar o aplicativo no grupo, nenhum ponto de entrada aparecerá para esses usuários e a instalação sob demanda será ativada somente se outro aplicativo ativar o aplicativo publicado.

 

 



