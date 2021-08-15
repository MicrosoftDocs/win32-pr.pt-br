---
description: Este tópico descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funções DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8c10951c63e14656fa967693145444c5d5fbffd96a2b11fa9ae4201ac89ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821080"
---
# <a name="dll-functions"></a>Funções DLL

Este tópico descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow.

Uma DLL deve implementar as funções a seguir para que ela possa ser registrada, não registrada e carregada na memória.

-   [*DllMain:*](/windows/desktop/Dlls/dllmain)o ponto de entrada da DLL. O nome *DllMain* é um espaço reservado para o nome da função definida pela biblioteca. A DirectShow implementação usa o nome **DllEntryPoint**. Para obter mais informações, consulte o SDK da plataforma.
-   [**DllGetClassObject:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject)cria uma instância de fábrica de classe. Descrito nas seções anteriores.
-   [**DllCanUnloadNow:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)consulta se a DLL pode ser descarregada com segurança.
-   [**DllRegisterServer:**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)cria entradas do Registro para a DLL.
-   [**DllUnregisterServer:**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)remove as entradas do Registro para a DLL.

Desses, os três primeiros são implementados por DirectShow. Se o modelo de fábrica fornece uma função de inicialização na variável de membro [**m \_ lpfnInit,**](cfactorytemplate-m-lpfninit.md) essa função é chamada de dentro da função de ponto de entrada DLL. Para obter mais informações sobre quando o sistema chama a função de ponto de entrada DLL, [*consulte DllMain*](/windows/desktop/Dlls/dllmain).

Você deve implementar [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer,**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)mas DirectShow fornece uma função chamada [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) que faz o trabalho necessário. O componente pode simplesmente envolver essa função, conforme mostrado no exemplo a seguir:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



No entanto, [**em DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer,**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) você pode personalizar o processo de registro conforme necessário. Se a DLL contiver um filtro, talvez seja necessário fazer algum trabalho adicional. Para obter mais informações, [consulte How to Register DirectShow Filters](how-to-register-directshow-filters.md).

No arquivo de definição de módulo (.def), exporte todas as funções de DLL, exceto a função de ponto de entrada. Veja a seguir um exemplo de arquivo .def:


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



Você pode registrar a DLL usando o utilitário Regsvr32.exe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar uma DLL DirectShow filtro de dados](how-to-create-a-dll.md)
</dt> </dl>

 

 
