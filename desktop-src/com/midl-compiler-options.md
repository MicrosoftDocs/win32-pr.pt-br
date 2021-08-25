---
title: Opções do compilador MIDL
description: Opções do compilador MIDL
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649cd96ffc0afa171ad218a737910ce15facbe0e9b5ef302dedb6615228bcf3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859326"
---
# <a name="midl-compiler-options"></a>Opções do compilador MIDL

Você pode usar as seguintes opções de linha de comando para substituir alguns dos comportamentos padrão do compilador MIDL e escolher otimizações apropriadas para seu aplicativo. Para obter uma lista completa das opções de linha de comando de MIDL, consulte a [referência de Command-Line MIDL](/windows/desktop/Midl/midl-command-line-reference).



| Opção de linha de comando                                       | Descrição                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | Use para fornecer um nome de arquivo ACF explícito. Essa opção também permite o uso de nomes de interface diferentes nos arquivos IDL e ACF.<br/>                                                                                                       |
| [**/dlldata nomedearquivo**](/windows/desktop/Midl/-dlldata)<br/>                  | Especifica um FileName para o arquivo de dados DLL gerado para uma DLL de proxy. O nome de arquivo padrão é dlldata. c.<br/>                                                                                                                              |
| [**/env**](/windows/desktop/Midl/-env)<br/>                          | Direciona MIDL para gerar stubs ou uma biblioteca de tipos para um ambiente de destino.<br/>                                                                                                                                                            |
| [**/header**](/windows/desktop/Midl/-header), [ **/h**](/windows/desktop/Midl/-h)<br/> | Especifica o nome do arquivo de cabeçalho da interface. O nome padrão é o do arquivo IDL com uma extensão. h.<br/>                                                                                                                       |
| [**/IID nomedearquivo**](/windows/desktop/Midl/-iid)<br/>                          | Especifica um nome de arquivo de identificador de interface que substitui o nome de arquivo do identificador de interface padrão para uma interface COM.<br/>                                                                                                              |
| [**/LCID**](/windows/desktop/Midl/-lcid)<br/>                        | Fornece suporte completo a DBCS para que você possa usar caracteres internacionais em seus arquivos de entrada, nomes de arquivo e caminhos de diretório.<br/>                                                                                                          |
| [**\_opção de formato de/// \_**](/windows/desktop/Midl/-no-format-opt)<br/>    | Por padrão, para reduzir o tamanho do código, MIDL elimina descritores duplicados. Essa opção desativa esse comportamento de otimização.<br/>                                                                                                               |
| [**/Oi**](/windows/desktop/Midl/-oi), **/OIC**, **/OIF**<br/>        | Direciona o MIDL para usar um método de marshaling totalmente interpretado. Os comutadores/OIC e/Oicf fornecem aprimoramentos de desempenho adicionais.<br/>                                                                                                   |
| [**/out**](/windows/desktop/Midl/-out)<br/>                          | Especifica o diretório no qual o compilador MIDL grava os arquivos de saída. O diretório de saída pode ser especificado com uma letra de unidade, um nome de caminho absoluto ou ambos. O padrão é que MIDL grava os arquivos no diretório atual.<br/> |
| [**/proxy nomedearquivo**](/windows/desktop/Midl/-proxy)<br/>                      | Especifica o nome do arquivo de proxy da interface para uma interface COM. O nome padrão é o do arquivo IDL mais " \_ p. c".<br/>                                                                                                            |
| [**/tlb**](/windows/desktop/Midl/-tlb)<br/>                          | Especifica o nome do arquivo de biblioteca de tipos. O nome padrão é o do arquivo IDL, com uma extensão. tlb.<br/>                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Compilação de MIDL](midl-compilation.md)
</dt> </dl>

 

