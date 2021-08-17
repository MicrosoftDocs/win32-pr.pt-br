---
description: 'Há duas fases para um processo de instalação bem-sucedido: aquisição e execução. Se a instalação não for bem-sucedida, poderá ocorrer uma fase de reversão.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Mecanismo de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bce4396701ab5cddb43a67dddbafd1e8310092d04d779af04ad7876681cc3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634214"
---
# <a name="installation-mechanism"></a>Mecanismo de instalação

Há duas fases para um processo de instalação bem-sucedido: aquisição e execução. Se a instalação não for bem-sucedida, poderá ocorrer uma fase de reversão.

## <a name="acquisition"></a>Aquisição

No início da fase de aquisição, um aplicativo ou um usuário instrui o instalador a instalar um recurso ou um aplicativo. Em seguida, o instalador progride pelas ações especificadas nas tabelas de sequência do banco de dados de instalação. Essas ações consultam o banco de dados de instalação e geram um script que fornece um procedimento passo a passo para a execução da instalação.

## <a name="execution"></a>Execução

Durante a fase de execução, o instalador passa as informações para um processo com privilégios elevados e executa o script.

## <a name="rollback"></a>Reversão

Se uma instalação não for bem-sucedida, o instalador restaurará o estado original do computador. Quando o instalador processa o script de instalação, ele gera um script de reversão simultaneamente. Além do script de reversão, o instalador salva uma cópia de cada arquivo que ele exclui durante a instalação. Esses arquivos são mantidos em um diretório de sistema oculto. Quando a instalação for concluída, o script de reversão e os arquivos salvos serão excluídos. Para obter mais informações, consulte [Rollback Installation](rollback-installation.md).

 

 



