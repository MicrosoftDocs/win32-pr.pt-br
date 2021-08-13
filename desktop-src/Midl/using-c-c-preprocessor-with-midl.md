---
title: Usando C/C++-pré-processador com MIDL
description: O compilador MIDL não processa arquivos de origem.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL do compilador MIDL, pré-processador C
- MIDL de pré-processador C-pré-processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac3952a342b101f0366d2bce8810426e758c4aa5b32fa267e685bc6d658f034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382790"
---
# <a name="using-cc-preprocessor-with-midl"></a>Usando C/C++-pré-processador com MIDL

O compilador MIDL não processa arquivos de origem. Em vez disso, o compilador MIDL usa um pré-processador disponível para preparar o fluxo de entrada para análise. Por padrão, o MIDL usa o pré-processador para o compilador C/C++ da Microsoft a partir do mesmo ambiente de compilação que MIDL. O usuário pode indicar um pré-processador diferente a ser usado pelo MIDL, se necessário.

O MIDL gera execuções de pré-processador separadas para arquivos IDL e ACF de nível superior e para cada arquivo importado com a diretiva de importação MIDL. Os arquivos incluídos na diretiva **\# include** são tratados diretamente pelo pré-processador.

Os tópicos a seguir descrevem vários aspectos das interações de pré-processamento de MIDL:

-   [Requisitos de pré-processador do C para MIDL](c-preprocessor-requirements-for-midl.md)
-   [Verificando opções de pré-processador](verifying-preprocessor-options.md)
-   [Salvando a saída do pré-processador](saving-preprocessor-output.md)
-   [Lidando com as \# definições em arquivos IDL](dealing-with-defines-in-idl-files-2.md)

 

 




