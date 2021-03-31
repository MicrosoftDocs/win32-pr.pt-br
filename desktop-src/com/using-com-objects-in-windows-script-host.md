---
title: Usando objetos COM no Windows Script Host
description: O Microsoft Windows Script Host é um utilitário de script que você pode usar para executar scripts no sistema operacional base.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663851"
---
# <a name="using-com-objects-in-windows-script-host"></a>Usando objetos COM no Windows Script Host

O Microsoft Windows Script Host é um utilitário de script que você pode usar para executar scripts no sistema operacional base. Você pode usar o Windows Script Host para automatizar tarefas comuns e criar macros e scripts de logon avançados. O Windows Script Host vem com mecanismos de script VBScript e JScript ActiveX. Outras empresas de software fornecem mecanismos de script do ActiveX para linguagens como PerlScript, PScript, Python e outros.

Para usar um objeto COM em um script executado pelo Windows Script Host, você deve primeiro criar uma instância do objeto. Depois que um objeto COM tiver sido criado, você poderá usá-lo em scripts.

O Windows Script Host consiste em dois aplicativos. Um executa scripts da área de trabalho do Windows ( `WScript.exe` ); o outro executa scripts do prompt de comando ( `CScript.exe` ).

Para executar um script da área de trabalho, basta clicar duas vezes em um arquivo de script. Os arquivos de script são arquivos de texto. Por convenção, os arquivos VBScript têm a extensão `.vbs` e os arquivos JScript `.js` .

Para executar um script do prompt de comando, execute o `Cscript.exe` aplicativo com uma linha de comando, como a seguinte:

```console
cscript "c:\\sample scripts\\chart.vbs"
```

em que `c:\\sample scripts\\chart.vbs` é o caminho para o arquivo que contém o script.

Você pode imprimir uma lista dos parâmetros com suporte pelo Cscript.exe digitando a seguinte linha de comando:

```console
call cscript //?
```

Para usar um objeto COM em um script executado pelo Windows Script Host, você deve primeiro criar uma instância do objeto. No VBScript, você pode fazer isso chamando o `CreateObject()` método. No JScript, um pode usar o `ActiveXObject` objeto ou o `WScript.CreateObject()` método. O exemplo a seguir ilustra a chamada `CreateObject()` usando o VBScript:


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



O exemplo a seguir ilustra a criação de um `ActiveXObject` objeto usando o JScript:


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
Como alternativa, usando o `WScript.CreateObject()` método dentro do JScript:

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


Depois de criar uma instância do objeto COM, você pode escrever um script que use o objeto, por exemplo:


```VB
objXL.Visible = true;
 
```



Além do método CreateObject e do objeto ActiveXobject, o VBScript e o JScript fornecem o método GetObject, que retorna uma instância de objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando scripts com objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




