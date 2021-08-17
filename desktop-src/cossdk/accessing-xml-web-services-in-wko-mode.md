---
description: Você pode acessar e usar qualquer serviço Web XML, mesmo que esse serviço Web XML não tenha sido criado usando COM+ ou até mesmo Microsoft Windows, desde que o Serviço Web XML publique uma descrição WSDL de sua sintaxe.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Acessando serviços Web XML no modo WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f412a1ec6493e713d2635136b2c4e82063cde56c30358653e476f300ffd2ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129398"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Acessando serviços Web XML no modo WKO

Você pode acessar e usar qualquer serviço Web XML, mesmo que esse serviço Web XML não tenha sido criado usando COM+ ou até mesmo Microsoft Windows, desde que o Serviço Web XML publique uma descrição WSDL de sua sintaxe. Basta criar uma instância do componente usando o moniker soap:wsdl=URL, em que URL é a URL da descrição WSDL do serviço Web XML que você deseja acessar. Esse é o modo WKO (objeto conhecido) de acessar serviços Web XML.

Os métodos do objeto podem ser chamados sem considerações especiais. O serviço Web XML é acessado por meio de uma consulta SOAP e a resposta é interpretada de forma transparente.

## <a name="component-services-administrative-tool"></a>Ferramenta Administrativa dos Serviços de Componentes

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

O fragmento de código Visual Basic Microsoft a seguir ilustra o uso de um serviço Web XML no modo WKO.


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



Neste fragmento de código, que ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML, servername é o nome de domínio totalmente qualificado do servidor que oferece o serviço Web XML; vroot é o diretório raiz virtual do IIS do qual o serviço Web XML é exposto; e progID é o ProgID do componente que você deseja usar.

## <a name="cc"></a>C/C++

O fragmento de código a seguir ilustra o uso de um serviço Web XML no modo WKO.


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



Neste fragmento de código, que ilustra o uso de um componente de um aplicativo COM+ que foi exposto como um serviço Web XML, servername é o nome de domínio totalmente qualificado do servidor que oferece o serviço Web XML; vroot é o diretório raiz virtual do IIS do qual o serviço Web XML é exposto; e progID é o ProgID do componente que você deseja usar.

## <a name="remarks"></a>Comentários

Quando um serviço Web XML é acessado pela primeira vez no modo WKO, o COM+ gera um cliente proxy e o compila em segundo plano. Essa geração de tempo de execução e a falta de conexões persistentes no modo WKO resulta em um desempenho significativamente reduzido em comparação com o modo DECOD.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando serviços Web XML no modo XML](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Visão geral do serviço COM+ SOAP](com--soap-service-overview.md)
</dt> <dt>

[Criando serviços Web XML](creating-xml-web-services.md)
</dt> <dt>

[Proteger serviços Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



