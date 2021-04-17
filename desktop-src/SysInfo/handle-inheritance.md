---
description: Um processo filho pode herdar identificadores de seu processo pai. Um identificador herdado é válido somente no contexto do processo filho. Para habilitar um processo filho para herdar identificadores abertos de seu processo pai, use as etapas a seguir.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Manipular herança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755774"
---
# <a name="handle-inheritance"></a>Manipular herança

Um processo filho pode herdar identificadores de seu processo pai. Um identificador herdado é válido somente no contexto do processo filho. Para habilitar um processo filho para herdar identificadores abertos de seu processo pai, use as etapas a seguir.

1.  Crie o identificador com o membro **bInheritHandle** da estrutura [**de \_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) definida como **true**.
2.  Crie o processo filho usando a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , com o parâmetro *BInheritHandles* definido como **true**.

A função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) duplica um identificador a ser usado no processo atual ou em outro processo. Se um aplicativo duplicar um de seus identificadores para outro processo, o identificador duplicado será válido somente no contexto do outro processo.

Um identificador duplicado ou herdado é um valor exclusivo, mas se refere ao mesmo objeto que o identificador original. Os processos podem herdar ou duplicar identificadores para os seguintes tipos de objetos:

-   Token de acesso
-   Dispositivo de comunicações
-   Entrada do console
-   Buffer da tela do console
-   Área de trabalho
-   Diretório
-   Evento
-   Arquivo
-   Mapeamento de arquivo
-   Trabalho
-   Recepção
-   Mutex
-   Pipe
-   Processar
-   Chave do Registro
-   Sinal
-   Soquete
-   Thread
-   Temporizador
-   Estação de janela

Todos os outros objetos são privados ao processo que os criou; seus identificadores de objeto não podem ser duplicados ou herdados.

Para obter mais informações, consulte [Herança](/windows/desktop/ProcThread/inheritance).

 

 
