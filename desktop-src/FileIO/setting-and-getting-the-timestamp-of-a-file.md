---
description: Os aplicativos podem recuperar e definir a data e a hora em que um arquivo é criado, modificado pela última vez ou acessado pela última vez usando as funções GetFileTime e SetFileTime.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Configurando e obtendo o carimbo de data/hora de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34735994dd3017662f517a8c0a57be1d5c0e3096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164645"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a>Configurando e obtendo o carimbo de data/hora de um arquivo

Os aplicativos podem recuperar e definir a data e a hora em que um arquivo é criado, modificado pela última vez ou acessado pela última vez usando as funções [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) e [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) . Para obter mais informações, consulte [horas de arquivo](/windows/desktop/SysInfo/file-times).

> [!Note]  
> Nem todos os sistemas de arquivos podem registrar a criação e os últimos tempos de acesso, e nem todos os sistemas de arquivos os registram da mesma maneira. Por exemplo, no sistema de arquivos FAT, a criação de tempo tem uma resolução de 10 milissegundos, o tempo de gravação tem uma resolução de 2 segundos e o tempo de acesso tem uma resolução de 1 dia (na verdade, a data de acesso). O sistema de arquivos NTFS atrasa a atualização para o último horário de acesso de um arquivo em até uma hora após o último acesso.

 

 

 
