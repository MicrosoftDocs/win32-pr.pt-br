---
title: O arquivo IDL
description: O arquivo IDL consiste em uma ou mais definições de interface, cada uma com um cabeçalho e um corpo.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454109"
---
# <a name="the-idl-file"></a><span data-ttu-id="72e60-103">O arquivo IDL</span><span class="sxs-lookup"><span data-stu-id="72e60-103">The IDL File</span></span>

<span data-ttu-id="72e60-104">O arquivo IDL consiste em uma ou mais definições de interface, cada uma com um cabeçalho e um corpo.</span><span class="sxs-lookup"><span data-stu-id="72e60-104">The IDL file consists of one or more interface definitions, each of which has a header and a body.</span></span> <span data-ttu-id="72e60-105">O cabeçalho contém informações que se aplicam à interface inteira, como o UUID.</span><span class="sxs-lookup"><span data-stu-id="72e60-105">The header contains information that applies to the entire interface, such as the UUID.</span></span> <span data-ttu-id="72e60-106">Essas informações são colocadas entre colchetes e são seguidas pela **interface** de palavra-chave e o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="72e60-106">This information is enclosed in square brackets and is followed by the keyword **interface** and the interface name.</span></span> <span data-ttu-id="72e60-107">O corpo contém definições de tipo de dados de estilo C e protótipos de função, aumentados com atributos que descrevem como os dados são transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="72e60-107">The body contains C-style data type definitions and function prototypes, augmented with attributes that describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="72e60-108">Neste exemplo, o cabeçalho da interface contém apenas o UUID e o número de versão.</span><span class="sxs-lookup"><span data-stu-id="72e60-108">In this example, the interface header contains only the UUID and the version number.</span></span> <span data-ttu-id="72e60-109">O número de versão garante que, quando houver várias versões de uma interface RPC, somente as versões compatíveis do cliente e do servidor serão conectadas.</span><span class="sxs-lookup"><span data-stu-id="72e60-109">The version number ensures that when there are multiple versions of an RPC interface, only compatible versions of the client and server will be connected.</span></span>

<span data-ttu-id="72e60-110">O corpo da interface contém o protótipo de função para **HelloProc**.</span><span class="sxs-lookup"><span data-stu-id="72e60-110">The interface body contains the function prototype for **HelloProc**.</span></span> <span data-ttu-id="72e60-111">Nesse protótipo, o parâmetro de função pszString tem os atributos **\[** [**in**](/windows/desktop/Midl/in) **\]** e **\[** [**String**](/windows/desktop/Midl/string) **\]** .</span><span class="sxs-lookup"><span data-stu-id="72e60-111">In this prototype, the function parameter pszString has the attributes **\[**[**in**](/windows/desktop/Midl/in)**\]** and **\[**[**string**](/windows/desktop/Midl/string)**\]**.</span></span> <span data-ttu-id="72e60-112">O atributo **\[ in \]** informa à biblioteca de tempo de execução que o parâmetro é passado somente do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="72e60-112">The **\[in\]** attribute tells the run-time library that the parameter is passed only from the client to the server.</span></span> <span data-ttu-id="72e60-113">O atributo **\[ String \]** especifica que o stub deve tratar o parâmetro como uma cadeia de caracteres de estilo C.</span><span class="sxs-lookup"><span data-stu-id="72e60-113">The **\[string\]** attribute specifies that the stub should treat the parameter as a C-style character string.</span></span>

<span data-ttu-id="72e60-114">O aplicativo cliente deve ser capaz de desligar o aplicativo de servidor, portanto, a interface contém um protótipo para outra função remota,**Shutdown** , que será implementada posteriormente neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="72e60-114">The client application should be able to shut down the server application, so the interface contains a prototype for another remote function,**Shutdown** , that will be implemented later in this tutorial.</span></span>

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 