---
title: Salvando a saída do pré-processador
description: A exibição da saída do pré-processador pode ser um método de solução de problemas eficaz, como quando ocorrem erros de pré-processador IDL, C ou C inválidos ou quando valores -D na linha de comando MIDL resultam em erros de notificação midl.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL compiler MIDL , salvando a saída do pré-processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f016885ac4d669d7b62eaf3ff1d5ee3154f03d5eae64fca5f63c6111dff4c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641371"
---
# <a name="saving-preprocessor-output"></a>Salvando a saída do pré-processador

A exibição da saída do pré-processador pode ser um método de solução de problemas eficaz, como quando ocorrem erros de pré-processador IDL, C ou C inválidos ou quando valores -D na linha de comando MIDL resultam em erros de notificação midl. Os desenvolvedores também podem querer examinar a saída do pré-processador para determinar quais arquivos e definições estavam presentes no fluxo de entrada do compilador, como quando um caso difícil de conflito de redefinição de tipo deve ser resolvido. Ou, menos comumente, determinados desenvolvedores podem querer forçar comutadores privados no pré-processador com [**/cpp \_ opt**](-cpp-opt.md)ou talvez queira ver como as opções funcionam.

A maneira mais fácil e menos obtusiva de obter os arquivos pré-processados de uma executar de compilação MIDL é usar a [**opção -savePP.**](-savepp.md) A **opção -savePP** simplesmente impede que MIDL extinga os arquivos temporários que o pré-processador passa de volta para MIDL. Considere o seguinte:

**midl -savePP -Id: \\ nt \\ public \\ sdk \\ inc -DNTENV=1 -Oicf -env win32 stub.idl**

Essa diretiva compila Stub.idl, mas preserva todos os arquivos de pré-processador.

> [!Note]  
> MIDL gera as executações de pré-processador separadas para arquivo IDL e ACF (se presente), bem como para cada arquivo importado.

 

Para uma compilação DCOM, vários arquivos de pré-processador normalmente são produzidos, mesmo que sejam processados pelo MIDL como um fluxo de entrada contíguo virtual. Em um ambiente Windows programação comum, os arquivos temporários podem ser encontrados no diretório Temp como nomes de arquivo, como MID \* .tmp. Se preservar a saída do pré-processador, é uma boa prática observar os arquivos recentes no diretório Temp para identificar quais arquivos estão associados a qual pré-processador é executado.

Em casos simples, como quando o arquivo IDL compilado não importa outros arquivos direta ou indiretamente ou ao examinar o arquivo de nível superior, o pré-processador pode ser invocado diretamente. Executar o pré-processador C/C++ diretamente pode revelar erros mascarados ou confundidos por MIDL. Por exemplo, as duas linhas de comando do pré-processador a seguir podem ser usadas para a linha MIDL entre aspas anteriormente:

**cl /E /nologo -Id: \\ nt \\ public \\ sdk \\ inc -DNTENV=1 stub.idl > stub.pp**

**cl /E /P -Id: \\ nt \\ public \\ sdk \\ inc -DNTENV=1 stub.idl**

No primeiro desses dois exemplos, **/E** [**/nologo**](-nologo.md) são as opções que MIDL adiciona ao invocar o pré-processador. A saída do pré-processador é enviada para stdout (a tela) e, portanto, requer redirecionamento para um arquivo para exame. No segundo desses exemplos, **/P** direciona o pré-processador para redirecionar a saída para um arquivo .i; nesse caso, um arquivo Stub.i seria criado no diretório \* atual.

A [**opção /cpp \_ opt**](-cpp-opt.md) também pode ser usada para obter um arquivo pré-processado, mas é difícil e inferior aos métodos mencionados anteriormente. O exemplo a seguir também produz um arquivo Stub.i, assim como o exemplo anterior. As aspas no exemplo a seguir são essenciais:

**Midl -Oicf -win32 -cpp \_ opt "/E /P -Id: \\ nt \\ public \\ sdk \\ inc -DNTENV=1" stub.idl**

 

 




