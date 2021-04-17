---
title: Instalando procedimentos de e/s personalizados
description: Instalando procedimentos de e/s personalizados
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- e/s de arquivo multimídia, procedimentos personalizados
- e/s de arquivo, procedimentos personalizados
- entrada e saída (e/s), procedimentos personalizados
- E/s (entrada e saída), procedimentos personalizados
- Instalando procedimentos de e/s personalizados
- e/s personalizada
- função mmioInstallIOProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366004"
---
# <a name="installing-custom-io-procedures"></a>Instalando procedimentos de e/s personalizados

Para instalar um procedimento de e/s associado ao. Extensão de nome de arquivo ARC, use a função [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) da seguinte maneira:


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Quando você instala um procedimento de e/s usando o [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), o procedimento permanece instalado até você removê-lo. O procedimento de e/s é usado para qualquer arquivo que você abrir, desde que o arquivo tenha a extensão de nome de arquivo apropriada.

Você também pode instalar temporariamente um procedimento de e/s usando a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Nesse caso, o procedimento de e/s é usado apenas com um arquivo aberto usando **mmioOpen** e é removido quando o arquivo é fechado usando a função [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) . Para especificar um procedimento de e/s ao abrir um arquivo usando **mmioOpen**, use o parâmetro *lpmmioinfo* para fazer referência a uma estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) da seguinte maneira:

1.  Defina o membro **fccIOProc** como **nulo**.
2.  Defina o membro **pIOProc** para o endereço de instância de procedimento do procedimento de e/s.
3.  Defina todos os outros membros como zero (a menos que você esteja abrindo um arquivo de memória ou lendo diretamente ou gravando no buffer de e/s de arquivo).

Certifique-se de remover os procedimentos de e/s que você instalou antes de sair do aplicativo.

 

 