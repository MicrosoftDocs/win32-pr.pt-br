---
title: Compilando marcação da faixa de medida
description: para o Windows estrutura da faixa de faixas consumir o arquivo de marcação da faixa de faixas, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows Faixa de faixas, compilando marcação
- Faixa de faixas, compilando marcação
- Windows Faixa de medida, fluxo de trabalho do compilador
- Faixa de medida, fluxo de trabalho do compilador
- Windows Faixa de comandos, compilador de comando de interface do usuário (UICC.exe)
- Faixa de comandos, compilador de comando de interface do usuário (UICC.exe)
- Compilador de comando de interface do usuário (UICC.exe)
- UICC.exe (compilador de comando de interface do usuário)
- compilando marcação de faixa de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cefd64103ceb501e8f4d23e937a242e910b0cad5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884908"
---
# <a name="compiling-ribbon-markup"></a>Compilando marcação da faixa de medida

para o Windows estrutura da faixa de faixas consumir o arquivo de [marcação da faixa de faixas](windowsribbon-schema.md) , o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário. um compilador de marcação dedicado, o UICC (compilador de comando de interface do usuário), está incluído com o SDK (Software Development Kit) do Windows (7,0 ou posterior) para essa finalidade. Além de compilar a versão binária da marcação, o UICC gera um arquivo de cabeçalho de definição de ID (. h) que expõe todos os elementos de marcação para o aplicativo host da faixa de versões e um arquivo de recurso (. rc) que é usado para vincular recursos de imagem e de cadeia de caracteres ao aplicativo host no momento da compilação.

-   [Fluxo de trabalho do compilador](#compiler-workflow)
-   [Sintaxe de linha de comando](#command-line-syntax)
    -   [Argumentos e opções](#arguments-and-options)
    -   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="compiler-workflow"></a>Fluxo de trabalho do compilador

O fluxo de trabalho do compilador de marcação da faixa de opções é ilustrado no diagrama a seguir.

![diagrama mostrando o fluxo de trabalho do compilador de marcação da faixa de Ribbon.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>Sintaxe da linha de comando

A sintaxe de linha de comando para o compilador de marcação da faixa de opções é mostrada no exemplo a seguir.


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>Argumentos e opções

Os argumentos e as opções para essa ferramenta são descritos na tabela a seguir.

> [!Note]  
> As opções de linha de comando listadas devem ser especificadas na ordem especificada.

 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/header: &lt; HeaderFile&gt;</td>
<td>Gere um arquivo de cabeçalho chamado &lt; HeaderFile &gt; que contém os símbolos de recurso de ID de comando de marcação. Se omitido, um arquivo de cabeçalho não será gerado.</td>
</tr>
<tr class="even">
<td>/res<resourceFile></td>
<td>Gerar um arquivo de recurso chamado <resourceFile> que vincula todos os recursos de imagem e de cadeia de caracteres, o arquivo de marcação binária e o arquivo de cabeçalho ao aplicativo host no momento da compilação. Se omitido, um arquivo de recurso não será gerado.</td>
</tr>
<tr class="odd">
<td>/Name<ribbonName></td>
<td>O nome do recurso para o arquivo de marcação binária que é registrado no <resourceFile> . O padrão é APPLICATION_RIBBON.</td>
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
<td>Mensagens de erro e de aviso apenas.<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>Padrão. <br/> Mensagens de erro, aviso e informativas.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>Exemplo

O exemplo a seguir demonstra como usar o compilador de marcação da faixa de opções para gerar um conjunto típico de arquivos de recurso para um aplicativo da faixa de opções.

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declarando comandos e controles com marcação de faixa de medida](windowsribbon-schema.md)
</dt> <dt>

[Criando um aplicativo de faixa de faixas](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





