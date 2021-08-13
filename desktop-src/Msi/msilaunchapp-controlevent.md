---
description: Esse evento de controle executa um arquivo especificado. Se o arquivo não existir ou se o evento falhar, Windows Instalador registrará o erro no log detalhado sem exibir uma caixa de diálogo contendo uma mensagem de erro.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982152d58748ba8b1b8f9d302766e1e9c55eb2ee3c9fa0ce7582507c017dc9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627784"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent

Esse evento de controle executa um arquivo especificado. Se o arquivo não existir ou se o evento falhar, Windows Instalador registrará o erro no log detalhado sem exibir uma caixa de diálogo contendo uma mensagem de erro.

**[Windows Instalador 4.5 ou anterior:](not-supported-in-windows-installer-4-5.md)** Sem suporte. Este ControlEvent está disponível a partir do Windows Installer 5.0.

## <a name="published-by"></a>Publicada por

Este ControlEvent é publicado pelo instalador.

## <a name="argument"></a>Argumento

Os campos do valor do argumento são delimitados por espaços. O primeiro campo contém um valor de cadeia de caracteres que especifica o arquivo a ser executado. Use um valor de cadeia de caracteres de filekey para identificar o arquivo e substituir filekey pelo identificador do arquivo que aparece na coluna Arquivo \[ \#  \] da [tabela](file-table.md) Arquivo.  Todos os campos restantes do argumento podem conter parâmetros que estão sendo usados pelo arquivo que está sendo executado.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Este ControlEvent não executa nenhuma ação em assinantes.

## <a name="typical-use"></a>Usos comum

Para permitir que um usuário opte por executar um arquivo no final de uma instalação. Esse evento pode ser condicional em uma propriedade definida por um [controle CheckBox](checkbox-control.md) exibido na caixa de diálogo final da instalação. O controle CheckBox não deve ser exibido durante a remoção do pacote.

 

 



