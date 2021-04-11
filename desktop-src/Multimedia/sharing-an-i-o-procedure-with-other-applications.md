---
title: Compartilhando um procedimento de e/s com outros aplicativos
description: Compartilhando um procedimento de e/s com outros aplicativos
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- e/s de arquivo multimídia, procedimentos compartilhados
- e/s de arquivo, procedimentos compartilhados
- entrada e saída (e/s), procedimentos compartilhados
- E/s (entrada e saída), procedimentos compartilhados
- compartilhando procedimentos de e/s com outros aplicativos
- função mmioInstallIOProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365894"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a>Compartilhando um procedimento de e/s com outros aplicativos

Se desejar compartilhar um procedimento de e/s com outros aplicativos, você precisará gravar uma DLL (biblioteca de vínculo dinâmico) para seu aplicativo. Você pode compartilhar o procedimento de e/s seguindo um destes procedimentos:

-   Inclua o código para o procedimento de e/s na DLL.
-   Crie uma função na DLL que chama a função [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) para instalar o procedimento de e/s.
-   Exporte essa função no arquivo de definições de módulo da DLL.

Para usar o procedimento de e/s compartilhado, um aplicativo deve primeiro chamar a função na DLL para instalar o procedimento de e/s.

 

 