---
description: Se o serviço Web XML que você deseja acessar foi criado expondo um aplicativo COM+, considere acessá-lo no modo DE (objeto ativado pelo cliente), o que evita a geração de tempo de execução de um proxy e aumenta o desempenho usando conexões persistentes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Acessando serviços Web XML no modo XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3f8dc1fa3c037d03d8b69cf45737c7211d92f7d38e733a97b9be109a2243a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549439"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Acessando serviços Web XML no modo XML

Se o serviço Web XML que você deseja acessar foi criado expondo um aplicativo COM+, considere acessá-lo no modo DE (objeto ativado pelo cliente), o que evita a geração de tempo de execução de um proxy e aumenta o desempenho usando conexões persistentes. Para acessar um serviço Web XML [](exporting-a-soap-enabled-application.md) no modo XML, primeiro exporte o aplicativo [](importing-a-soap-enabled-application.md) habilitado para SOAP correspondente do seu servidor no modo proxy e, em seguida, importe o aplicativo para o cliente do qual você deseja acessar o aplicativo como um serviço Web XML. Os componentes do aplicativo podem ser instanados no cliente assim como os componentes de aplicativos locais, por exemplo, usando **GetObject** e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Interface do Usuário

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

O seguinte Visual Basic fragmento de código ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML no modo XML.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

O fragmento de código a seguir ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML no modo XML.


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando serviços Web XML no modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Visão geral do serviço COM+ SOAP](com--soap-service-overview.md)
</dt> <dt>

[Criando serviços Web XML](creating-xml-web-services.md)
</dt> <dt>

[Proteger serviços Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 
