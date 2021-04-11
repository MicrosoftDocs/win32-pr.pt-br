---
title: O sinalizador de teste
description: O sinalizador de teste
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- Sinalizador de MCI_TEST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292821"
---
# <a name="the-test-flag"></a>O sinalizador de teste

O sinalizador "teste" ( \_ teste MCI) consulta o dispositivo para determinar se ele pode executar o comando. O dispositivo retornará um erro se ele não puder executar o comando. Ele não retornará nenhum erro se puder manipular o comando. Quando você especifica esse sinalizador, o MCI retorna o controle para o aplicativo sem executar o comando.

Esse sinalizador tem suporte dos dispositivos de vídeo digital e VCR para todos os comandos, exceto [**abrir**](open.md) ([**MCI \_ aberto**](mci-open.md)) e [**Close**](close.md) ([**MCI, \_ fechar**](mci-close.md)).

 

 




