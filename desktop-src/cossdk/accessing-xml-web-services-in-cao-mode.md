---
description: Se o serviço Web XML que você deseja acessar foi criado pela exposição de um aplicativo COM+, considere acessá-lo no modo de objeto ativado pelo cliente (CAO), que evita a geração de um proxy e aumenta o desempenho usando conexões persistentes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Acessando serviços Web XML no modo CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810493"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Acessando serviços Web XML no modo CAO

Se o serviço Web XML que você deseja acessar foi criado pela exposição de um aplicativo COM+, considere acessá-lo no modo de objeto ativado pelo cliente (CAO), que evita a geração de um proxy e aumenta o desempenho usando conexões persistentes. Para acessar um serviço Web XML no modo CAO, primeiro [exporte](exporting-a-soap-enabled-application.md) o aplicativo habilitado para SOAP correspondente do servidor no modo proxy e, em seguida, [importe](importing-a-soap-enabled-application.md) o aplicativo para o cliente do qual você deseja acessar o aplicativo como um serviço Web XML. Os componentes do aplicativo podem então ser instanciados no cliente, assim como os componentes de aplicativos locais, por exemplo, usando **GetObject** e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Interface do Usuário

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

O fragmento de código Visual Basic a seguir ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML no modo CAO.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

O fragmento de código a seguir ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML no modo CAO.


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

[Visão geral do serviço SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Criando Serviços Web XML](creating-xml-web-services.md)
</dt> <dt>

[Protegendo serviços Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 
