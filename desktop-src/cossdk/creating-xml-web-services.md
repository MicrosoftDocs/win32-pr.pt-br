---
description: Qualquer aplicativo COM+ pode ser exposto como um serviço Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Criando Serviços Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796222"
---
# <a name="creating-xml-web-services"></a>Criando Serviços Web XML

Qualquer aplicativo COM+ pode ser exposto como um serviço Web XML. Os métodos nas interfaces padrão dos componentes configurados aplicativos (componentes no catálogo COM+ de servidores) podem ser chamados remotamente. Você pode usar a ferramenta administrativa serviços de componentes para criar um diretório raiz virtual do IIS a partir do qual os métodos de componente podem ser chamados usando SOAP.

> [!Note]  
> O .NET Framework deve ser instalado em seu computador para expor um aplicativo COM+ como um serviço Web XML.

 

**Para expor um aplicativo COM+ como um serviço Web XML**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.

2.  Clique com o botão direito do mouse no aplicativo que você deseja expor como um serviço Web XML e escolha **Propriedades**.

3.  Clique na guia **ativação** na caixa de diálogo Propriedades.

4.  Marque a caixa de seleção **usa SOAP** .

5.  Na caixa de texto **Vroot do SOAP** , digite o nome do diretório raiz virtual do IIS do qual os métodos dos componentes podem ser acessados remotamente. Observe que uma VRoot SOAP não pode ser um subdiretório de outro diretório VRoot SOAP.

6.  Clique em **OK**.

    Se você especificar o diretório raiz virtual do IIS como *vroot* e se o nome de domínio totalmente qualificado de seus servidores for *ServerName*, a URL em que o componente é exposto como um serviço Web XML é https://*ServerName* / *vroot*/.

    O diretório correspondente no sistema de arquivos é o \\ Windows \\ System32 \\ com \\ SoapVRoots \\ *vroot* \\ ; O COM+ coloca vários arquivos de configuração e programas ASP.NET. Para um serviço Web XML sob carga pesada, talvez você queira ajustar os parâmetros armazenados no arquivo web.config. Para obter informações sobre esse arquivo, consulte a documentação do IIS.

    As configurações de segurança padrão para um aplicativo COM+ exposto como um serviço Web XML diferem dependendo de qual versão do .NET Framework está instalada. Se a versão 1,0 estiver instalada, os serviços Web XML não serão seguros por padrão; todas as chamadas são aceitas e nenhuma criptografia é usada. Se a versão 1,1 ou posterior estiver instalada, os serviços Web XML serão protegidos por padrão; os chamadores devem ser autenticados e a criptografia é necessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando serviços Web XML no modo CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Acessando serviços Web XML no modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Visão geral do serviço SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Protegendo serviços Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



