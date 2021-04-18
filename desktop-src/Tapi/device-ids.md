---
description: Outras funções de telefone TAPI usam um identificador para um dispositivo de telefone aberto para identificar o dispositivo de telefone aberto.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: IDs de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759477"
---
# <a name="device-ids"></a>IDs de dispositivo

Outras funções de telefone TAPI usam um identificador para um dispositivo de telefone aberto para identificar o dispositivo de telefone aberto. As únicas funções para dispositivos de telefone que usam um parâmetro de identificador de dispositivo de telefone (em oposição a um identificador de telefone) são as funções [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) . Um aplicativo pode recuperar o identificador de dispositivo do telefone usando a função [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) com o identificador de telefone como um parâmetro.

Um aplicativo também pode obter identificadores de dispositivo para várias classes de dispositivo associadas a um telefone aberto invocando [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid). Consulte [classes de dispositivo TAPI](tapi-device-classes.md) para nomes de classe de dispositivo.

Essa função usa um identificador de telefone e uma descrição de classe de dispositivo. Ele retorna o identificador de dispositivo para o dispositivo da classe de dispositivo fornecida que está associada ao dispositivo de telefone aberto. Se a classe de dispositivo for "TAPI/telefone", o identificador de dispositivo do dispositivo de telefone será retornado.

Em contraste com os dispositivos de linha, para os quais os serviços de linha básica fornecem o equivalente de POTS, nenhum conjunto mínimo garantido de funções é definido para dispositivos de telefone. Embora cada dispositivo de telefone forneça pelo menos as funções e mensagens descritas nesta seção, eles não oferecem nenhuma operação real no dispositivo de telefone físico.

 

 



