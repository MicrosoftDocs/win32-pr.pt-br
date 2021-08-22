---
title: Serviços personalizados
description: Serviços personalizados
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- e/s de arquivo multimídia, serviços personalizados
- e/s de arquivo, serviços personalizados
- entrada e saída (e/s), serviços personalizados
- E/s (entrada e saída), serviços personalizados
- e/s personalizada
- função mmioInstallIOProc
- função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c2418d3a87669527feda37547674bee83175dd6e4533312e8b89c346048c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144569"
---
# <a name="custom-services"></a>Serviços personalizados

Os serviços de e/s de arquivo de multimídia usam os procedimentos de e/s para lidar com a entrada física e a saída associada à leitura e gravação em diferentes tipos de sistemas de armazenamento, como sistemas de arquivamento de arquivos e de armazenamento de banco de dados. Os procedimentos de e/s predefinidos existem para os sistemas de arquivos padrão e para os arquivos de memória, mas você pode fornecer um procedimento de e/s personalizado para acessar um sistema de armazenamento exclusivo usando a função [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .

Para abrir um arquivo usando um procedimento de e/s personalizado, use a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Inclua um sinal de adição (+) ou a constante CFSEPCHAR no nome de arquivo para separar o nome do arquivo físico do nome do elemento do arquivo que você deseja abrir. O exemplo a seguir abre um elemento file chamado "element" de um arquivo chamado FILENAME. ARCO


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



Quando o Gerenciador de e/s de arquivos encontra um sinal de adição em um nome de arquivo, ele examina a extensão de nome de arquivo para determinar qual procedimento de e/s associar ao arquivo. No exemplo anterior, o Gerenciador de e/s de arquivo tentaria usar o procedimento de e/s associado ao. Extensão de nome de arquivo ARC; Esse procedimento de e/s teria sido instalado usando [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc). Se nenhum procedimento de e/s for instalado, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) retornará um erro.

Os procedimentos de e/s devem responder às seguintes mensagens:

-   [**MMIOM \_ fechar**](mmiom-close.md)
-   [**MMIOM \_ abrir**](mmiom-open.md)
-   [**MMIOM \_ leitura**](mmiom-read.md)
-   [**MMIOM \_ gravação**](mmiom-write.md)
-   [**MMIOM \_ Seek**](mmiom-seek.md)
-   [**\_renomear MMIOM**](mmiom-rename.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)

Você também pode criar mensagens personalizadas e enviá-las para o procedimento de e/s usando a função [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) . Se você definir suas próprias mensagens, verifique se elas estão definidas no valor definido pela constante de usuário do MMIOM ou acima dele \_ .

Além de processar mensagens, um procedimento de e/s deve manter o membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (apontado pelo parâmetro *lpmmioinfo* da função **mmioOpen** ). O membro **lDiskOffset** sempre deve conter o deslocamento do arquivo para o local que a próxima MMIOM \_ leitura ou a mensagem de gravação de MMIOM \_ será acessada. O deslocamento é especificado em bytes e é relativo ao início do arquivo. O procedimento de e/s pode usar o membro **adwInfo** para manter qualquer informação de estado necessária. O procedimento de e/s não deve modificar nenhum outro membro na estrutura **MMIOINFO** .

 

 