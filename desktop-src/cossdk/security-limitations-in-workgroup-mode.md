---
description: Limitações de segurança no modo de grupo de trabalho
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Limitações de segurança no modo de grupo de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af613b8de16b99090bcdb02bde0015d01312df3d642c895d61ef59ff80873eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546270"
---
# <a name="security-limitations-in-workgroup-mode"></a>Limitações de segurança no modo de grupo de trabalho

A configuração do grupo de trabalho do [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) não permite que o serviço de componentes em fila com+ ofereça suporte à segurança do aplicativo. Se você tiver instalado o enfileiramento de mensagens com a configuração de grupo de trabalho, deverá [desabilitar a segurança](specifying-the-authentication-protocol.md) em cada aplicativo em fila acessado nessa configuração selecionando não **autenticar mensagens** na guia **enfileiramento** da caixa de diálogo de **Propriedades** do aplicativo com+, usando a ferramenta administrativa serviços de componentes. Isso deve ser feito somente em uma rede confiável e deve ser feito no cliente e no servidor se o aplicativo já tiver sido exportado.

 

 



