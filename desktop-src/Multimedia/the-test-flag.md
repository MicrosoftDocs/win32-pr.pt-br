---
title: O sinalizador de teste
description: O sinalizador de teste
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST sinalizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837b7812a904ed39fa0350d703b1525bbffa6f981b4736d25927840395932f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801469"
---
# <a name="the-test-flag"></a>O sinalizador de teste

O sinalizador "test" (MCI \_ TEST) consulta o dispositivo para determinar se ele pode executar o comando. O dispositivo retornará um erro se não puder executar o comando. Ele não retornará nenhum erro se puder manipular o comando. Quando você especifica esse sinalizador, a MCI retorna o controle para o aplicativo sem executar o comando.

Esse sinalizador é compatível com dispositivos de vídeo digital e VCR para todos os comandos, exceto [**abrir**](open.md) ([**MCI \_ OPEN**](mci-open.md)) e [**fechar**](close.md) ([**MCI \_ CLOSE**](mci-close.md)).

 

 




