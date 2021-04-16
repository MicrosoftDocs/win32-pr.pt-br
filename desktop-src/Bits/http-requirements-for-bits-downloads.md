---
title: Requisitos de HTTP para downloads de BITS
description: O BITS dá suporte a downloads e uploads de HTTP e HTTPS e requer que o servidor ofereça suporte ao protocolo HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453527"
---
# <a name="http-requirements-for-bits-downloads"></a>Requisitos de HTTP para downloads de BITS

O BITS dá suporte a downloads e uploads de HTTP e HTTPS e requer que o servidor ofereça suporte ao protocolo HTTP/1.1. Para downloads, o método **Head** do servidor http deve retornar o tamanho do arquivo e seu método **Get** deve oferecer suporte aos cabeçalhos Content-Range e Content-Length. Como resultado, o BITS transfere apenas o conteúdo do arquivo estático e gera um erro se você tentar transferir conteúdo dinâmico, a menos que o script ASP, ISAPI ou CGI dê suporte aos cabeçalhos Content-Range e Content-Length.

O BITS pode usar um servidor HTTP/1.0 contanto que atenda aos requisitos de método **Head** e **Get** .

Para dar suporte ao download de intervalos de um arquivo, o servidor deve dar suporte aos seguintes requisitos:

-   Permitir que os cabeçalhos MIME incluam o intervalo de conteúdo padrão e os cabeçalhos de tipo de conteúdo, mais um máximo de 180 bytes de outros cabeçalhos.
-   Permita um máximo de dois CR/LFs entre os cabeçalhos HTTP e a primeira cadeia de caracteres de limite.

 

 




