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
# <a name="using-com-objects-in-windows-script-host"></a><span data-ttu-id="f8830-103">Usando objetos COM no Windows Script Host</span><span class="sxs-lookup"><span data-stu-id="f8830-103">Using COM Objects in Windows Script Host</span></span>

<span data-ttu-id="f8830-104">O Microsoft Windows Script Host é um utilitário de script que você pode usar para executar scripts no sistema operacional base.</span><span class="sxs-lookup"><span data-stu-id="f8830-104">Microsoft Windows Script Host is a scripting utility you can use to run scripts within the base operating system.</span></span> <span data-ttu-id="f8830-105">Você pode usar o Windows Script Host para automatizar tarefas comuns e criar macros e scripts de logon avançados.</span><span class="sxs-lookup"><span data-stu-id="f8830-105">You can use Windows Script Host to automate common tasks and to create powerful macros and logon scripts.</span></span> <span data-ttu-id="f8830-106">O Windows Script Host vem com mecanismos de script VBScript e JScript ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f8830-106">Windows Script Host comes with VBScript and JScript ActiveX scripting engines.</span></span> <span data-ttu-id="f8830-107">Outras empresas de software fornecem mecanismos de script do ActiveX para linguagens como PerlScript, PScript, Python e outros.</span><span class="sxs-lookup"><span data-stu-id="f8830-107">Other software companies provide ActiveX scripting engines for languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="f8830-108">Para usar um objeto COM em um script executado pelo Windows Script Host, você deve primeiro criar uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="f8830-108">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="f8830-109">Depois que um objeto COM tiver sido criado, você poderá usá-lo em scripts.</span><span class="sxs-lookup"><span data-stu-id="f8830-109">After a COM object has been created, you can then use it in scripts.</span></span>

<span data-ttu-id="f8830-110">O Windows Script Host consiste em dois aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f8830-110">Windows Script Host consists of two applications.</span></span> <span data-ttu-id="f8830-111">Um executa scripts da área de trabalho do Windows ( `WScript.exe` ); o outro executa scripts do prompt de comando ( `CScript.exe` ).</span><span class="sxs-lookup"><span data-stu-id="f8830-111">One runs scripts from the Windows desktop (`WScript.exe`); the other runs scripts from the command prompt (`CScript.exe`).</span></span>

<span data-ttu-id="f8830-112">Para executar um script da área de trabalho, basta clicar duas vezes em um arquivo de script.</span><span class="sxs-lookup"><span data-stu-id="f8830-112">To run a script from the desktop, simply double-click a script file.</span></span> <span data-ttu-id="f8830-113">Os arquivos de script são arquivos de texto.</span><span class="sxs-lookup"><span data-stu-id="f8830-113">Script files are text files.</span></span> <span data-ttu-id="f8830-114">Por convenção, os arquivos VBScript têm a extensão `.vbs` e os arquivos JScript `.js` .</span><span class="sxs-lookup"><span data-stu-id="f8830-114">By convention, VBScript files have the extension `.vbs` and JScript files `.js`.</span></span>

<span data-ttu-id="f8830-115">Para executar um script do prompt de comando, execute o `Cscript.exe` aplicativo com uma linha de comando, como a seguinte:</span><span class="sxs-lookup"><span data-stu-id="f8830-115">To run a script from the command prompt, run the `Cscript.exe` application with a command line such as the following:</span></span>

```console
cscript "c:\\sample scripts\\chart.vbs"
```

<span data-ttu-id="f8830-116">em que `c:\\sample scripts\\chart.vbs` é o caminho para o arquivo que contém o script.</span><span class="sxs-lookup"><span data-stu-id="f8830-116">where `c:\\sample scripts\\chart.vbs` is the path to the file containing the script.</span></span>

<span data-ttu-id="f8830-117">Você pode imprimir uma lista dos parâmetros com suporte pelo Cscript.exe digitando a seguinte linha de comando:</span><span class="sxs-lookup"><span data-stu-id="f8830-117">You can print out a list of the parameters supported by Cscript.exe by entering the following command line:</span></span>

```console
call cscript //?
```

<span data-ttu-id="f8830-118">Para usar um objeto COM em um script executado pelo Windows Script Host, você deve primeiro criar uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="f8830-118">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="f8830-119">No VBScript, você pode fazer isso chamando o `CreateObject()` método.</span><span class="sxs-lookup"><span data-stu-id="f8830-119">In VBScript you can do this by calling the `CreateObject()` method.</span></span> <span data-ttu-id="f8830-120">No JScript, um pode usar o `ActiveXObject` objeto ou o `WScript.CreateObject()` método.</span><span class="sxs-lookup"><span data-stu-id="f8830-120">In JScript one can use either the `ActiveXObject` object or the `WScript.CreateObject()` method.</span></span> <span data-ttu-id="f8830-121">O exemplo a seguir ilustra a chamada `CreateObject()` usando o VBScript:</span><span class="sxs-lookup"><span data-stu-id="f8830-121">The following example illustrates calling `CreateObject()` using VBScript:</span></span>


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



<span data-ttu-id="f8830-122">O exemplo a seguir ilustra a criação de um `ActiveXObject` objeto usando o JScript:</span><span class="sxs-lookup"><span data-stu-id="f8830-122">The following example illustrates creating an `ActiveXObject` object using JScript:</span></span>


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
<span data-ttu-id="f8830-123">Como alternativa, usando o `WScript.CreateObject()` método dentro do JScript:</span><span class="sxs-lookup"><span data-stu-id="f8830-123">Alternatively using `WScript.CreateObject()` method inside JScript:</span></span>

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


<span data-ttu-id="f8830-124">Depois de criar uma instância do objeto COM, você pode escrever um script que use o objeto, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f8830-124">After you have created an instance of the COM object, you can write script that uses the object, for example:</span></span>


```VB
objXL.Visible = true;
 
```



<span data-ttu-id="f8830-125">Além do método CreateObject e do objeto ActiveXobject, o VBScript e o JScript fornecem o método GetObject, que retorna uma instância de objeto.</span><span class="sxs-lookup"><span data-stu-id="f8830-125">In addition to the CreateObject method and ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8830-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8830-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8830-127">Criando scripts com objetos COM</span><span class="sxs-lookup"><span data-stu-id="f8830-127">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




