---
title: Requisitos HTTP para downloads de BITS
description: O BITS dá suporte a downloads e uploads HTTP e HTTPS e requer que o servidor seja compatível com o protocolo HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9bd997bb5ef7f2125cfe7c3dc6850c0f44e81a8c3138f7f130952e31202a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010871"
---
# <a name="http-requirements-for-bits-downloads"></a>Requisitos HTTP para downloads de BITS

O BITS dá suporte a downloads e uploads HTTP e HTTPS e requer que o servidor seja compatível com o protocolo HTTP/1.1. Para downloads, o método  Head do servidor HTTP deve retornar o tamanho do arquivo e seu método **Get** deve dar suporte aos cabeçalhos Content-Range e Content-Length. Como resultado, o BITS transfere apenas o conteúdo do arquivo estático e gera um erro se você tentar transferir conteúdo dinâmico, a menos que o script ASP, ISAPI ou CGI seja compatível com os headers Content-Range e Content-Length.

O BITS pode usar um servidor HTTP/1.0, desde que atenda aos requisitos do método **Head** e **Get.**

Para dar suporte ao download de intervalos de um arquivo, o servidor deve dar suporte aos seguintes requisitos:

-   Permita que os headers MIME incluam os headers padrão Content-Range e Content-Type, além de um máximo de 180 bytes de outros títulos.
-   Permita um máximo de dois CR/LFs entre os cabeçalhos HTTP e a primeira cadeia de caracteres de limite.

 

 




