---
title: C-definições de compilador para proxy/stubs
description: O arquivo de cabeçalho RpcProxy. h inclui as seguintes definições de macro, e cada uma delas pode ser conveniente ao criar um aplicativo COM distribuído. Essas macros são invocadas com a opção de pré-processador/D (ou-D) no momento da compilação C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL do compilador MIDL, C-Compiler, definições para proxy/stubs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b272b8b540420930366864c45e993172f5c00e67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882060"
---
# <a name="c-compiler-definitions-for-proxystubs"></a>C-definições de compilador para proxy/stubs

O arquivo de cabeçalho RpcProxy. h inclui as seguintes definições de macro, e cada uma delas pode ser conveniente ao criar um aplicativo COM distribuído. Essas macros são invocadas com a opção de pré-processador [**/d**](-d.md) (ou-D) no momento da compilação C.



| MACRO                                                                                                                                                                                           | Description                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REGISTRAR \_ dll de proxy \_                                                                                                                                                                            | Gera as funções **DllMain**, **DllRegisterServer** e **DLLUNREGISTERSERVER** para registrar automaticamente uma DLL de proxy.                                                                                       |
| CLSID de PROXY \_ = &lt; CLSID&gt;                                                                                                                                                                      | Especifica um identificador de classe para o servidor. Se essa macro não estiver definida, o CLSID padrão será o primeiro identificador de interface que o compilador MIDL encontrará na especificação IDL do servidor proxy/stub. |
| CLSID de PROXY \_ \_ é = {0x *8hexdigits*,*0x 4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*,}} | Especifica o valor do identificador de classe do servidor no formato hexadecimal binário.                                                                                                                                           |



 

Ao definir a macro da **\_ \_ dll do proxy de registro** ao compilar dlldata. c, sua DLL de marshaling de proxy/stub incluirá automaticamente as definições padrão para as funções **DllMain**, **DllRegisterServer** e **DllUnregisterServer** . Você pode usar essas funções para registrar automaticamente sua DLL de proxy no registro do sistema.

Esse código de registro padrão usa o GUID da primeira interface encontrado como o CLSID para registrar todo o servidor DLL de proxy/stub. O COM mais tarde usa esse CLSID para localizar e carregar o servidor proxy/stub compilado para o marshaling de qualquer uma das interfaces que o servidor está registrado para manipular. Quando um aplicativo faz uma chamada de método de interface que cruza os limites do thread, do processo ou do computador, COM usa a entrada do registro do identificador de interface para localizar a entrada do Registro CLSID para o servidor de marshaling do proxy/stub. Em seguida, ele usa esse CLSID para carregar o servidor (se ele ainda não estiver carregado) para que a chamada de interface possa ser empacotada.

Use a **macro \_ CLSID de proxy** CLSID = &lt; &gt; quando desejar especificar explicitamente o CLSID do servidor de proxy/stub em vez de confiar no CLSID padrão. Por exemplo, se você estiver criando uma DLL de marshaling padrão como seu próprio servidor COM em processo, ou se precisar definir seu próprio **DllMain** para manipular a \_ anexação do processo de dll \_ .

Use **CLSID de proxy \_ \_ é**= macro em vez de **\_ CLSID de proxy** para definir o valor do CLSID no formato hexadecimal binário que a macro **define \_ GUID** usa.

Observe também que, quando a função **DllRegisterServer** padrão é executada, ela registra o servidor com ThreadingModel = both.

O exemplo de makefile a seguir usa a **\_ \_ dll de registro de proxy** e o **proxy \_ CLSID**= macros:

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

Para obter mais informações sobre a opção [**/d**](-d.md) pré-processador, consulte a documentação do compilador do C.

 

 




