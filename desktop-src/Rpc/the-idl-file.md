---
title: O arquivo IDL
description: O arquivo IDL consiste em uma ou mais definições de interface, cada uma das quais tem um header e um corpo.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f46a92fe5967dca1faeca1d658cf398fb0baf6ebd9160c3a736747de324e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924410"
---
# <a name="the-idl-file"></a>O arquivo IDL

O arquivo IDL consiste em uma ou mais definições de interface, cada uma das quais tem um header e um corpo. O header contém informações que se aplica a toda a interface, como o UUID. Essas informações são entre colchetes e são seguidas pela interface de **palavra-chave** e pelo nome da interface. O corpo contém definições de tipo de dados no estilo C e protótipos de função, aumentados com atributos que descrevem como os dados são transmitidos pela rede.

Neste exemplo, o header da interface contém apenas o UUID e o número de versão. O número de versão garante que, quando houver várias versões de uma interface RPC, somente as versões compatíveis do cliente e do servidor serão conectadas.

O corpo da interface contém o protótipo de função **para HelloProc.** Nesse protótipo, o parâmetro de função pszString tem os atributos **\[** [**em**](/windows/desktop/Midl/in) **\]** e cadeia de **\[** [**caracteres**](/windows/desktop/Midl/string) **\]** . O **\[ atributo in \]** informa à biblioteca em tempo de executar que o parâmetro é passado somente do cliente para o servidor. O **\[ atributo de \]** cadeia de caracteres especifica que o stub deve tratar o parâmetro como uma cadeia de caracteres de estilo C.

O aplicativo cliente deve ser capaz de desligar o aplicativo de servidor, portanto, a interface contém um protótipo para outra função remota,**Shutdown** , que será implementado posteriormente neste tutorial.

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

 

 