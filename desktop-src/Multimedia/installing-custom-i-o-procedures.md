---
title: Instalando procedimentos personalizados de E/S
description: Instalando procedimentos personalizados de E/S
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- E/S de arquivo multimídia, procedimentos personalizados
- E/S de arquivo, procedimentos personalizados
- entrada e saída (E/S), procedimentos personalizados
- E/S (entrada e saída), procedimentos personalizados
- instalando procedimentos personalizados de E/S
- E/S personalizada
- Função mmioInstallIOProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ec92542efe80c24e1e620983d78b4b9a6c246ff003934a1ace1cae159fbd1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140455"
---
# <a name="installing-custom-io-procedures"></a>Instalando procedimentos personalizados de E/S

Para instalar um procedimento de E/S associado ao . Extensão de nome de arquivo ARC, use [**a função mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) da seguinte forma:


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Quando você instala um procedimento de E/S usando [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), o procedimento permanece instalado até que você o remova. O procedimento de E/S é usado para qualquer arquivo que você abrir, desde que o arquivo tenha a extensão de nome de arquivo apropriada.

Você também pode instalar temporariamente um procedimento de E/S usando a [**função mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) Nesse caso, o procedimento de E/S é usado apenas com um arquivo aberto usando **mmioOpen** e é removido quando o arquivo é fechado usando a [**função mmioClose.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) Para especificar um procedimento de E/S ao abrir um arquivo usando **mmioOpen**, use o parâmetro *lpmmioinfo* para referenciar uma [**estrutura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) da seguinte forma:

1.  De acordo **com o membro de yorkIOProc** como **NULL.**
2.  De definir **o membro pIOProc** como o endereço da instância de procedimento do procedimento de E/S.
3.  De definir todos os outros membros como zero (a menos que você esteja abrindo um arquivo de memória ou lendo ou escrevendo diretamente no buffer de E/S do arquivo).

Remova todos os procedimentos de E/S instalados antes de sair do aplicativo.

 

 