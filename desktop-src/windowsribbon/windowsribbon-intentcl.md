---
title: Compilando marcação de faixa de opções
description: Para que a estrutura Windows faixa de opções consuma o arquivo de marcação faixa de opções, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows Faixa de opções, marcação de compilação
- Faixa de opções, marcação de compilação
- Windows Faixa de opções, fluxo de trabalho do compilador
- Faixa de opções, fluxo de trabalho do compilador
- Windows Ribbon,UI Command Compiler (UICC.exe)
- Ribbon,Compilador de Comando da Interface do Usuário (UICC.exe)
- Compilador de comando da interface do usuário (UICC.exe)
- UICC.exe (compilador de comando da interface do usuário)
- compilando uma marcação Windows faixa de opções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85534a05b3bde59cc2ec0eec482d8c3b47e898d39ad988c595fbac33eb5e9f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932556"
---
# <a name="compiling-ribbon-markup"></a>Compilando marcação de faixa de opções

Para que a estrutura Windows Faixa [](windowsribbon-schema.md) de Opções consuma o arquivo de marcação faixa de opções, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário. Um compilador de marcação dedicado, o UICC (Compilador de Comando da Interface do Usuário), está incluído com o SDK (Software Development Kit) do Windows (7.0 ou posterior) para essa finalidade. Além de compilar a versão binária da marcação, o UICC gera um arquivo de título de definição de ID (.h) que expõe todos os elementos de marcação para o aplicativo host da Faixa de Opções e um arquivo de recurso (.rc) usado para vincular recursos de imagem e cadeia de caracteres ao aplicativo host no momento da compilação.

-   [Fluxo de trabalho do compilador](#compiler-workflow)
-   [Sintaxe de linha de comando](#command-line-syntax)
    -   [Argumentos e opções](#arguments-and-options)
    -   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="compiler-workflow"></a>Fluxo de trabalho do compilador

O fluxo de trabalho do compilador de marcação ribbon é ilustrado no diagrama a seguir.

![diagrama mostrando o fluxo de trabalho do compilador de marcação da faixa de opções.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>Sintaxe da linha de comando

A sintaxe de linha de comando para o compilador de marcação da Faixa de Opções é mostrada no exemplo a seguir.


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>Argumentos e opções

Os argumentos e as opções para essa ferramenta são descritos na tabela a seguir.

> [!Note]  
> As opções de linha de comando listadas devem ser especificadas na ordem especificada.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/header:<headerFile></td>
<td>Gere um arquivo de header chamado que contém os símbolos de recurso <headerFile> da ID de comando de marcação. Se omitido, um arquivo de header não será gerado.</td>
</tr>
<tr class="even">
<td>/res:<resourceFile></td>
<td>Gere um arquivo de recurso chamado que vincula todos os recursos de imagem e cadeia de caracteres, o arquivo de marcação binária e o arquivo de header para o aplicativo host no <resourceFile> momento do build. Se omitido, um arquivo de recurso não será gerado.</td>
</tr>
<tr class="odd">
<td>/name:<ribbonName></td>
<td>O nome do recurso para o arquivo de marcação binário registrado no <resourceFile> . O padrão é APPLICATION_RIBBON.</td>
</tr>
<tr class="even">
<td>/W{0\1\2}</td>
<td>Filtre as mensagens de evento com base na severidade. 
<table>
<tbody>
<tr class="odd">
<td>0<br/></td>
<td>Mensagens de erro somente.<br/></td>
</tr>
<tr class="even">
<td>1<br/></td>
<td>Somente mensagens de erro e aviso.<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>Padrão. <br/> Mensagens de erro, aviso e informações.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>Exemplo

O exemplo a seguir demonstra como usar o compilador de marcação Faixa de Opções para gerar um conjunto típico de arquivos de recurso para um aplicativo de Faixa de Opções.

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declarando comandos e controles com marcação de faixa de opções](windowsribbon-schema.md)
</dt> <dt>

[Criando um aplicativo de faixa de opções](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





