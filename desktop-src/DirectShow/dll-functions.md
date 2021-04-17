---
description: Este tópico descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funções de DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105748797"
---
# <a name="dll-functions"></a>Funções de DLL

Este tópico descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow.

Uma DLL deve implementar as seguintes funções para que possam ser registradas, canceladas e carregadas na memória.

-   [*DllMain*](/windows/desktop/Dlls/dllmain): o ponto de entrada de dll. O nome *DllMain* é um espaço reservado para o nome da função definida pela biblioteca. A implementação do DirectShow usa o nome **DllEntryPoint**. Para obter mais informações, consulte o SDK da plataforma.
-   [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): cria uma instância de fábrica de classes. Descrito nas seções anteriores.
-   [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): consulta se a dll pode ser descarregada com segurança.
-   [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): cria entradas de registro para a dll.
-   [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): remove entradas do registro para a dll.

Desses, os três primeiros são implementados pelo DirectShow. Se o modelo de fábrica fornecer uma função de inicialização na variável de membro [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) , essa função será chamada de dentro da função de ponto de entrada de dll. Para obter mais informações sobre quando o sistema chama a função de ponto de entrada de DLL, consulte [*DllMain*](/windows/desktop/Dlls/dllmain).

Você deve implementar [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), mas o DirectShow fornece uma função chamada [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) que faz o trabalho necessário. O componente pode simplesmente encapsular essa função, conforme mostrado no exemplo a seguir:


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



No entanto, dentro de [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) , você pode personalizar o processo de registro conforme necessário. Se sua DLL contiver um filtro, talvez seja necessário fazer algum trabalho adicional. Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).

No arquivo de definição de módulo (. def), exporte todas as funções de DLL, exceto a função de ponto de entrada. Este é um arquivo. def de exemplo:


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

[Como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
