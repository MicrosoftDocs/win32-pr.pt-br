---
description: Os bloqueios oportunistas são solicitados abrindo primeiro um arquivo com permissões e sinalizadores apropriados para o aplicativo que abre o arquivo. Todos os arquivos para os quais os bloqueios oportunistas serão solicitados devem ser abertos para a operação sobreposta (assíncrona).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Como solicitar um bloqueio oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836999"
---
# <a name="how-to-request-an-opportunistic-lock"></a>Como solicitar um bloqueio oportunista

Os aplicativos cliente solicitam diretamente os bloqueios oportunistas somente quando o bloqueio é destinado a um arquivo no servidor local. Ao acessar arquivos em servidores remotos, ele é o redirecionador de rede, e não o aplicativo cliente, que solicita o bloqueio oportunista do servidor remoto.

Os bloqueios oportunistas são solicitados abrindo primeiro um arquivo com permissões e sinalizadores apropriados para o aplicativo que abre o arquivo. Todos os arquivos para os quais os bloqueios oportunistas serão solicitados devem ser abertos para a operação sobreposta (assíncrona). Depois que os arquivos forem abertos para operação sobreposta, use a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com o código de controle apropriado para solicitar um bloqueio oportunista. Para obter uma lista das operações de bloqueio oportunista, consulte [operações de bloqueio oportunista](opportunistic-lock-operations.md).

Os aplicativos são notificados de que um bloqueio oportunista é interrompido usando o membro **hEvent** da estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associada ao arquivo. Os aplicativos também podem usar funções como [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) e [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted). O aplicativo é responsável por associar o arquivo correto ao bloqueio oportunista rompido.

Para obter mais informações sobre notificação, consulte [sincronização](/windows/desktop/Sync/synchronization).

 

 
