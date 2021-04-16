---
title: Self-Registration
description: O auto-registro é o meio padrão pelo qual um módulo de servidor pode empacotar suas próprias operações de registro, registro e cancelamento de registro, no próprio módulo.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454374"
---
# <a name="self-registration"></a>Self-Registration

À medida que o software do componente continua crescendo como um mercado, haverá mais e mais instâncias em que um usuário Obtém um novo componente de software como um único módulo DLL ou EXE, como ao baixar um novo componente de um serviço online ou receber um de um amigo em um disquete. Nesses casos, não é prático exigir que o usuário passe por um procedimento de instalação demorado ou programa de instalação. Além dos problemas de licenciamento, que são manipulados por meio do [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), um procedimento de instalação normalmente cria as entradas de Registro necessárias para que um componente seja executado corretamente no contexto com e OLE.

O auto-registro é o meio padrão pelo qual um módulo de servidor pode empacotar suas próprias operações de registro, registro e cancelamento de registro, no próprio módulo. Quando usado com licenciamento manipulado por meio de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), um servidor pode se tornar um módulo totalmente independente, sem a necessidade de programas de instalação externos ou arquivos. reg.

Qualquer módulo de registro automático, DLL ou EXE, deve primeiro incluir uma cadeia de caracteres "OleSelfRegister" na seção [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) de seu recurso de informações de versão, como mostrado aqui.

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

A existência desses dados permite que qualquer parte interessada, como um aplicativo que queira integrar esse novo componente, determine se o servidor dá suporte a Autoregistro sem precisar carregar primeiro a DLL ou o EXE.

Se o servidor for empacotado em um módulo de DLL, a DLL deverá exportar as funções [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Qualquer aplicativo que queira instruir o servidor a se registrar (ou seja, todos os seus CLSIDs e IDs de biblioteca de tipos) pode obter um ponteiro para **DllRegisterServer** por meio da função [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) . Dentro de **DllRegisterServer**, a dll cria todas as suas entradas de Registro necessárias, armazenando o caminho correto para a dll para todas as entradas [InprocServer32](inprocserver32.md) ou [InprocHandler32](inprochandler32.md) .

Quando um aplicativo deseja remover o componente do sistema, ele deve cancelar o registro desse componente chamando [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Nessa chamada, o servidor remove exatamente as entradas que ele criou anteriormente em [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver). O servidor não deve remover de forma oculta todas as entradas de suas classes porque outro software pode ter armazenado entradas adicionais, como uma chave [Treats](treatas.md) .

Se o servidor for empacotado em um módulo EXE, o aplicativo que deseja registrar o servidor iniciará o servidor EXE com o argumento de linha de comando **/RegServer** ou **-RegServer** (não diferencia maiúsculas de minúsculas). Se o aplicativo quiser cancelar o registro do servidor, ele iniciará o EXE com o argumento de linha de comando **opção/UnregServer** ou **-UnregServer**. O EXE de registro automático detecta esses argumentos de linha de comando e invoca as mesmas operações que uma DLL dentro de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectivamente, registrando seu caminho de módulo em [LocalServer32](localserver32.md) em vez de **InprocServer32** ou **InprocHandler32**.

O servidor deve registrar o caminho completo para o local de instalação do módulo DLL ou EXE para suas respectivas chaves **InprocServer32**, **InprocHandler32** e **LocalServer32** no registro. O caminho do módulo é facilmente obtido por meio da função [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instalando como um aplicativo de serviço](installing-as-a-service-application.md)
</dt> <dt>

[Registrando uma classe na instalação](registering-a-class-at-installation.md)
</dt> <dt>

[Registrando um servidor EXE em execução](registering-a-running-exe-server.md)
</dt> <dt>

[Registrando objetos no corrompidos](registering-objects-in-the-rot.md)
</dt> </dl>

 

 