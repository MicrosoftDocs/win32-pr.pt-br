---
title: Erros e avisos do compilador MIDL
description: Ao usar o compilador MIDL, erros e avisos podem ser causados pelo uso impróprio das opções de linha de comando ou pelo conteúdo dos arquivos IDL e ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- MIDL linguagem IDL da Microsoft, referência
- MIDL do compilador MIDL, erros
- MIDL do compilador, erros
- MIDL de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822156"
---
# <a name="midl-compiler-errors-and-warnings"></a>Erros e avisos do compilador MIDL

Ao usar o compilador MIDL, erros e avisos podem ser causados pelo uso impróprio das opções de linha de comando ou pelo conteúdo dos arquivos IDL e ACF. Se o erro for devido à inserção inadequada das opções de linha de comando, uma mensagem de erro ou de aviso poderá especificar o nome de uma ou mais opções do modo de compilador MIDL. Por exemplo, você pode incluir certos atributos de ACF em um arquivo IDL ao usar a opção **/ \_ configuração de aplicativo** , mas esse arquivo IDL gerará um erro se você compilar sem usar a opção/**\_ configuração de aplicativo** .

Os erros nos arquivos IDL e ACF se enquadram em duas categorias: erros capturados pelo pré-processador e erros reconhecidos pelo compilador. Esta seção lista o pré-processador de MIDL e as mensagens de erro do compilador. Ele também descreve seus formatos e causas.

-   [Formatos de mensagem de erro e de aviso](error-and-warning-message-formats.md)
-   [Erros de pré-processador](preprocessor-errors.md)
-   [Erros do compilador](compiler-errors.md)

 

 




