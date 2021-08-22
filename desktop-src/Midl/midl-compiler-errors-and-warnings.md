---
title: Erros e avisos do compilador MIDL
description: Ao usar o compilador MIDL, erros e avisos podem ser causados pelo uso inadequado das opções de linha de comando ou pelo conteúdo dos arquivos IDL e ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- linguagem IDL da Microsoft MIDL, referência
- MIDL compiler MIDL , erros
- compiler MIDL , erros
- erros MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f6c2dfd830a1240e2af107eb4a3f1799eafcd0de35ccec7f3756b3e9de5bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146399"
---
# <a name="midl-compiler-errors-and-warnings"></a>Erros e avisos do compilador MIDL

Ao usar o compilador MIDL, erros e avisos podem ser causados pelo uso inadequado das opções de linha de comando ou pelo conteúdo dos arquivos IDL e ACF. Se o erro for devido à inserção incorreta das opções de linha de comando, um erro ou mensagem de aviso poderá especificar o nome de uma ou mais opções de modo do compilador MIDL. Por exemplo, você pode incluir determinados atributos do ACF em um arquivo IDL ao usar a opção de configuração **/app, \_** mas esse arquivo IDL gerará um erro se você compilar sem usar a opção de configuração **/app. \_**

Os erros nos arquivos IDL e ACF se enquadram em duas categorias: erros capturados pelo pré-processador e erros reconhecidos pelo compilador. Esta seção lista as mensagens de erro do pré-processador MIDL e do compilador. Ele também descreve seus formatos e causas.

-   [Formatos de mensagem de erro e aviso](error-and-warning-message-formats.md)
-   [Erros de pré-processador](preprocessor-errors.md)
-   [Erros do compilador](compiler-errors.md)

 

 




