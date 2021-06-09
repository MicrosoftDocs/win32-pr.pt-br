---
title: Criando e registrando uma DLL de proxy
description: Se você escolher marshaling de proxy/stub para seu aplicativo, os arquivos. c e. h que o MIDL gerado devem ser compilados e vinculados para criar uma DLL de proxy, e essa DLL deve ser inserida no registro do sistema para que os clientes possam localizar suas interfaces.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d4cafbe2be56d9e9a02a451e3daf905496c424
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826801"
---
# <a name="building-and-registering-a-proxy-dll"></a>Criando e registrando uma DLL de proxy

Se você escolher marshaling de proxy/stub para seu aplicativo, os arquivos. c e. h que o MIDL gerado devem ser compilados e vinculados para criar uma DLL de proxy, e essa DLL deve ser inserida no registro do sistema para que os clientes possam localizar suas interfaces. O arquivo gerado pelo MIDL dlldata. c contém as rotinas necessárias e outras informações para compilar e registrar uma DLL de proxy/stub.

A primeira etapa na criação da DLL é gravar um arquivo de definição de módulo para o vinculador, conforme mostrado no exemplo a seguir:

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

Como alternativa, você pode especificar essas funções exportadas na linha de comando do LINK do makefile.

As funções exportadas são declaradas em RpcProxy. h, que dlldata. c inclui, e as implementações padrão fazem parte da biblioteca de tempo de execução RPC. COM usa essas funções para criar uma fábrica de classes, descarregar DLLs (depois de certificar-se de que não existam objetos ou bloqueios), recuperar informações sobre a DLL de proxy e registrar em Autoregistro e cancelar o registro da DLL de proxy. Para aproveitar essas funções predefinidas, você precisa invocar a opção Cpreprocessor/D (ou-D) ao compilar os arquivos dlldata. c e example \_ p. c, conforme mostrado no seguinte makefile:

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

Se você não especificar essas definições de pré-processador em tempo de compilação, essas funções não serão definidas automaticamente. (Ou seja, as macros em RpcProxy. c expandem para Nothing.) Você precisaria defini-las explicitamente em outro arquivo de origem, cujo módulo também seria incluído na vinculação e compilação final na linha de comando do compilador C.

Quando o \_ registro \_ dll de proxy é definido, o RpcProxy. h fornece um controle de compilação condicional adicional com proxy \_ CLSID =*GUID*, proxy \_ CLSID \_ é =*valor explícito de GUID* e prefixo de entrada \_ =*cadeia de caracteres de prefixo*. Essas definições de macro são descritas mais detalhadamente em [definições de compilador C para proxy/stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) no guia do programador de MIDL.

## <a name="manually-registering-the-proxy-dll"></a>Registrando manualmente a DLL de proxy

Se, por alguma razão, você não puder usar as rotinas de registro de stub de proxy padrão, poderá registrar manualmente a DLL adicionando as seguintes entradas ao registro do sistema, usando Regedt32.exe.

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[C-definições de compilador para proxy/stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 
