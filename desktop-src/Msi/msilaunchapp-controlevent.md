---
description: Esse evento de controle executa um arquivo especificado. Se o arquivo não existir ou se o evento falhar, Windows Installer registrará o erro no log detalhado sem exibir uma caixa de diálogo contendo uma mensagem de erro.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748150"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent,

Esse evento de controle executa um arquivo especificado. Se o arquivo não existir ou se o evento falhar, Windows Installer registrará o erro no log detalhado sem exibir uma caixa de diálogo contendo uma mensagem de erro.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esse ControlEvent, está disponível a partir do Windows Installer 5,0.

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Os campos do valor do argumento são delimitados por espaços. O primeiro campo contém um valor de cadeia de caracteres que especifica o arquivo a ser executado. Use um valor de cadeia de caracteres de \[ \# *FileKey* \] para identificar o arquivo e substitua *FileKey* pelo identificador do arquivo que aparece na coluna arquivo da tabela de [arquivos](file-table.md) . Todos os campos restantes do argumento podem conter parâmetros que estão sendo usados pelo arquivo que está sendo executado.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa ações em assinantes.

## <a name="typical-use"></a>Usos comum

Para permitir que um usuário escolha Executar um arquivo no final de uma instalação. Esse evento pode ser condicionado em uma propriedade definida por um controle de [caixa de seleção](checkbox-control.md) exibido na caixa de diálogo final da instalação. O controle de caixa de seleção não deve ser exibido durante a remoção do pacote.

 

 



