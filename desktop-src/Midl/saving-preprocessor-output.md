---
title: Salvando a saída do pré-processador
description: A exibição da saída do pré-processador pode ser um método eficaz de solução de problemas, como quando ocorre uma sintaxe IDL, C ou C-pré-processador inválida, ou quando valores falsos-D na linha de comando MIDL resultam em erros de misteriosos de relatório de MIDL.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL do compilador MIDL, salvando a saída do pré-processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364115"
---
# <a name="saving-preprocessor-output"></a>Salvando a saída do pré-processador

A exibição da saída do pré-processador pode ser um método eficaz de solução de problemas, como quando ocorre uma sintaxe IDL, C ou C-pré-processador inválida, ou quando valores falsos-D na linha de comando MIDL resultam em erros de misteriosos de relatório de MIDL. Os desenvolvedores também podem querer examinar a saída do pré-processador para determinar quais arquivos e definições estavam presentes no fluxo de entrada do compilador, como quando um caso difícil do conflito de redefinição de tipo deve ser resolvido. Ou menos comumente, alguns desenvolvedores podem querer forçar comutadores privados no pré-processador com [**/cpp \_ opt**](-cpp-opt.md)ou talvez queiram ver como funcionam as opções.

A maneira mais fácil e menos invasiva de obter arquivos pré-processados de uma execução de compilação MIDL é usar a opção [**-savePP**](-savepp.md) . A opção **-savePP** simplesmente impede o MIDL de excluir os arquivos temporários que o pré-processador passa de volta para o MIDL. Considere o seguinte:

**MIDL-savePP-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1-Oicf-env Win32 stub. idl**

Essa diretiva compila stub. idl, mas preserva todos os arquivos de pré-processador.

> [!Note]  
> O MIDL gera execuções de pré-processador separadas para o arquivo IDL e ACF (se presente), bem como para todos os arquivos importados.

 

Para uma compilação de DCOM, vários arquivos de pré-processador são geralmente produzidos, mesmo que sejam processados pelo MIDL como um fluxo de entrada contíguo virtual. Em um ambiente de programação típico do Windows, os arquivos temporários podem ser encontrados no diretório Temp como nomes de arquivos, como MID \* . tmp. Se estiver preservando a saída do pré-processador, é uma prática recomendada observar os arquivos recentes no diretório Temp para identificar quais arquivos estão associados ao pré-processador executado.

Em casos simples, como quando o arquivo IDL compilado não importa outros arquivos direta ou indiretamente, ou ao examinar o arquivo de nível superior, o pré-processador pode ser invocado diretamente. Executar o pré-processador do C/C++ diretamente pode revelar erros mascarados ou confusos pelo MIDL. Por exemplo, as duas linhas de comando de pré-processador a seguir podem ser usadas para a linha MIDL citada anteriormente:

**CL/E/nologo-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1 stub. idl > stub. PP**

**CL/E/P-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1 stub. idl**

No primeiro desses dois exemplos, **/e** [**/nologo**](-nologo.md) são as opções que o MIDL adiciona ao invocar o pré-processador. A saída do pré-processador é enviada para stdout (a tela) e, portanto, requer o redirecionamento para um arquivo para exame. No segundo desses exemplos, **/p** direciona o pré-processador para redirecionar a saída para um \* arquivo. i; nesse caso, um arquivo stub. i seria criado no diretório atual.

A opção [**/cpp \_ opt**](-cpp-opt.md) também pode ser usada para obter um arquivo pré-processado, mas é difícil e inferior aos métodos mencionados anteriormente. O exemplo a seguir também produz um arquivo stub. i, como fazia o exemplo anterior. As aspas no exemplo a seguir são essenciais:

**MIDL-Oicf-Win32-cpp \_ opt "/E/p-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1" stub. idl**

 

 




