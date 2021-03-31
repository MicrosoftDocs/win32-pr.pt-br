---
description: Quando um arquivo é aberto por um processo usando a função CreateFile, um identificador de arquivo é associado a ele até que o processo seja encerrado ou o identificador seja fechado usando a função CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Identificadores de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837002"
---
# <a name="file-handles"></a>Identificadores de arquivo

Quando um arquivo é aberto por um processo usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , um *identificador de arquivo* é associado a ele até que o processo seja encerrado ou o identificador seja fechado usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . O identificador de arquivo é usado para identificar o arquivo em muitas chamadas de função.

Cada identificador de arquivo e objeto de arquivo é geralmente exclusivo para cada processo que abre um arquivo – as únicas exceções a isso são quando um identificador de arquivo mantido por um processo é duplicado ou quando um processo filho herda os identificadores de arquivo do processo pai. Nessas situações, esses identificadores de arquivo são exclusivos, mas vêem um único objeto de arquivo compartilhado. Consulte [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) para obter mais informações sobre como duplicar identificadores de arquivo mantidos por processos.

Observe que, embora os identificadores de arquivo sejam normalmente privados a um processo, os dados de arquivo aos quais os identificadores de arquivo apontam não são. Portanto, processos e threads que compartilham o mesmo arquivo devem sincronizar seu acesso. Para a maioria das operações em um arquivo, um processo identifica o arquivo por meio de seu pool de identificadores privado.

 

 
