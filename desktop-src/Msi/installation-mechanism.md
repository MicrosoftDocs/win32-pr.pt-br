---
description: 'Há duas fases para um processo de instalação bem-sucedido: aquisição e execução. Se a instalação não for bem-sucedida, poderá ocorrer uma fase de reversão.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Mecanismo de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752041"
---
# <a name="installation-mechanism"></a>Mecanismo de instalação

Há duas fases para um processo de instalação bem-sucedido: aquisição e execução. Se a instalação não for bem-sucedida, poderá ocorrer uma fase de reversão.

## <a name="acquisition"></a>Aquisição

No início da fase de aquisição, um aplicativo ou um usuário instrui o instalador a instalar um recurso ou um aplicativo. Em seguida, o instalador progride pelas ações especificadas nas tabelas de sequência do banco de dados de instalação. Essas ações consultam o banco de dados de instalação e geram um script que fornece um procedimento passo a passo para a execução da instalação.

## <a name="execution"></a>Execução

Durante a fase de execução, o instalador passa as informações para um processo com privilégios elevados e executa o script.

## <a name="rollback"></a>Reversão

Se uma instalação não for bem-sucedida, o instalador restaurará o estado original do computador. Quando o instalador processa o script de instalação, ele gera um script de reversão simultaneamente. Além do script de reversão, o instalador salva uma cópia de cada arquivo que ele exclui durante a instalação. Esses arquivos são mantidos em um diretório de sistema oculto. Quando a instalação for concluída, o script de reversão e os arquivos salvos serão excluídos. Para obter mais informações, consulte [Rollback Installation](rollback-installation.md).

 

 



