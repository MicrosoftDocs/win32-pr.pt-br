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
# <a name="the-idl-file"></a>O arquivo IDL

O arquivo IDL consiste em uma ou mais definições de interface, cada uma com um cabeçalho e um corpo. O cabeçalho contém informações que se aplicam à interface inteira, como o UUID. Essas informações são colocadas entre colchetes e são seguidas pela **interface** de palavra-chave e o nome da interface. O corpo contém definições de tipo de dados de estilo C e protótipos de função, aumentados com atributos que descrevem como os dados são transmitidos pela rede.

Neste exemplo, o cabeçalho da interface contém apenas o UUID e o número de versão. O número de versão garante que, quando houver várias versões de uma interface RPC, somente as versões compatíveis do cliente e do servidor serão conectadas.

O corpo da interface contém o protótipo de função para **HelloProc**. Nesse protótipo, o parâmetro de função pszString tem os atributos **\[** [**in**](/windows/desktop/Midl/in) **\]** e **\[** [**String**](/windows/desktop/Midl/string) **\]** . O atributo **\[ in \]** informa à biblioteca de tempo de execução que o parâmetro é passado somente do cliente para o servidor. O atributo **\[ String \]** especifica que o stub deve tratar o parâmetro como uma cadeia de caracteres de estilo C.

O aplicativo cliente deve ser capaz de desligar o aplicativo de servidor, portanto, a interface contém um protótipo para outra função remota,**Shutdown** , que será implementada posteriormente neste tutorial.

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

 

 